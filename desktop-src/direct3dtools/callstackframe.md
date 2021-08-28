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
ms.openlocfilehash: c6cb4b0e32213165149d7df8c7bf334049e37399
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631342"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>Структура Каллстаккфраме

Представляет сведения о кадре в стеке вызовов.

## <a name="syntax"></a>Синтаксис


```C++
} CallStackFrame;
```

## <a name="members"></a>Участники

**functionName**  
Строка COM, содержащая имя связанной функции.

**sourceFile**  
Строка COM, содержащая файл FilePath связанного исходного файла.

**moduleName**  
Строка COM, содержащая имя связанного модуля кода.

**lineNumber**  
Номер связанной строки.

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



