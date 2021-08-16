---
description: Класс устройств TAPI/Line состоит из всех устройств линии. Доступ к этим устройствам осуществляется с помощью функций линии TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/Line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56478f43d1055d7bf2a382bc84611360675da97e506812a1806df4beca0aeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760736"
---
# <a name="tapiline"></a>TAPI/Line

Класс устройств TAPI/Line состоит из всех устройств линии. Доступ к этим устройствам осуществляется с помощью функций линии TAPI.

Функция [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **ДВСТРИНГФОРМАТ** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

Элемент **двдевицеид** — это идентификатор устройства линии, связанного с маркером линии, заданным параметром [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

Функция [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) также заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , настроив **двстрингформат** на STRINGFORMAT \_ binary и добавляя этот дополнительный элемент:

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

Элемент **адвдевицеидс** — это массив, содержащий идентификаторы устройств всех устройств линий, связанных с телефонным устройством. Если связанных устройств нет, [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) ВОЗВРАЩАЕТ \_ значение фонирр инвалдевицекласс.

 

 



