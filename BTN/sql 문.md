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