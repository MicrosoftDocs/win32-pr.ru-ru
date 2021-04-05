---
description: Указывает, выполняет ли преобразование Media Foundation (MFT) асинхронную обработку.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: Атрибут MF_TRANSFORM_ASYNC (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811014"
---
# <a name="mf_transform_async-attribute"></a>\_ \_ Асинхронный атрибут преобразования MF

Указывает, выполняет ли преобразование Media Foundation (MFT) асинхронную обработку.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Атрибут является логическим значением:

-   Если атрибут не равен нулю, то MFT выполняет асинхронную обработку.
-   Если атрибут равен 0 или не задан, MFT является синхронным.

Чтобы получить этот атрибут, сначала вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить хранилище атрибутов MFT. Если этот метод завершился с ошибкой, вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить значение атрибута. Если один из двух методов завершается неудачей, MFT является синхронным.

Для асинхронного МФТС этому атрибуту должно быть присвоено ненулевое значение. Для синхронного МФТС этот атрибут является необязательным, но при его наличии его необходимо задать равным 0.

Асинхронные МФТС несовместимы с более ранними версиями Media Foundation. Чтобы использовать асинхронную таблицу MFT, клиент должен задать атрибут [**MF \_ Transform \_ Async \_ reunlock**](mf-transform-async-unlock.md) в MFT. (Microsoft Media Foundation конвейер выполняет этот шаг автоматически.)

## <a name="examples"></a>Примеры

Следующий код проверяет, выполняет ли MFT асинхронную обработку.


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Асинхронный МФТС](asynchronous-mfts.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> <dt>

[**\_ \_ асинхронное \_ деблокирование преобразования MF**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




