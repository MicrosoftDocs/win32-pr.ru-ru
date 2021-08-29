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
ms.openlocfilehash: ecf25b450b613f433704de976d25fcbb77af8c7a586547fb99954a5cc86171e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119398"
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

 

 



