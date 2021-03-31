---
description: Флаги, используемые Ивикдевелоправнотификатионкаллбакк для указания, какие элементы были изменены.
ms.assetid: 4e94b4f4-abd9-4395-87ec-a08e49a2cf88
title: Константы Ивикдевелоправнотификатионкаллбакк (Винкодек. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8bf5d7cb2f4ac0e6fddd1f2e9151c95143b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999258"
---
# <a name="iwicdeveloprawnotificationcallback-constants"></a>Константы Ивикдевелоправнотификатионкаллбакк

Флаги, используемые [**ивикдевелоправнотификатионкаллбакк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) для указания, какие элементы были изменены.



| Константа/значение                                                                                                                                                                                                                                                                                                                                                                                            | Описание                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| <span id="WICRawChangeNotification_ExposureCompensation"></span><span id="wicrawchangenotification_exposurecompensation"></span><span id="WICRAWCHANGENOTIFICATION_EXPOSURECOMPENSATION"></span><dl> <dt>**Викравчанженотификатион \_ Експосурекомпенсатион**</dt> <dt>0x00000001</dt> </dl>             | Маска, используемая для сообщения об изменении компенсации экспозиции.<br/>                                                       |
| <span id="WICRawChangeNotification_NamedWhitePoint"></span><span id="wicrawchangenotification_namedwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_NAMEDWHITEPOINT"></span><dl> <dt>**Викравчанженотификатион \_ Намедвхитепоинт**</dt> <dt>0x00000002</dt> </dl>                                 | Маска, используемая для сообщения об изменении [**викнамедвхитепоинт**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint) .<br/>                 |
| <span id="WICRawChangeNotification_KelvinWhitePoint"></span><span id="wicrawchangenotification_kelvinwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_KELVINWHITEPOINT"></span><dl> <dt>**Викравчанженотификатион \_ Келвинвхитепоинт**</dt> <dt>0x00000004</dt> </dl>                             | Маска, используемая для сообщения об изменении белой точки в градусах Кельвина.<br/>                                                          |
| <span id="WICRawChangeNotification_RGBWhitePoint"></span><span id="wicrawchangenotification_rgbwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_RGBWHITEPOINT"></span><dl> <dt>**Викравчанженотификатион \_ Ргбвхитепоинт**</dt> <dt>0x00000008</dt> </dl>                                         | Маска, используемая для сообщения об изменении белого точки RGB.<br/>                                                             |
| <span id="WICRawChangeNotification_Contrast"></span><span id="wicrawchangenotification_contrast"></span><span id="WICRAWCHANGENOTIFICATION_CONTRAST"></span><dl> <dt>**Викравчанженотификатион \_ Контрастное отличие**</dt> <dt>0x00000010</dt> </dl>                                                             | Маска, используемая для сообщения об изменении контрастности.<br/>                                                                    |
| <span id="WICRawChangeNotification_Gamma"></span><span id="wicrawchangenotification_gamma"></span><span id="WICRAWCHANGENOTIFICATION_GAMMA"></span><dl> <dt>**Викравчанженотификатион \_ Гамма**</dt> - <dt>0x00000020</dt> </dl>                                                                         | Маска, используемая для передачи гамма-изменения.<br/>                                                                       |
| <span id="WICRawChangeNotification_Sharpness"></span><span id="wicrawchangenotification_sharpness"></span><span id="WICRAWCHANGENOTIFICATION_SHARPNESS"></span><dl> <dt>**Викравчанженотификатион \_ Резкость**</dt> <dt>0x00000040</dt> </dl>                                                         | Маска, используемая для сообщения об изменении четкости.<br/>                                                                   |
| <span id="WICRawChangeNotification_Saturation"></span><span id="wicrawchangenotification_saturation"></span><span id="WICRAWCHANGENOTIFICATION_SATURATION"></span><dl> <dt>**Викравчанженотификатион \_ 0x00000080 насыщенности**</dt> <dt></dt> </dl>                                                     | Маска, используемая для сообщения об изменении насыщенности.<br/>                                                                  |
| <span id="WICRawChangeNotification_Tint"></span><span id="wicrawchangenotification_tint"></span><span id="WICRAWCHANGENOTIFICATION_TINT"></span><dl> <dt>**Викравчанженотификатион \_ Оттенок**</dt> <dt>0x00000100</dt> </dl>                                                                             | Маска, используемая для сообщения об изменении оттенка.<br/>                                                                        |
| <span id="WICRawChangeNotification_NoiseReduction"></span><span id="wicrawchangenotification_noisereduction"></span><span id="WICRAWCHANGENOTIFICATION_NOISEREDUCTION"></span><dl> <dt>**Викравчанженотификатион \_ Ноисередуктион**</dt> <dt>0x00000200</dt> </dl>                                     | Маска, используемая для сообщения об изменении снижения шума.<br/>                                                             |
| <span id="WICRawChangeNotification_DestinationColorContext"></span><span id="wicrawchangenotification_destinationcolorcontext"></span><span id="WICRAWCHANGENOTIFICATION_DESTINATIONCOLORCONTEXT"></span><dl> <dt>**Викравчанженотификатион \_ Дестинатионколорконтекст**</dt> <dt>0x00000400</dt> </dl> | Маска, используемая для сообщения об изменении контекста целевого цвета.<br/>                                                   |
| <span id="WICRawChangeNotification_ToneCurve"></span><span id="wicrawchangenotification_tonecurve"></span><span id="WICRAWCHANGENOTIFICATION_TONECURVE"></span><dl> <dt>**Викравчанженотификатион \_ Тонекурве**</dt> <dt>0x00000800</dt> </dl>                                                         | Маска, используемая для сообщения об изменении кривой тона.<br/>                                                                  |
| <span id="WICRawChangeNotification_Rotation"></span><span id="wicrawchangenotification_rotation"></span><span id="WICRAWCHANGENOTIFICATION_ROTATION"></span><dl> <dt>**Викравчанженотификатион \_ Поворот**</dt> <dt>0x00001000</dt> </dl>                                                             | Маска, используемая для сообщения об изменении [**викравротатионкапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) .<br/> |
| <span id="WICRawChangeNotification_RenderMode"></span><span id="wicrawchangenotification_rendermode"></span><span id="WICRAWCHANGENOTIFICATION_RENDERMODE"></span><dl> <dt>**Викравчанженотификатион \_ RenderMode**</dt> <dt>0x00002000</dt> </dl>                                                     | Маска, используемая для сообщения об изменении [**викраврендермоде**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) .<br/>                     |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Винкодек. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивикдевелоправнотификатионкаллбакк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)
</dt> </dl>

 

 




