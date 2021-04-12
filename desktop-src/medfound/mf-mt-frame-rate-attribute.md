---
description: Частота кадров типа видеоклипа в кадрах в секунду.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: Атрибут MF_MT_FRAME_RATE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423990"
---
# <a name="mf_mt_frame_rate-attribute"></a>\_ \_ Атрибут частоты кадров MF MT \_

Частота кадров типа видеоклипа в кадрах в секунду.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Комментарии

Частота кадров выражается в виде коэффициента. Верхний 32 бит значения атрибута содержит числитель, а младшие 32 бита содержат знаменатель. Например, если частота кадров составляет 30 кадров в секунду (кадров/с), то соотношение составляет 30/1. Если частота кадров составляет 29,97 кадров/с, то коэффициент равен 30000/1001.

Чтобы задать значение, используйте функцию [**мфсетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Чтобы получить значение, используйте функцию [**мфжетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="examples"></a>Примеры

В следующем примере задается частота кадров для типа видеоклипа.


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



В следующем примере показано получение частоты кадров из типа видеоклипа.


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[**мфаверажетимеперфраметофрамерате**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[**мффрамератетоаверажетимеперфраме**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




