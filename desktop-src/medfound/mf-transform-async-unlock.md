---
description: Позволяет использовать асинхронное преобразование Media Foundation (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: Атрибут MF_TRANSFORM_ASYNC_UNLOCK (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543226"
---
# <a name="mf_transform_async_unlock-attribute"></a>\_ \_ Атрибут асинхронного \_ разблокировки MF Transform

Позволяет использовать асинхронное преобразование Media Foundation (MFT).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Асинхронные МФТС несовместимы с более ранними версиями Microsoft Media Foundation. Чтобы предотвратить случайное использование асинхронной таблицы MFT существующими приложениями, для этого атрибута необходимо задать ненулевое значение, прежде чем можно будет использовать асинхронную таблицу MFT. Конвейер Media Foundation автоматически задает атрибут, так что большинству приложений не требуется использовать этот атрибут. Однако если приложение использует асинхронную таблицу MFT вне Media Foundation конвейера, приложение должно установить этот атрибут.

Синхронный МФТС не требует этого атрибута.

Чтобы проверить, является ли MFT асинхронным, получите значение атрибута [MF \_ Transform \_ Async](mf-transform-async.md) в MFT.

## <a name="examples"></a>Примеры

Следующий код разблокирует асинхронную основную таблицу.


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
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
</dt> </dl>

 

 




