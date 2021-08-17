---
title: Отмена
description: Большинство операций в ВВСАПИ могут быть отменены во время выполнения.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Отмена веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf75bd8d07d8f78ddf0a5750e6f4f96feb073dc15b8e63ed23ab8ceb061de145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841784"
---
# <a name="cancellation"></a>Отмена

Большинство операций в ВВСАПИ могут быть отменены во время выполнения.

Какая функция, используемая для отмены операции, зависит от затрагиваемого объекта.

| Функция                                           | Описание                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**всабортчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Отменяет все ожидающие входные и выходные данные в указанном канале и устанавливает состояние канала в состояние WS \_ канала с \_ \_ ошибкой. |
| [**всабортлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Отменяет все ожидающие входные и выходные данные для указанного прослушивателя.                                                          |
| [**всабортсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Отменяет все ожидающие входные и выходные данные для указанного прокси-сервера службы.                                                     |
| [**всабортсервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Прерывает и прекращает выполнение текущих операций на узле службы.                                                    |
| [**всабандонкалл**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Отменяет вызов, указанный вызов для указанного прокси-сервера службы.                                                        |



 

Сведения об отменах, влияющих на [операции службы на стороне сервера](server-side-service-operations.md) и обратные вызовы модели служб, см. в разделе [Отмена вызова](call-cancellation.md).


 

 




