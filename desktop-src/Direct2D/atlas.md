---
title: Результат Atlas
description: Этот результат можно использовать для вывода части изображения, но не хранить его вне части для использования в последующих операциях.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492126"
---
# <a name="atlas-effect"></a><span data-ttu-id="35c63-103">Результат Atlas</span><span class="sxs-lookup"><span data-stu-id="35c63-103">Atlas effect</span></span>

<span data-ttu-id="35c63-104">Этот результат можно использовать для вывода части изображения, но не хранить его вне части для использования в последующих операциях.</span><span class="sxs-lookup"><span data-stu-id="35c63-104">You can use this effect to output a portion of an image but retain the region outside of the portion for use in subsequent operations.</span></span>

<span data-ttu-id="35c63-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1Atlas.</span><span class="sxs-lookup"><span data-stu-id="35c63-105">The CLSID for this effect is CLSID\_D2D1Atlas.</span></span>

<span data-ttu-id="35c63-106">Результат Atlas удобен, если требуется загрузить крупное изображение, состоящие из нескольких небольших изображений, таких как различные кадры спрайта.</span><span class="sxs-lookup"><span data-stu-id="35c63-106">The atlas effect is useful if you want to load a large image made up of many smaller images, such as various frames of a sprite.</span></span>

<span data-ttu-id="35c63-107">Чтобы создать выходные данные, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="35c63-107">To create the output the effect:</span></span>

1.  <span data-ttu-id="35c63-108">Обрезает входные данные в заданное свойство *инпутрект* .</span><span class="sxs-lookup"><span data-stu-id="35c63-108">Crops the input to the given *InputRect* property.</span></span>
2.  <span data-ttu-id="35c63-109">Преобразует происхождение результата в (0, 0).</span><span class="sxs-lookup"><span data-stu-id="35c63-109">Translates the origin of the result to (0,0).</span></span>

> [!Note]  
> <span data-ttu-id="35c63-110">Свойство *инпутпаддингрект* должно быть больше только только в том случае, если Пиксели между двумя прямоугольниками являются прозрачными черными для входных данных.</span><span class="sxs-lookup"><span data-stu-id="35c63-110">The *InputPaddingRect* property should only be larger if and only if the pixels between the two rectangles are transparent black on the input.</span></span> <span data-ttu-id="35c63-111">Это может привести к более оптимальному выполнению графа Direct2D.</span><span class="sxs-lookup"><span data-stu-id="35c63-111">This may result in Direct2D executing the graph more optimally.</span></span>

 

<span data-ttu-id="35c63-112">Ниже приведен пример этого результата.</span><span class="sxs-lookup"><span data-stu-id="35c63-112">Here is an example of the effect.</span></span> <span data-ttu-id="35c63-113">Это изображение является небольшим и простым для наглядности.</span><span class="sxs-lookup"><span data-stu-id="35c63-113">This image is small and simple for illustration purposes.</span></span>

![входной образ.](images/atlas.png)

<span data-ttu-id="35c63-115">Предыдущее изображение — это входные данные для действия.</span><span class="sxs-lookup"><span data-stu-id="35c63-115">The preceding image is the input to the effect.</span></span> <span data-ttu-id="35c63-116">Здесь код создает результат Atlas, устанавливает входные данные, устанавливает прямоугольник ввода, а затем рисует выходные данные.</span><span class="sxs-lookup"><span data-stu-id="35c63-116">The code here creates an atlas effect, sets the input, sets the input rectangle, and then draws the output.</span></span>


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



<span data-ttu-id="35c63-117">Предыдущий код выбирает прямоугольник вокруг второго треугольника.</span><span class="sxs-lookup"><span data-stu-id="35c63-117">The preceding code selects a rectangle that is around the second triangle.</span></span> <span data-ttu-id="35c63-118">Заполнение вокруг него игнорируется.</span><span class="sxs-lookup"><span data-stu-id="35c63-118">The padding around it is ignored.</span></span> <span data-ttu-id="35c63-119">Это полученное изображение.</span><span class="sxs-lookup"><span data-stu-id="35c63-119">Here is the resulting image.</span></span>

