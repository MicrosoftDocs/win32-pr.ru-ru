---
title: Что нового в Windows Vista
description: Версия 1,0 для управления цветом изображений (ICM) была предоставлена в Microsoft Windows 95 и предоставляет базовые возможности управления цветом в контекстах устройств Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Цветовая система Windows (WCS), Windows Vista
- WCS (цветовая система Windows), Windows Vista
- Управление цветом изображений, Windows Vista
- Управление цветом, Windows Vista
- цвета, Windows Vista
- Цветовая система Windows (WCS), операционные системы
- WCS (цветовая система Windows), операционные системы
- Управление цветом изображений, операционные системы
- Управление цветом, операционные системы
- цвета, операционные системы
- ICM (Image Color Management — управление цветом изображений)
- ICM (Управление цветом изображений)
- Управление цветом Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105719865"
---
# <a name="whats-new-in-windows-vista"></a>Что нового в Windows Vista

Версия 1,0 для управления цветом изображений (ICM) была предоставлена в Microsoft Windows 95 и предоставляет базовые возможности управления цветом в контекстах устройств Windows.

ICM версии 2,0 была предоставлена в Windows 98, Windows Millennium Edition, Windows 2000 и WindowsXP и включал ряд новых функций, реализующих управление цветом за пределами контекстов устройств. Эти новые функции подходят для более требовательных требований к управлению цветом, а приложения имеют больший контроль над процессом управления цветом.

С выпуском Windows Vista ICM 2,0 теперь включен в цветовую систему Windows (WCS) 1,0, что расширяет функциональность. В следующей таблице перечислены новые прикладные программные интерфейсы (API), поставляемые в составе Windows Vista.

## <a name="new-api-shipping-in-windows-vista"></a>Новая доставка API в Windows Vista



Перечисления

Имя API

Header

Библиотека

[**колордататипе**](/windows/win32/api/icm/ne-icm-colordatatype)

ICM. h

мскмс. lib

[**колорпрофилесубтипе**](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

ICM. h

мскмс. lib

[**колорпрофилетипе**](/windows/win32/api/icm/ne-icm-colorprofiletype)

ICM. h

мскмс. lib

[**\_область управления профилями WCS \_ \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

ICM. h

мскмс. lib



 



Функции

Имя API

Header

Библиотека

[**вксассоЦиатеколорпрофилевисдевице**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

мскмс. lib

[**вксчеккколорс**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

мскмс. lib

[**вкскреатеиккпрофиле**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

ICM. h

мскмс. lib

[**вксдисассоЦиатеколорпрофилефромдевице**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

ICM. h

мскмс. lib

[**вксенумколорпрофилес**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

ICM. h

мскмс. lib

[**вксенумколорпрофилессизе**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

ICM. h

мскмс. lib

[**вксжетдефаултколорпрофиле**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

ICM. h

мскмс. lib

[**вксжетдефаултколорпрофилесизе**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

ICM. h

мскмс. lib

[**вксжетдефаултрендерингинтент**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

мскмс. lib

[**вксжетусеперусерпрофилес**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

мскмс. lib

[**вксопенколорпрофилев**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

ICM. h

мскмс. lib

[**вкссетдефаултколорпрофиле**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

ICM. h

мскмс. lib

[**вкссетдефаултрендерингинтент**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

ICM. h

мскмс. lib

[**вкссетусеперусерпрофилес**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

ICM. h

мскмс. lib

[**вкстранслатеколорс**](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

ICM. h

мскмс. lib



 



Интерфейсы и их функции

Имя API

Header

Библиотека

[**идевицемоделплугин**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Колориметриктодевицеколорс**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Колориметриктодевицеколорсвисблакк**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

Вксплугин. h

Н/Д

[**Идевицемоделплугин::D Евицетоколориметрикколорс**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Жетгамутбаундаримеш**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Жетгамутбаундаримешсизе**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Жетнеутралаксис**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Жетнеутралаксиссизе**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Жетнумчаннелс**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Жетпримарисамплес**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

Вксплугин. h

Н/Д

[**Идевицемоделплугин:: Сеттрансформдевицемоделинфо**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

Вксплугин. h

Н/Д

[**игамутмапмоделплугин**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

Вксплугин. h

Н/Д

[**Игамутмапмоделплугин:: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

Вксплугин. h

Н/Д

[**Игамутмапмоделплугин:: Саурцетодестинатионаппеаранцеколорс**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

Вксплугин. h

Н/Д



 



Структуры

Имя API

Header

Библиотека

[**блаккинформатион**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

Вксплугин. h

Н/Д

[**гамутбаундаридескриптион**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

Вксплугин. h

Н/Д

[**ксизколорф**](https://www.bing.com/search?q=**XYZColorF**)

Вксплугин. h

Н/Д

[**жчколорф**](https://www.bing.com/search?q=**JChColorF**)

Вксплугин. h

Н/Д

[**жабколорф**](https://www.bing.com/search?q=**JabColorF**)

Вксплугин. h

Н/Д

[**гамутшелл**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

Вксплугин. h

Н/Д

[**гамутшеллтриангле**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

Вксплугин. h

Н/Д

[**примарижабколорс**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

Вксплугин. h

Н/Д

[**примариксизколорс**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

Вксплугин. h

Н/Д



 

 

 