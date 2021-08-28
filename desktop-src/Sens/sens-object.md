---
description: Служба уведомлений о системных событиях (Сенс) определяет кокласс Сенс как часть библиотеки типов Сенс.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Объект Сенс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acdf70b5e2229051d569bd1f607ad8db5d3d567b4c0421464757f02bc6a8e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003952"
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
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Исходящий интерфейс, реализованный объектом приемника в приложении подписчика. доступно в Windows XP. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**исенслогон**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**исенснетворк**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**исенсоннов**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[О службе уведомлений о системных событиях](about-system-event-notification-service.md)
</dt> </dl>

 

 
