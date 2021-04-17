---
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении одного из указанных жестов.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Визуализация жестов (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693507"
---
# <a name="gesture-visualization"></a>Визуализация жестов

Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении одного из указанных жестов.

Эти константы используются с параметрами **SPI \_ Жетжестуревисуализатион** и **SPI \_ сетжестуревисуализатион** и функцией [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

**Примечание**  

Для получения или установки сведений о визуализации пера рекомендуется использовать параметры **SPI \_ Жетпенвисуализатион** и **SPI \_ сетпенвисуализатион** , а также константы, перечисленные в поле [**визуализация пера**](pen-visualization.md).

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Указывает, что обратная связь пользовательского интерфейса для всех жестов отключена.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Указывает, что для всех жестов включена обратная связь пользовательского интерфейса.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ коснуться**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Указывает отзыв пользовательского интерфейса для касания.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ даублетап**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Указывает отзыв пользовательского интерфейса для двойного касания.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ прессандтап**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Указывает отзыв пользовательского интерфейса для нажатия и касания.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ прессандхолд**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Указывает отзыв пользовательского интерфейса для нажатия и удерживания.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ ригхттап**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Указывает отзыв пользовательского интерфейса для правильного касания.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы конфигурации](configuration-constants.md)
</dt> <dt>

[**Связь с визуализацией**](contact-visualization.md)
</dt> <dt>

[**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Настройка обратной связи для ввода](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

