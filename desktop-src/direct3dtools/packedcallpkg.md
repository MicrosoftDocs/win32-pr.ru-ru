---
description: Представляет пакет из четырех вызовов.
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Паккедкаллпкг
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39be8828cf3ea0fbf773965db7272d566d43546b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626530"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span id="vspixengine.packedcallpkg"></span>Структура Паккедкаллпкг

Представляет пакет из четырех вызовов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a>Участники

**pcp1**  
Первый вызов в пакете.

**pcp2**  
Второй вызов в пакете.

**pcp3**  
Третий вызов в пакете.

**pcp4**  
Четвертый вызов в пакете.

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



