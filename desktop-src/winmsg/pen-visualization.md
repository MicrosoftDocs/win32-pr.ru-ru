---
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении одного из перечисленных жестов пера.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Визуализация пера (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545575"
---
# <a name="pen-visualization"></a>Визуализация пера

Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении одного из перечисленных жестов пера.

Эти константы используются с параметрами **SPI \_ Жетпенвисуализатион** и **SPI \_ сетпенвисуализатион** и функцией [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**ПЕНВИСУАЛИЗАТИОН \_**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Указывает, что обратная связь пользовательского интерфейса для всех жестов пера отключена.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**ПЕНВИСУАЛИЗАТИОН \_**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Указывает, что для всех жестов пера включена обратная связь пользовательского интерфейса.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**ПЕНВИСУАЛИЗАТИОН \_ коснуться**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Указывает отзыв пользовательского интерфейса для касания пером.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**ПЕНВИСУАЛИЗАТИОН \_ даублетап**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Указывает отзыв пользовательского интерфейса для двойного касания пером.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**ПЕНВИСУАЛИЗАТИОН \_ курсор**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Указывает отзыв пользовательского интерфейса для курсора пера.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                 |
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

 

