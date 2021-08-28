---
description: <span id="vspixengine.remotecommandtype"></span>перечисление ремотекоммандтипе — перечисление, используемое для обмена данными между ядром записи и узлом (например, Visual Studio диагностика графики).
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление Ремотекоммандтипе
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 73accd6f73a7c33219c83a3285837d2e1c7c133a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631722"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>Перечисление Ремотекоммандтипе

перечисление, используемое для обмена данными между подсистемой захвата и узлом (например, Visual Studio диагностика графики).

## <a name="syntax"></a>Синтаксис


```C++
};
```

## <a name="constants"></a>Константы

<span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**бегинкоммуникатион**  
Начинает обмен данными.

<span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**рунексперимент**  
Запускает диагностика графики сеанс записи (эксперимент).

<span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**рунактион**  
Запускает захват (то же, что и экран печати). Отправляется узлом при захвате кадра.

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



