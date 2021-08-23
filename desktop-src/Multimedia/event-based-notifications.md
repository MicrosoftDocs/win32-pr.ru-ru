---
title: Уведомления Event-Based
description: Уведомления Event-Based
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- Джойстики, уведомления
- Джойстики, сообщения
- Джойстики, уведомления на основе событий
- Джойстики, пороговое значение перемещения
- уведомления джойстика на основе событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b50e973434d5f5706c92a22f76846ada150bfc7caf3f5ba88c3f385f7eaf84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526184"
---
# <a name="event-based-notifications"></a>Уведомления Event-Based

Можно попросить систему отправить джойстику сообщения в приложение каждый раз, когда расположение джойстика изменится на значение, превышающее *порог перемещения* устройства. Пороговое значение перемещения — это расстояние, на которое джойстик необходимо переместить, прежде чем сообщение об изменении расположения джойстика будет отправлено в окно, в котором было захвачено устройство. Дополнительные сведения см. в [**разделе \_ mm JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)или [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).

Пороговое значение изначально равно нулю. Порог перемещения можно задать с помощью функции [**жойсетсрешолд**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) . Минимальную частоту опроса джойстика можно получить с помощью функции [**жойжетдевкапс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .

 

 