---
description: Приложение инвертирует цвета, отображаемые в области, путем вызова функции Инвертргн.
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: Инвертирование регионов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1920b2bcc764bcc1c6e93c3a0c18bacf84a87e5bc2536d1bd503a0d47138166b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037862"
---
# <a name="inverting-regions"></a>Инвертирование регионов

Приложение инвертирует цвета, отображаемые в области, путем вызова функции [**инвертргн**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) . Для монохромных экранов **инвертргн** делает белые Пиксели черными и черными пикселами белым цветом. На цветовых экранах эта инверсия зависит от типа технологии, используемой для создания цветов на экране.

 

 



