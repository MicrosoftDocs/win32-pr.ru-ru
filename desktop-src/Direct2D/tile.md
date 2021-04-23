---
title: Действие плитки
description: Используйте действие плитки для повторения указанной области изображения.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- действие плитки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071704"
---
# <a name="tile-effect"></a><span data-ttu-id="c8f75-104">Действие плитки</span><span class="sxs-lookup"><span data-stu-id="c8f75-104">Tile effect</span></span>

<span data-ttu-id="c8f75-105">Используйте действие плитки для повторения указанной области изображения.</span><span class="sxs-lookup"><span data-stu-id="c8f75-105">Use the tile effect to repeat the specified region of the image.</span></span>

<span data-ttu-id="c8f75-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1Tile.</span><span class="sxs-lookup"><span data-stu-id="c8f75-106">The CLSID for this effect is CLSID\_D2D1Tile.</span></span>

## <a name="example-image"></a><span data-ttu-id="c8f75-107">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="c8f75-107">Example image</span></span>



| <span data-ttu-id="c8f75-108">До</span><span class="sxs-lookup"><span data-stu-id="c8f75-108">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg) |
| <span data-ttu-id="c8f75-110">После</span><span class="sxs-lookup"><span data-stu-id="c8f75-110">After</span></span>                                                      |
| ![изображение после преобразования.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="c8f75-112">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="c8f75-112">Effect properties</span></span>



| <span data-ttu-id="c8f75-113">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="c8f75-113">Display name and index enumeration</span></span>                | <span data-ttu-id="c8f75-114">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c8f75-114">Type and default value</span></span>                                              | <span data-ttu-id="c8f75-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c8f75-115">Description</span></span>                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f75-116">Rect</span><span class="sxs-lookup"><span data-stu-id="c8f75-116">Rect</span></span><br/> <span data-ttu-id="c8f75-117">D2D1 \_ элемента \_ prop \_ плитки</span><span class="sxs-lookup"><span data-stu-id="c8f75-117">D2D1\_TILE\_PROP\_RECT</span></span><br/> | <span data-ttu-id="c8f75-118">D2D1 \_ vector \_ 4F</span><span class="sxs-lookup"><span data-stu-id="c8f75-118">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="c8f75-119">{0,0 f, 0,0 f, 100,0 f, 100,0 f}</span><span class="sxs-lookup"><span data-stu-id="c8f75-119">{0.0f, 0.0f, 100.0f, 100.0f}</span></span><br/> | <span data-ttu-id="c8f75-120">Область изображения для мозаичного заполнения.</span><span class="sxs-lookup"><span data-stu-id="c8f75-120">The region of the image to be tiled.</span></span> <span data-ttu-id="c8f75-121">Это свойство является D2D1 \_ вектором \_ 4F, определенным как: (слева, сверху, справа, снизу).</span><span class="sxs-lookup"><span data-stu-id="c8f75-121">This property is a D2D1\_VECTOR\_4F defined as: (left, top, right, bottom).</span></span> <span data-ttu-id="c8f75-122">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="c8f75-122">The units are in DIPs.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="c8f75-123">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="c8f75-123">Output bitmap</span></span>

<span data-ttu-id="c8f75-124">Этот результат приводит к созданию точечного рисунка с логически бесконечным размером.</span><span class="sxs-lookup"><span data-stu-id="c8f75-124">This effect generates a logically infinite sized bitmap.</span></span>

<span data-ttu-id="c8f75-125">Можно мозаично разместить изображение и вывести определенный размер без дополнительных эффектов, задав размер при вызове [**ID2D1DeviceContext::D равимаже**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span><span class="sxs-lookup"><span data-stu-id="c8f75-125">You can tile an image and output a certain size without any additional effects by setting the size when you call [**ID2D1DeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f75-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c8f75-126">Requirements</span></span>



| <span data-ttu-id="c8f75-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c8f75-127">Requirement</span></span> | <span data-ttu-id="c8f75-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c8f75-128">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f75-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8f75-129">Minimum supported client</span></span> | <span data-ttu-id="c8f75-130">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="c8f75-130">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c8f75-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8f75-131">Minimum supported server</span></span> | <span data-ttu-id="c8f75-132">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="c8f75-132">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c8f75-133">Header</span><span class="sxs-lookup"><span data-stu-id="c8f75-133">Header</span></span>                   | <span data-ttu-id="c8f75-134">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c8f75-134">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c8f75-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c8f75-135">Library</span></span>                  | <span data-ttu-id="c8f75-136">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="c8f75-136">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c8f75-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c8f75-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8f75-138">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c8f75-138">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

