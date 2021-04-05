---
description: Указывает, копирует ли Media Foundation преобразование (MFT) атрибуты из входных образцов в выходные.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Свойство MFPKEY_EXATTRIBUTE_SUPPORTED (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908779"
---
# <a name="mfpkey_exattribute_supported-property"></a>МФПКЭЙ \_ ексаттрибуте \_ поддерживаемое свойство

Указывает, копирует ли Media Foundation преобразование (MFT) атрибуты из входных образцов в выходные.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**VARIANT \_ bool**

Логическое значение VT \_

**булвал**



## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[**Имфтрансформ::P Роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




