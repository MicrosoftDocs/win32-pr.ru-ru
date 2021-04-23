---
description: Перечисление, используемое для обмена данными между подсистемой захвата и узлом (например, Visual Studio диагностика графики).
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
ms.openlocfilehash: 63b94ace0818e2057a87c0f3962bb3967843bcfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072296"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span data-ttu-id="2e1ab-103"><span id="vspixengine.remotecommandtype"></span>Перечисление Ремотекоммандтипе</span><span class="sxs-lookup"><span data-stu-id="2e1ab-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType enumeration</span></span>

<span data-ttu-id="2e1ab-104">Перечисление, используемое для обмена данными между подсистемой захвата и узлом (например, Visual Studio диагностика графики).</span><span class="sxs-lookup"><span data-stu-id="2e1ab-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e1ab-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="2e1ab-106">Константы</span><span class="sxs-lookup"><span data-stu-id="2e1ab-106">Constants</span></span>

<span data-ttu-id="2e1ab-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**бегинкоммуникатион**</span><span class="sxs-lookup"><span data-stu-id="2e1ab-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span></span>  
<span data-ttu-id="2e1ab-108">Начинает обмен данными.</span><span class="sxs-lookup"><span data-stu-id="2e1ab-108">Starts communication.</span></span>

<span data-ttu-id="2e1ab-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**рунексперимент**</span><span class="sxs-lookup"><span data-stu-id="2e1ab-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span></span>  
<span data-ttu-id="2e1ab-110">Запускает диагностика графики сеанс записи (эксперимент).</span><span class="sxs-lookup"><span data-stu-id="2e1ab-110">Starts a Graphics Diagnostics capture session (an experiment).</span></span>

<span data-ttu-id="2e1ab-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**рунактион**</span><span class="sxs-lookup"><span data-stu-id="2e1ab-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span></span>  
<span data-ttu-id="2e1ab-112">Запускает захват (то же, что и экран печати).</span><span class="sxs-lookup"><span data-stu-id="2e1ab-112">Starts a capture (same as hitting print screen).</span></span> <span data-ttu-id="2e1ab-113">Отправляется узлом при захвате кадра.</span><span class="sxs-lookup"><span data-stu-id="2e1ab-113">Sent by a host when capturing a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1ab-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2e1ab-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2e1ab-115">Header</span><span class="sxs-lookup"><span data-stu-id="2e1ab-115">Header</span></span></p></td><td><span data-ttu-id="2e1ab-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="2e1ab-116">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



