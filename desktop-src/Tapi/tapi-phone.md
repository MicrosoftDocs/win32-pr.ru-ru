---
description: Класс устройств TAPI/Phone состоит из всех телефонных устройств. Доступ к этим устройствам осуществляется с помощью телефонных функций TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI и телефон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998990"
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

 

 



