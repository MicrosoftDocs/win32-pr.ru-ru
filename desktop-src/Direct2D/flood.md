---
title: Результат переполнения
description: Используйте результат переполнения для создания точечного рисунка на основе заданного цвета и альфа-значения. Этот результат можно использовать, если требуется конкретный цвет в качестве входного для действия, например цвет фона.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- результат переполнения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989038"
---
# <a name="flood-effect"></a><span data-ttu-id="c2fc5-105">Результат переполнения</span><span class="sxs-lookup"><span data-stu-id="c2fc5-105">Flood effect</span></span>

<span data-ttu-id="c2fc5-106">Используйте результат переполнения для создания точечного рисунка на основе заданного цвета и альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-106">Use the flood effect to generate a bitmap based on the specified color and alpha value.</span></span> <span data-ttu-id="c2fc5-107">Этот результат можно использовать, если требуется конкретный цвет в качестве входного для действия, например цвет фона.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-107">You can use this effect when you want a specific color as an input for an effect, like a background color.</span></span>

> [!Note]  
> <span data-ttu-id="c2fc5-108">Этот результат передается по указанному значению цвета.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-108">The effect passes along the specified color value as specified.</span></span> <span data-ttu-id="c2fc5-109">Необходимо вручную выполнить предварительное умножение значений, если планируется передать выходные данные эффектам, которые предполагают предварительно умноженные входные данные.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-109">You must manually pre-multiply the values if you plan to pass the output to effects that expect a pre-multiplied input.</span></span>

 

<span data-ttu-id="c2fc5-110">Идентификатором CLSID для этого действия является CLSID \_ D2D1Flood.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-110">The CLSID for this effect is CLSID\_D2D1Flood.</span></span>

<span data-ttu-id="c2fc5-111">Результат переполнения не имеет входного изображения.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-111">The flood effect has no input image.</span></span>

-   [<span data-ttu-id="c2fc5-112">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="c2fc5-112">Example image</span></span>](#example-image)
-   [<span data-ttu-id="c2fc5-113">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="c2fc5-113">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c2fc5-114">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="c2fc5-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="c2fc5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c2fc5-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c2fc5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="c2fc5-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c2fc5-117">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="c2fc5-117">Example image</span></span>

![Пример изображения, которое выводится зеленым цветом.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="c2fc5-119">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="c2fc5-119">Effect properties</span></span>



| <span data-ttu-id="c2fc5-120">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="c2fc5-120">Display name and index enumeration</span></span>                   | <span data-ttu-id="c2fc5-121">Описание</span><span class="sxs-lookup"><span data-stu-id="c2fc5-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2fc5-122">Цвет</span><span class="sxs-lookup"><span data-stu-id="c2fc5-122">Color</span></span><br/> <span data-ttu-id="c2fc5-123">\_ \_ Цвет Prop D2D1 \_ Flood</span><span class="sxs-lookup"><span data-stu-id="c2fc5-123">D2D1\_FLOOD\_PROP\_COLOR</span></span><br/> | <span data-ttu-id="c2fc5-124">Цвет и непрозрачность точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-124">The color and opacity of the bitmap.</span></span> <span data-ttu-id="c2fc5-125">Это свойство является D2D1 \_ векторным \_ 4Fом.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-125">This property is a D2D1\_VECTOR\_4F.</span></span> <span data-ttu-id="c2fc5-126">Отдельные значения для каждого канала имеют тип FLOAT, без привязки и без единицы.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-126">The individual values for each channel are of type FLOAT, unbounded and unitless.</span></span> <span data-ttu-id="c2fc5-127">Этот результат не изменяет значения для каналов.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-127">The effect doesn't modify the values for the channels.</span></span><br/> <span data-ttu-id="c2fc5-128">Значения RGBA для каждого канала в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-128">The RGBA values for each channel range from 0 to 1.</span></span><br/> <span data-ttu-id="c2fc5-129">Тип — D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-129">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="c2fc5-130">Значение по умолчанию — {0.0 f, 0,0 f, 0,0 f, 1,0 f}.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-130">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="c2fc5-131">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="c2fc5-131">Output bitmap</span></span>

<span data-ttu-id="c2fc5-132">Этот результат приводит к созданию точечного рисунка с логически бесконечным размером.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-132">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2fc5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c2fc5-133">Requirements</span></span>



| <span data-ttu-id="c2fc5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c2fc5-134">Requirement</span></span> | <span data-ttu-id="c2fc5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c2fc5-135">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2fc5-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2fc5-136">Minimum supported client</span></span> | <span data-ttu-id="c2fc5-137">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="c2fc5-137">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c2fc5-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2fc5-138">Minimum supported server</span></span> | <span data-ttu-id="c2fc5-139">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="c2fc5-139">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c2fc5-140">Header</span><span class="sxs-lookup"><span data-stu-id="c2fc5-140">Header</span></span>                   | <span data-ttu-id="c2fc5-141">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c2fc5-141">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c2fc5-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2fc5-142">Library</span></span>                  | <span data-ttu-id="c2fc5-143">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="c2fc5-143">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c2fc5-144">См. также</span><span class="sxs-lookup"><span data-stu-id="c2fc5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2fc5-145">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c2fc5-145">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

