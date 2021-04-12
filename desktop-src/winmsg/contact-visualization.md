---
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении входного контакта.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Визуализация контакта (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348192"
---
# <a name="contact-visualization"></a>Связь с визуализацией

Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении входного контакта.

Эти константы используются с параметрами **SPI \_ Жетконтактвисуализатион** и **SPI \_ сетконтактвисуализатион** и функцией [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**КОНТАКТВИСУАЛИЗАТИОН \_**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Указывает, что отзывы о пользовательском интерфейсе для всех контактов отключены.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**КОНТАКТВИСУАЛИЗАТИОН \_**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Указывает Отзывы о пользовательском интерфейсе для всех контактов.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**КОНТАКТВИСУАЛИЗАТИОН \_ пресентатионмоде**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Указывает Отзывы о пользовательском интерфейсе для всех контактов с визуальными элементами режима представления.


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

[**Визуализация жестов**](gesture-visualization.md)
</dt> <dt>

[**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Настройка обратной связи для ввода](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

