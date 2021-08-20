---
description: Указывает роль устройства для устройства записи звука.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe0aecb12a7831218fceb3c480c6c4e2a20a1ffa330675a642feefc14ecbe39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060747"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a>\_ \_ \_ \_ \_ Атрибут роли АУДКАП для типа источника \_ атрибута MF девсаурце

Указывает роль устройства для устройства записи звука.

## <a name="data-type"></a>Тип данных

**Ероле** хранится как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

Тип перечисления **ероле** описан в основной документации по API аудио.

Значение атрибута указывает роль устройства. Этот атрибут используется со следующими функциями.

Этот атрибут может использоваться в качестве входных данных для функций [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) и [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Если атрибут указан, функция создает источник мультимедиа, использующий устройство записи звука по умолчанию для указанной роли устройства.

Этот атрибут можно также использовать в качестве входных данных для функции [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Если атрибут указан, перечисление ограничивается указанной ролью устройства. Кроме того, каждый объект активации, возвращаемый функцией **мфенумдевицесаурцес** , содержит этот атрибут. Атрибут затем используется объектом активации для внутренних целей при создании источника мультимедиа.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Захват аудио- и видеоданных](audio-video-capture.md)
</dt> <dt>

[Запись атрибутов устройства](capture-device-attributes.md)
</dt> </dl>

 

 




