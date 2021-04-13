---
description: Указывает предпочтительную структуру устаревшего формата, используемую при преобразовании типа аудио Media.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Атрибут MF_MT_AUDIO_PREFER_WAVEFORMATEX (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544351"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>\_АУДИОРАЗЪЕМ MF \_ , \_ предпочтительный \_ атрибут вавеформатекс

Указывает предпочтительную структуру устаревшего формата, используемую при преобразовании типа аудио Media.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Этот атрибут предоставляет указание для функции [**мфкреатевавеформатексфроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) . Если атрибут имеет **значение true**, функция по возможности преобразует тип звукового носителя в структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , вместо того чтобы преобразовывать ее в структуру [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .

Функция [**мфинитмедиатипефромвавеформатекс**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) задает этот атрибут. Значение этого атрибута можно переопределить, но установка этого атрибута в **значение true** не гарантирует, что тип звукового носителя можно преобразовать в [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) форму.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

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

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 
