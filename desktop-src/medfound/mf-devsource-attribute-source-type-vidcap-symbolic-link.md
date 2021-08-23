---
description: Содержит символьную ссылку для драйвера видеозаписи.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd3b69899eb9df1973cb13611a822139ffda0e744c84137ff9d6094ed4a962d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104950"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>\_ДЕВСАУРЦЕ MF \_ \_ тип источника \_ атрибута \_ видкап \_ символьный \_ атрибут ссылки

Содержит символьную ссылку для драйвера видеозаписи.

## <a name="data-type"></a>Тип данных

**WCHAR\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Remarks

Используйте этот атрибут в качестве входных данных для функции [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

Кроме того, этот атрибут задается для объектов активации, возвращаемых следующими функциями:

-   [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Символьная ссылка должна рассматриваться как непрозрачная строка. Отображаемое понятное имя устройства содержится в атрибуте [ \_ \_ \_ понятного \_ имени атрибута MF девсаурце](mf-devsource-attribute-friendly-name.md) .

\_ \_ \_ Атрибут девсаурце типа источника атрибута MF \_ \_ видкап \_ \_ может быть передан в качестве значения аргумента DevicePath функции [**сетупдиопендевицеинтерфаце**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Захват аудио- и видеоданных](audio-video-capture.md)
</dt> <dt>

[Запись атрибутов устройства](capture-device-attributes.md)
</dt> </dl>

 

 
