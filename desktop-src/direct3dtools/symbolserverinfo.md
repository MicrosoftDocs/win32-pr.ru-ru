---
description: Представляет сведения о сервере символов отладки.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Симболсерверинфо
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139755"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>Структура Симболсерверинфо

Представляет сведения о сервере символов отладки.

## <a name="syntax"></a>Синтаксис


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Члены

**symbolPath**  
Строка COM, содержащая путь к серверу символов.

**симболкачедир**  
Строка COM, содержащая каталог кэша сервера символов.

**публиксимболсервернаме**  
Строка COM, содержащая открытое имя сервера символов.

**симболексклуделист**  
Строка COM, указывающая список исключаемых символов.

**симболинклуделист**  
Строка COM, указывающая список включаемых символов.

**усиксклуделист**  
значение true, если список исключений игнорируется; в противном случае — значение false.

**усемссимболсервер**  
значение true, если используется сервер символов Майкрософт; в противном случае — значение false.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



