---
title: Расположение джойстика
description: Расположение джойстика
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- Джойстики, расположение
- Джойстики, кнопки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e5664166d20f9195a33d03534f792a4262b291bc3db34194fd05e06681563a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140309"
---
# <a name="joystick-position"></a>Расположение джойстика

Вы можете запросить в джойстике сведения о положении и кнопке с помощью функции [**жойжетпос**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Например, приложение может отправлять запросы к джойстику для значений расположения базовых показателей. Страница свойств панели управления джойстика использует этот метод при калибровке джойстика.

Вы также можете запросить джойстик или другое устройство с расширенными возможностями с помощью функции [**жойжетпосекс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

 

 