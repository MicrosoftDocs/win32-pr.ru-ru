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
ms.openlocfilehash: 10f1d1780404303109a72fe1a12023bc35b2c0ca
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625170"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>Структура Пипелинестаже

Представляет стадию конвейера, включая сведения об используемом шейдере.

## <a name="syntax"></a>Синтаксис


```C++
} PipeLineStage;
```

## <a name="members"></a>Участники

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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



