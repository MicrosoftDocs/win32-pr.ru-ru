---
title: Возможности записи драйверов
description: Возможности записи драйверов
ms.assetid: 6e74635e-9dac-419d-a264-08fee04ae7b7
keywords:
- Сообщение WM_CAP_DRIVER_GET_CAPS
- макрос Капдривержеткапс
- Структура КАПДРИВЕРКАПС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87fb4f9cb439229721b6c10aa6207af601f9ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067574"
---
# <a name="capture-driver-capabilities"></a>Возможности записи драйверов

Вы можете получить аппаратные возможности подключенного к текущему драйверу записи с помощью сообщения о [**\_ \_ \_ получении \_ политик с ограничением WM**](wm-cap-driver-get-caps.md) (или макроса [**капдривержеткапс**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) ). Это сообщение возвращает возможности драйвера записи и базового оборудования в структуре [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

 

 




