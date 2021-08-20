---
description: Указывает, включает ли загрузчик топологии перекодированный процессор видео (КСВП). для преобразований — Включение аппаратного ускоренного преобразования цвета.
title: Атрибут MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Мфидл. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: 3f315463ce1719617c5a48066401219f4b971f0a555cadf2af43b055a2b0e9a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875743"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>\_Топология MF \_ Включение \_ ксвп \_ для \_ атрибута воспроизведения

Указывает, включает ли загрузчик топологии перекодированный процессор видео (КСВП). для преобразований — Включение аппаратного ускоренного преобразования цвета.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Remarks

Если этот атрибут задан, загрузчик топологии будет запрашивать обработчик видео при необходимости во время разрешения топологии, отличной от перекодировки. При использовании топологии для создания собственного [имфтопологи](/windows/win32/api/mfidl/nn-mfidl-imftopology) этот атрибут указывает загрузчику использовать ксвп для преобразований вместо устаревшего цветового преобразователя, тем самым обеспечивая аппаратное преобразование цветов. устаревший цветовой конвертер — только программное обеспечение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[диспетчер устройств Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> </dl>

 

 




