---
description: Указывает предпочтительную структуру устаревшего формата, используемую при преобразовании типа аудио Media.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Атрибут MF_MT_AUDIO_PREFER_WAVEFORMATEX (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23e2aeb00e2967b3f031a2aafe3a01f3846d7db077ba344a59680508bd385fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035302"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>\_АУДИОРАЗЪЕМ MF \_ , \_ предпочтительный \_ атрибут вавеформатекс

Указывает предпочтительную структуру устаревшего формата, используемую при преобразовании типа аудио Media.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Этот атрибут предоставляет указание для функции [**мфкреатевавеформатексфроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) . Если атрибут имеет **значение true**, функция по возможности преобразует тип звукового носителя в структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , вместо того чтобы преобразовывать ее в структуру [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .

Функция [**мфинитмедиатипефромвавеформатекс**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) задает этот атрибут. Значение этого атрибута можно переопределить, но установка этого атрибута в **значение true** не гарантирует, что тип звукового носителя можно преобразовать в [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) форму.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 
