---
description: Представляет сведения о триггере эксперимента.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Експерименттригжер
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894565"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span id="vspixengine.experimenttrigger"></span>Структура Експерименттригжер

Представляет сведения о триггере эксперимента.

## <a name="syntax"></a>Синтаксис


```C++
} ExperimentTrigger;
```

## <a name="members"></a>Члены

**type**  
Тип запуска эксперимента (захват).

**key**  
Если тип равен ЕКСПЕРИМЕНТТРИГЖЕРТИПЕ:: KEY, ключ, используемый для активации захвата.

**фраменумбер**  
Если тип равен ЕКСПЕРИМЕНТТРИГЖЕРТИПЕ:: ФРАМЕНУМБЕР, то номер кадра, который запустит захват.

**каптурекаунт**  
Число последовательных кадров для записи.

**актиониид**  
Идентификатор события действия (снимок экрана, запись кадра и т. д.).

**актионплайлоад**  
Указатель на полезные данные события действия.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



