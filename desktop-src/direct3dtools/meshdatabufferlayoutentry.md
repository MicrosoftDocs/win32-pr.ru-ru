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
ms.openlocfilehash: 44cc67402c69b690ba9070fa51bf8d26f316faa7d10ac991226db2c05b6d6a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282281"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>Структура Мешдатабуфферлайаутентри

Представляет сведения об отдельной записи в макете буфера сетки.

## <a name="syntax"></a>Синтаксис


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Члены

**pName**  
Строка COM, содержащая имя записи.

**нумкомпонентс**  
Количество однородных компонентов (значений), составляющих эту запись.

**Позиционирование**  
значение true, если запись является позицией; в противном случае — значение false.

**format**  
Формат данных записи (Register). Дополнительные сведения см. в разделе \_ перечисление форматов регистров.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



