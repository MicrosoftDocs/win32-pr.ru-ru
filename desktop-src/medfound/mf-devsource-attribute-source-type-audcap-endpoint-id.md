---
description: Указывает идентификатор конечной точки для устройства записи звука.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6baafd2aa1bdfc3f4959b877963faff5df9aabe57c672555edb98f4cded8b1ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113954"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>\_ \_ Тип источника атрибута MF девсаурце \_ \_ \_ \_ атрибут идентификатора конечной точки аудкап \_

Указывает идентификатор конечной точки для устройства записи звука.

## <a name="data-type"></a>Тип данных

**WCHAR\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Remarks

Значением атрибута является идентификатор конечной точки. Этот атрибут используется со следующими функциями:

-   Его можно использовать в качестве входных данных для функций [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) и [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . В этом контексте атрибут указывает устройство аудиозаписи для функции. Идентификатор конечной точки для данного устройства можно получить, вызвав метод [**иммдевице:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) . Дополнительные сведения см. в документации по API аудио.
-   Когда функция [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) перечисляет звуковые устройства, возвращаемые объекты активации содержат этот атрибут. Атрибут используется внутренне объектом активации при создании источника мультимедиа.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Захват аудио- и видеоданных](audio-video-capture.md)
</dt> <dt>

[Запись атрибутов устройства](capture-device-attributes.md)
</dt> </dl>

 

 
