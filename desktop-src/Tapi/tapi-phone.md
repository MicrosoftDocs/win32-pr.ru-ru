---
description: Класс устройств TAPI/Phone состоит из всех телефонных устройств. Доступ к этим устройствам осуществляется с помощью телефонных функций TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI и телефон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b3238fb2e83d4f6e5e565f40b3ab3b124236ae2c89f879cb284d4a5997f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002722"
---
# <a name="tapiphone"></a>TAPI и телефон

Класс устройств TAPI/Phone состоит из всех телефонных устройств. Доступ к этим устройствам осуществляется с помощью телефонных функций TAPI.

Функция [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **ДВСТРИНГФОРМАТ** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

Член **двдевицеид** — это идентификатор телефонного устройства, связанного с телефонным маркером, заданным параметром [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).

Функция [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) также заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , настроив **двстрингформат** на STRINGFORMAT \_ binary и добавляя этот дополнительный элемент:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

Элемент **адвдевицеидс** — это массив, содержащий идентификаторы устройств всех телефонных устройств, связанных с данным устройством. Если нет связанных телефонных устройств, [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) ВОЗВРАЩАЕТ \_ значение линирр инвалдевицекласс.

 

 



