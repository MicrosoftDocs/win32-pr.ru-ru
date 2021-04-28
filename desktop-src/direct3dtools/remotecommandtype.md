---
description: <span id="vspixengine.remotecommandtype"></span>Перечисление Ремотекоммандтипе — перечисление, используемое для обмена данными между ядром записи и узлом (например, Visual Studio диагностика графики).
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
ms.openlocfilehash: ed57b9b044613351e99096a8c8cb741b8ad7a269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110511"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>Перечисление Ремотекоммандтипе

Перечисление, используемое для обмена данными между подсистемой захвата и узлом (например, Visual Studio диагностика графики).

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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



