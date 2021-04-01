---
title: Расположение джойстика
description: Расположение джойстика
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- Джойстики, расположение
- Джойстики, кнопки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcdc187cfba244bb2b8c28c37e3677593f99870
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260776"
---
# <a name="joystick-position"></a>Расположение джойстика

Вы можете запросить в джойстике сведения о положении и кнопке с помощью функции [**жойжетпос**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Например, приложение может отправлять запросы к джойстику для значений расположения базовых показателей. Страница свойств панели управления джойстика использует этот метод при калибровке джойстика.

Вы также можете запросить джойстик или другое устройство с расширенными возможностями с помощью функции [**жойжетпосекс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

 

 