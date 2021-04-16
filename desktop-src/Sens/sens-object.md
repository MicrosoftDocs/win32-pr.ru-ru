---
description: Служба уведомлений о системных событиях (Сенс) определяет кокласс Сенс как часть библиотеки типов Сенс.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Объект Сенс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664211"
---
# <a name="sens-object"></a>Объект Сенс

Служба уведомлений о системных событиях (Сенс) определяет кокласс Сенс как часть библиотеки типов Сенс.

## <a name="implementation"></a>Реализация

Реализация объекта Сенс обеспечивается операционной системой.

## <a name="creationaccess-functions"></a>Функции создания и доступа



| Функция                                      | Описание                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Создает экземпляр объекта Сенс, используя его CLSID. |



 

## <a name="interfaces"></a>Интерфейсы



| Интерфейс                            | Описание                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**исенснетворк**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | По умолчанию. Исходящий интерфейс, реализованный объектом приемника в приложении подписчика.                   |
| [**исенсоннов**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Исходящий интерфейс, реализованный объектом приемника в приложении подписчика.                            |
| [**исенслогон**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Исходящий интерфейс, реализованный объектом приемника в приложении подписчика.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Исходящий интерфейс, реализованный объектом приемника в приложении подписчика. Доступно в Windows XP. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**исенслогон**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**исенснетворк**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**исенсоннов**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[О службе уведомлений о системных событиях](about-system-event-notification-service.md)
</dt> </dl>

 

 
