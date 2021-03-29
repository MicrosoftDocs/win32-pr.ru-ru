---
description: Указывает, является ли источник видеозаписи аппаратным устройством или программным устройством.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647237"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a>\_ \_ Тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ \_ атрибут источника оборудования

Указывает, является ли источник видеозаписи аппаратным устройством или программным устройством.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Если значение равно **true**, источником захвата является аппаратное устройство. Если значение равно **false**, это программное устройство. Значение по умолчанию — **false**.

Этот атрибут задается для объектов активации, возвращаемых следующими функциями:

-   [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Атрибут применяется только к устройствам записи видео.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Захват аудио- и видеоданных](audio-video-capture.md)
</dt> <dt>

[Запись атрибутов устройства](capture-device-attributes.md)
</dt> </dl>

 

 




