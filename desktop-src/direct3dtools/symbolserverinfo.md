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
ms.openlocfilehash: 28f85445e6affc006c5c0898df1c85d71693a66d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632092"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>Структура Симболсерверинфо

Представляет сведения о сервере символов отладки.

## <a name="syntax"></a>Синтаксис


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Участники

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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