![изображение вывода.](images/atlas2.png)

> [!Note]  
> <span data-ttu-id="35c63-121">Это ситуация, когда вы можете указать *инпутпаддингрект* , так как заполнение является прозрачным черным.</span><span class="sxs-lookup"><span data-stu-id="35c63-121">This is a situation where you may choose to specify a *InputPaddingRect* because the padding is transparent black.</span></span> <span data-ttu-id="35c63-122">Прямоугольник будет иметь вид `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .</span><span class="sxs-lookup"><span data-stu-id="35c63-122">The rectangle would be `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);`.</span></span>

 

## <a name="effect-properties"></a><span data-ttu-id="35c63-123">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="35c63-123">Effect properties</span></span>



| <span data-ttu-id="35c63-124">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="35c63-124">Display name and index enumeration</span></span>                                             | <span data-ttu-id="35c63-125">Описание</span><span class="sxs-lookup"><span data-stu-id="35c63-125">Description</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c63-126">инпутрект</span><span class="sxs-lookup"><span data-stu-id="35c63-126">InputRect</span></span><br/> <span data-ttu-id="35c63-127">\_ \_ \_ Входной прямоугольник D2D1 Atlas \_ prop</span><span class="sxs-lookup"><span data-stu-id="35c63-127">D2D1\_ATLAS\_PROP\_INPUT\_RECT</span></span><br/>                 | <span data-ttu-id="35c63-128">Часть изображения, передаваемая следующему результату.</span><span class="sxs-lookup"><span data-stu-id="35c63-128">The portion of the image passed to the next effect.</span></span><br/> <span data-ttu-id="35c63-129">Тип — D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="35c63-129">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="35c63-130">Значение по умолчанию — (-ФЛТ \_ Max,-ФЛТ \_ Max, ФЛТ \_ Max, ФЛТ \_ max).</span><span class="sxs-lookup"><span data-stu-id="35c63-130">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span> <br/> |
| <span data-ttu-id="35c63-131">инпутпаддингрект</span><span class="sxs-lookup"><span data-stu-id="35c63-131">InputPaddingRect</span></span><br/> <span data-ttu-id="35c63-132">D2D1 \_ Atlas \_ для \_ \_ заполнения входного \_ прямоугольника</span><span class="sxs-lookup"><span data-stu-id="35c63-132">D2D1\_ATLAS\_PROP\_INPUT\_PADDING\_RECT</span></span><br/> | <span data-ttu-id="35c63-133">Максимальный размер образца для выходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="35c63-133">The maximum size sampled for the output rectangle.</span></span><br/> <span data-ttu-id="35c63-134">Тип — D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="35c63-134">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="35c63-135">Значение по умолчанию — (-ФЛТ \_ Max,-ФЛТ \_ Max, ФЛТ \_ Max, ФЛТ \_ max).</span><span class="sxs-lookup"><span data-stu-id="35c63-135">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="35c63-136">Требования</span><span class="sxs-lookup"><span data-stu-id="35c63-136">Requirements</span></span>



| <span data-ttu-id="35c63-137">Требование</span><span class="sxs-lookup"><span data-stu-id="35c63-137">Requirement</span></span> | <span data-ttu-id="35c63-138">Значение</span><span class="sxs-lookup"><span data-stu-id="35c63-138">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35c63-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35c63-139">Minimum supported client</span></span> | <span data-ttu-id="35c63-140">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="35c63-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="35c63-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35c63-141">Minimum supported server</span></span> | <span data-ttu-id="35c63-142">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="35c63-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="35c63-143">Header</span><span class="sxs-lookup"><span data-stu-id="35c63-143">Header</span></span>                   | <span data-ttu-id="35c63-144">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="35c63-144">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="35c63-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="35c63-145">Library</span></span>                  | <span data-ttu-id="35c63-146">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="35c63-146">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="35c63-147">См. также</span><span class="sxs-lookup"><span data-stu-id="35c63-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35c63-148">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="35c63-148">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

