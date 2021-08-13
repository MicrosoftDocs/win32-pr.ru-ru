---
description: Объект службы
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Объект службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587ca25e1e9fc225a0b555263bf3f3f4e725c83e5f9b01e716fd6fa191fc270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445591"
---
# <a name="service-object"></a>Объект службы

Объект службы должен поддерживать следующие свойства.



| Имя свойства                                                                                                                      | Обязательный или необязательный                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_идентификатор объекта \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Обязательный. .                                                                           |
| [\_ \_ идентификатор родительского объекта \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Обязательный.                                                                             |
| [\_имя объекта \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Обязательный.                                                                             |
| [\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Обязательный.                                                                             |
| [\_объект WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Требуется, если объект службы не должен отображаться для пользователя.                       |
| [\_система объектов \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Требуется, если объект является системным объектом (например, он представляет системный файл). |
| [\_Категория функционального \_ объекта WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Обязательный. Представляет тип службы устройства, например Контакты службы.          |
| [\_версия службы \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Обязательный.                                                                             |
| [\_тип хранилища \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Требуется, если служба используется для хранения объектов.                                     |
| [\_емкость хранилища \_ WPD](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Требуется, если служба используется для хранения объектов.                                     |



 

## <a name="typical-resources"></a>Типичные ресурсы

Обычно эти объекты не размещают ресурсы.

## <a name="typical-formats"></a>Стандартные форматы

В следующем списке приведены типичные форматы, используемые объектом службы. Однако этот объект не ограничен этими форматами.

-   \_Формат объекта WPD не \_ \_ указан

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Требования к объектам**](requirements-for-objects.md)
</dt> </dl>

 

 
