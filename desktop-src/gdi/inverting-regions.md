---
description: Приложение инвертирует цвета, отображаемые в области, путем вызова функции Инвертргн.
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: Инвертирование регионов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e3c4b4d01f9ed8f09e819d59bf3268a1ccae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997343"
---
# <a name="inverting-regions"></a>Инвертирование регионов

Приложение инвертирует цвета, отображаемые в области, путем вызова функции [**инвертргн**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) . Для монохромных экранов **инвертргн** делает белые Пиксели черными и черными пикселами белым цветом. На цветовых экранах эта инверсия зависит от типа технологии, используемой для создания цветов на экране.

 

 



