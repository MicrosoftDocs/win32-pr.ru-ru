---
description: Представляет стадию конвейера, включая сведения об используемом шейдере.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Пипелинестаже
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990062"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>Структура Пипелинестаже

Представляет стадию конвейера, включая сведения об используемом шейдере.

## <a name="syntax"></a>Синтаксис


```C++
} PipeLineStage;
```

## <a name="members"></a>Члены

**стажеид**  
Идентификатор этапа конвейера.

**Отлаживаемых**  
значение true, если этап конвейера поддерживает отладку; в противном случае — значение false.

**StageName**  
Строка COM, содержащая имя этапа конвейера.

**гуарантидаутпут**  
значение true, если на этапе конвейера всегда есть выходные данные конвейера; в противном случае — значение false.

**дебужентрипоинт**  
Строка COM, содержащая имя точки входа шейдера, если таковая имеется.

**шадерфиле**  
Строка COM, содержащая путь к файлу исходного кода шейдера.

**шадербитестреамптр**  
ФИЛЕПТР для потока байтов шейдера. Это значение передается обратно для отладки.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



