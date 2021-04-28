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
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span data-ttu-id="1000b-103"><span id="vspixengine.remotecommandtype"></span>Перечисление Ремотекоммандтипе</span><span class="sxs-lookup"><span data-stu-id="1000b-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType enumeration</span></span>

<span data-ttu-id="1000b-104">Перечисление, используемое для обмена данными между подсистемой захвата и узлом (например, Visual Studio диагностика графики).</span><span class="sxs-lookup"><span data-stu-id="1000b-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="1000b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1000b-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="1000b-106">Константы</span><span class="sxs-lookup"><span data-stu-id="1000b-106">Constants</span></span>

<span data-ttu-id="1000b-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**бегинкоммуникатион**</span><span class="sxs-lookup"><span data-stu-id="1000b-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span></span>  
<span data-ttu-id="1000b-108">Начинает обмен данными.</span><span class="sxs-lookup"><span data-stu-id="1000b-108">Starts communication.</span></span>

<span data-ttu-id="1000b-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**рунексперимент**</span><span class="sxs-lookup"><span data-stu-id="1000b-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span></span>  
<span data-ttu-id="1000b-110">Запускает диагностика графики сеанс записи (эксперимент).</span><span class="sxs-lookup"><span data-stu-id="1000b-110">Starts a Graphics Diagnostics capture session (an experiment).</span></span>

<span data-ttu-id="1000b-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**рунактион**</span><span class="sxs-lookup"><span data-stu-id="1000b-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span></span>  
<span data-ttu-id="1000b-112">Запускает захват (то же, что и экран печати).</span><span class="sxs-lookup"><span data-stu-id="1000b-112">Starts a capture (same as hitting print screen).</span></span> <span data-ttu-id="1000b-113">Отправляется узлом при захвате кадра.</span><span class="sxs-lookup"><span data-stu-id="1000b-113">Sent by a host when capturing a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="1000b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1000b-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1000b-115">Header</span><span class="sxs-lookup"><span data-stu-id="1000b-115">Header</span></span></p></td><td><span data-ttu-id="1000b-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="1000b-116">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



