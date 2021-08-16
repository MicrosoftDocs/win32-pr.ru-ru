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
ms.openlocfilehash: d4260c696834814f8ed42fc78154a506f3f156f3df37c02ccbff337c651f0ef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375371"
---
# <a name="capture-driver-capabilities"></a>Возможности записи драйверов

Вы можете получить аппаратные возможности подключенного к текущему драйверу записи с помощью сообщения о [**\_ \_ \_ получении \_ политик с ограничением WM**](wm-cap-driver-get-caps.md) (или макроса [**капдривержеткапс**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) ). Это сообщение возвращает возможности драйвера записи и базового оборудования в структуре [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

 

 




