---
description: Указывает, включает ли загрузчик топологии перекодированный процессор видео (КСВП). для преобразований — Включение аппаратного ускоренного преобразования цвета.
title: Атрибут MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Мфидл. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105720843"
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

## <a name="remarks"></a>Комментарии

Если этот атрибут задан, загрузчик топологии будет запрашивать обработчик видео при необходимости во время разрешения топологии, отличной от перекодировки. При использовании топологии для создания собственного [имфтопологи](/windows/win32/api/mfidl/nn-mfidl-imftopology) этот атрибут указывает загрузчику использовать ксвп для преобразований вместо устаревшего цветового преобразователя, тем самым обеспечивая аппаратное преобразование цветов. устаревший цветовой конвертер — только программное обеспечение.

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

[диспетчер устройств Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> </dl>

 

 




