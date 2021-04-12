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
# <a name="video-color-source"></a>Источник цвета видео

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Источник видеоцвета создает непрерывное изображение с сплошным цветом.

Идентификатор класса (CLSID): **{0CFDD070-581A-11d2-9EE6-006008039E37}**

Имя переменной CLSID: **CLSID \_ колорсаурце**

Свойства



| Свойство | Тип      | По умолчанию | Описание                                   |
|----------|-----------|---------|-----------------------------------------------|
| Color  | **DWORD** | 0       | Задает создаваемый цвет. См. заметки. |



 

## <a name="remarks"></a>Комментарии

Источник цвет видео используется с исходными объектами. Сначала создайте новый исходный объект. Затем задайте для GUID подобъекта исходного объекта значение CLSID \_ колорсаурце, вызвав метод [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) .

Чтобы задать цвет, создайте объект [задания свойств](property-setter.md) и примените свойство "Color" в момент нулевого значения. Значение этого свойства представляет собой шестнадцатеричное число в формате *0xAARRGGBB*, где *AA* — альфа-значение, *RR* — это значение красного *цвета, то есть —* зеленым значением, а *BB* — синим. Значения альфа находятся в диапазоне от 0x00 (прозрачный) до 0xFF (непрозрачный). Свойство является статическим и должно применяться во время нулевого значения.

Если значение альфа не указано, по умолчанию оно равно нулю (прозрачный). В проекте видео в 32-разрядном цвете это приведет к тому, что переходы или эффекты, использующие альфа, будут визуализировать источник цвета видео как полностью прозрачный. Чтобы обеспечить безопасность, всегда указывайте альфа-канал. Например, непрозрачный черный — **0xFF000000**.

В следующем примере кода показано, как использовать этот объект. Дополнительные сведения об использовании [**ипропертисеттер**](ipropertysetter.md)см. [в разделе Задание свойств для эффектов и переходов](setting-properties-on-effects-and-transitions.md).


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



В следующем примере показано XML-представление объекта, созданного в предыдущем примере. В этом случае элемент [**param**](param-element.md) не поддерживает [**в**](at-element.md) или [**линейные**](linear-element.md) элементы, так как объект не поддерживает динамические свойства:


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



