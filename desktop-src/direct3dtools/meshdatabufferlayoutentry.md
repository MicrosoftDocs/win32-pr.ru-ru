---
description: Представляет сведения об отдельной записи в макете буфера сетки.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Мешдатабуфферлайаутентри
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 40360e73f480b4c12dcb24311c26fd9718093705
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625360"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>Структура Мешдатабуфферлайаутентри

Представляет сведения об отдельной записи в макете буфера сетки.

## <a name="syntax"></a>Синтаксис


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Участники

**pName**  
Строка COM, содержащая имя записи.

**нумкомпонентс**  
Количество однородных компонентов (значений), составляющих эту запись.

**Позиционирование**  
значение true, если запись является позицией; в противном случае — значение false.

**format**  
Формат данных записи (Register). Дополнительные сведения см. в разделе \_ перечисление форматов регистров.

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



