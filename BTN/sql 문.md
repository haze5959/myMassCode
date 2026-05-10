// 바코드 넣기
INSERT INTO public.barcodes (id, barcode_id, product_id)
VALUES (
    gen_random_uuid(), 
    'barcode_id', 
    'product_id'
);

// 제품 id로 제품 찾기
SELECT * FROM public.products
WHERE id = '54f98f7e-0d9f-4c34-98ec-57e6dd3149e1';

// 바코드로 제품 찾기
SELECT p.*
FROM public.products p
JOIN public.barcodes b ON p.id = b.product_id
WHERE b.barcode_id = '찾으려는_바코드_값';

// 바코드에서 제품 바꾸기
UPDATE public.barcodes
SET product_id = '0aedb48a-f023-43fe-8250-dae8fdb2da28'
WHERE barcode_id = '7501035011434';