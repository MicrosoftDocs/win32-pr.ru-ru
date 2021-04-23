---
description: Источник цвета видео
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Источник цвета видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265256"
---
# <a name="video-color-source"></a><span data-ttu-id="0f5fc-103">Источник цвета видео</span><span class="sxs-lookup"><span data-stu-id="0f5fc-103">Video Color Source</span></span>

> [!Note]  
> <span data-ttu-id="0f5fc-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-104">\[Deprecated.</span></span> <span data-ttu-id="0f5fc-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f5fc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0f5fc-106">Источник видеоцвета создает непрерывное изображение с сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-106">The Video Color Source creates a continuous video image of a solid color.</span></span>

<span data-ttu-id="0f5fc-107">Идентификатор класса (CLSID): **{0CFDD070-581A-11d2-9EE6-006008039E37}**</span><span class="sxs-lookup"><span data-stu-id="0f5fc-107">Class ID (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span></span>

<span data-ttu-id="0f5fc-108">Имя переменной CLSID: **CLSID \_ колорсаурце**</span><span class="sxs-lookup"><span data-stu-id="0f5fc-108">CLSID Variable Name: **CLSID\_ColorSource**</span></span>

<span data-ttu-id="0f5fc-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f5fc-109">Properties</span></span>



| <span data-ttu-id="0f5fc-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="0f5fc-110">Property</span></span> | <span data-ttu-id="0f5fc-111">Тип</span><span class="sxs-lookup"><span data-stu-id="0f5fc-111">Type</span></span>      | <span data-ttu-id="0f5fc-112">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="0f5fc-112">Default</span></span> | <span data-ttu-id="0f5fc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0f5fc-113">Description</span></span>                                   |
|----------|-----------|---------|-----------------------------------------------|
| <span data-ttu-id="0f5fc-114">Color</span><span class="sxs-lookup"><span data-stu-id="0f5fc-114">"Color"</span></span>  | <span data-ttu-id="0f5fc-115">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="0f5fc-115">**DWORD**</span></span> | <span data-ttu-id="0f5fc-116">0</span><span class="sxs-lookup"><span data-stu-id="0f5fc-116">0</span></span>       | <span data-ttu-id="0f5fc-117">Задает создаваемый цвет.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-117">Specifies the color to generate.</span></span> <span data-ttu-id="0f5fc-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-118">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0f5fc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f5fc-119">Remarks</span></span>

<span data-ttu-id="0f5fc-120">Источник цвет видео используется с исходными объектами.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-120">The Video Color Source is used with source objects.</span></span> <span data-ttu-id="0f5fc-121">Сначала создайте новый исходный объект.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-121">First, create a new source object.</span></span> <span data-ttu-id="0f5fc-122">Затем задайте для GUID подобъекта исходного объекта значение CLSID \_ колорсаурце, вызвав метод [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="0f5fc-122">Then set the source object's subobject GUID to CLSID\_ColorSource, by calling the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="0f5fc-123">Чтобы задать цвет, создайте объект [задания свойств](property-setter.md) и примените свойство "Color" в момент нулевого значения.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-123">To set the color, create a [Property Setter](property-setter.md) object and apply the "Color" property at time zero.</span></span> <span data-ttu-id="0f5fc-124">Значение этого свойства представляет собой шестнадцатеричное число в формате *0xAARRGGBB*, где *AA* — альфа-значение, *RR* — это значение красного *цвета, то есть —* зеленым значением, а *BB* — синим.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-124">The value of this property is a hexadecimal number with the format *0xAARRGGBB*, where *AA* is the alpha value, *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="0f5fc-125">Значения альфа находятся в диапазоне от 0x00 (прозрачный) до 0xFF (непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="0f5fc-125">Alpha values range from 0x00 (transparent) to 0xFF (opaque).</span></span> <span data-ttu-id="0f5fc-126">Свойство является статическим и должно применяться во время нулевого значения.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-126">The property is static and must be applied at time zero.</span></span>

<span data-ttu-id="0f5fc-127">Если значение альфа не указано, по умолчанию оно равно нулю (прозрачный).</span><span class="sxs-lookup"><span data-stu-id="0f5fc-127">If you do not specify the alpha value, it defaults to zero (transparent).</span></span> <span data-ttu-id="0f5fc-128">В проекте видео в 32-разрядном цвете это приведет к тому, что переходы или эффекты, использующие альфа, будут визуализировать источник цвета видео как полностью прозрачный.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-128">In a 32-bit-color video project, this will cause transitions or effects that use alpha to render the Video Color Source as completely transparent.</span></span> <span data-ttu-id="0f5fc-129">Чтобы обеспечить безопасность, всегда указывайте альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-129">To be safe, always specify the alpha.</span></span> <span data-ttu-id="0f5fc-130">Например, непрозрачный черный — **0xFF000000**.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-130">For example, opaque black is **0xFF000000**.</span></span>

<span data-ttu-id="0f5fc-131">В следующем примере кода показано, как использовать этот объект.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-131">The following code example shows how to use this object.</span></span> <span data-ttu-id="0f5fc-132">Дополнительные сведения об использовании [**ипропертисеттер**](ipropertysetter.md)см. [в разделе Задание свойств для эффектов и переходов](setting-properties-on-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="0f5fc-132">For more information about using [**IPropertySetter**](ipropertysetter.md), see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md):</span></span>


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



<span data-ttu-id="0f5fc-133">В следующем примере показано XML-представление объекта, созданного в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-133">The following example shows the XML representation of the object created in the previous example.</span></span> <span data-ttu-id="0f5fc-134">В этом случае элемент [**param**](param-element.md) не поддерживает [**в**](at-element.md) или [**линейные**](linear-element.md) элементы, так как объект не поддерживает динамические свойства:</span><span class="sxs-lookup"><span data-stu-id="0f5fc-134">In this case the [**param**](param-element.md) element does not support [**at**](at-element.md) or [**linear**](linear-element.md) elements, because the object does not support dynamic properties:</span></span>


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



