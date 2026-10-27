# 可编辑提示词骨架

根据当前图片填写花括号字段；不把未核实细节填成事实。交付实际运行的提示词前清除未填写字段，或先向用户说明缺失项。

```text
Create one premium {framing} {aspect_ratio} e-commerce fashion image: {view} view.

Use {product_reference_ids} as the authoritative references for the garment only. Use {model_reference_id} as the fixed model reference: preserve {identity_hair_proportions_and_selected_accessories}. Preserve {background_reference_and_scene_details}. Follow {pose_or_pose_style}.

Replace {explicit_old_garments_and_accessories_to_remove} with {target_garment}. Preserve exactly the visible product details: {neckline}; {sleeves_and_cuffs}; {waist_construction_and_fit}; {length_and_hem}; {color}; {pattern_scale_and_distribution}; {texture_and_sheen}; {other_verified_details}.

Do not introduce {unwanted_old_items_or_extra_styling}. No extra limbs, unintended text or watermark, or changes to the specified model and background. {sku_specific_failure_correction}.
```

对已有 logo/文字按商品证据和用户要求处理；示例里的“无 logo”不能用于擅自抹除新商品的真实品牌标识。局部详情图调整 framing，不同时要求全身构图。改变视角时保留人物身份和场景风格，不把“姿势完全不动”与背面拍摄同时写入。

历史示例的局部修正：

```text
Keep the waist drape soft and natural; do not make the dress tight-fitting or transform it into a wrap dress.
```

这句话仅在商品确有该结构时使用。修正应针对已观察到的误差或明确的 SKU 约束。
