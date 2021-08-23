---
description: Указывает, копирует ли Media Foundation преобразование (MFT) атрибуты из входных образцов в выходные.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Свойство MFPKEY_EXATTRIBUTE_SUPPORTED (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248609828df3ef977112058ffe0d169104e68c181fa455ef27f2adcea0220aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663513"
---
# <a name="mfpkey_exattribute_supported-property"></a>МФПКЭЙ \_ ексаттрибуте \_ поддерживаемое свойство

Указывает, копирует ли Media Foundation преобразование (MFT) атрибуты из входных образцов в выходные.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**VARIANT \_ bool**

Логическое значение VT \_

**булвал**



## <a name="remarks"></a>Remarks

Этот атрибут может иметь следующие значения.



| Значение              | Описание                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ВАРИАНТ \_ true**  | MFT копирует атрибуты из входных примеров в выходные образцы.                                                                                 |
| **ВАРИАНТ \_ false** | Сеанс мультимедиа копирует атрибуты из входных примеров в выходные образцы. Он не перезаписывает никакие атрибуты, которые задаются MFT в выходных образцах. |



 

Чтобы получить этот атрибут, вызовите **QueryInterface** в MFT для интерфейса **ипропертисторе** .

Значение по умолчанию — **Variant \_ false**. Если таблица MFT не предоставляет интерфейс **ипропертисторе** или если это свойство не задано, то следует рассматривать значение как **Variant \_ false**.

Это свойство доступно только для чтения.

> [!NOTE] 
> Этот атрибут не применяется к асинхронному МФТС. Атрибуты не будут скопированы из входных примеров в выходные данные для асинхронного МФТС, независимо от значения этого атрибута.

## <a name="examples"></a>Примеры

В следующем примере возвращается значение VARIANT \_ true, если в MFT копируются образцы атрибутов.


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[**Имфтрансформ::P Роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




