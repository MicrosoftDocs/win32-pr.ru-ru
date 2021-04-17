---
description: Представляет сведения о кадре в стеке вызовов.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Каллстаккфраме
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691980"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>Структура Каллстаккфраме

Представляет сведения о кадре в стеке вызовов.

## <a name="syntax"></a>Синтаксис


```C++
} CallStackFrame;
```

## <a name="members"></a>Члены

**functionName**  
Строка COM, содержащая имя связанной функции.

**sourceFile**  
Строка COM, содержащая файл FilePath связанного исходного файла.

**moduleName**  
Строка COM, содержащая имя связанного модуля кода.

**lineNumber**  
Номер связанной строки.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



