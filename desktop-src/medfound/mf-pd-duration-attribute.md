---
description: Указывает длительность презентации в единицах 100-наносекундных.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: Атрибут MF_PD_DURATION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712324"
---
# <a name="mf_pd_duration-attribute"></a>\_ \_ Атрибут DURATION для MF PD

Указывает длительность презентации в единицах 100-наносекундных.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="remarks"></a>Комментарии

Источники мультимедиа могут установить этот атрибут для дескриптора презентации, чтобы указать длительность презентации.

Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**. Однако атрибут не должен содержать отрицательное значение.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="examples"></a>Примеры

В следующем примере показано, как получить длительность презентации из источника мультимедиа.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> <dt>

[Дескрипторы представления](presentation-descriptors.md)
</dt> </dl>

 

 




