---
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении входного контакта.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Визуализация контакта (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea196017b1731bb176cd21a7dc02aaa360f4fe70503bd204b9c488d38eff99ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437257"
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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                 |
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

 

