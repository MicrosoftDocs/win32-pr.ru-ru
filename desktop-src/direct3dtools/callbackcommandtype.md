---
description: <span id="vspixengine.callbackcommandtype"></span>Перечисление Каллбакккоммандтипе — перечисление, используемое для обмена данными между ядром записи и узлом (например, Visual Studio диагностика графики).
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление Каллбакккоммандтипе
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85e1b7d396d125add00824e9b7c94086e0da6be2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090132"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span data-ttu-id="b48d4-103"><span id="vspixengine.callbackcommandtype"></span>Перечисление Каллбакккоммандтипе</span><span class="sxs-lookup"><span data-stu-id="b48d4-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType enumeration</span></span>

<span data-ttu-id="b48d4-104">Перечисление, используемое для обмена данными между подсистемой захвата и узлом (например, Visual Studio диагностика графики).</span><span class="sxs-lookup"><span data-stu-id="b48d4-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="b48d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b48d4-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="b48d4-106">Константы</span><span class="sxs-lookup"><span data-stu-id="b48d4-106">Constants</span></span>

<span data-ttu-id="b48d4-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**бегинкоммуникатионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b48d4-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span></span>  
<span data-ttu-id="b48d4-108">Результаты из Бегинкоммуникатион.</span><span class="sxs-lookup"><span data-stu-id="b48d4-108">Results from BeginCommunication.</span></span>

<span data-ttu-id="b48d4-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**еррорлисткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b48d4-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span></span>  
<span data-ttu-id="b48d4-110">Ошибки.</span><span class="sxs-lookup"><span data-stu-id="b48d4-110">Errors.</span></span>

<span data-ttu-id="b48d4-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**варнинглисткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b48d4-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span></span>  
<span data-ttu-id="b48d4-112">Предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b48d4-112">Warnings.</span></span>

<span data-ttu-id="b48d4-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**мессажескаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b48d4-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span></span>  
<span data-ttu-id="b48d4-114">Сообщения.</span><span class="sxs-lookup"><span data-stu-id="b48d4-114">Messages.</span></span>

<span data-ttu-id="b48d4-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**рунексперименткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b48d4-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span></span>  
<span data-ttu-id="b48d4-116">Результат из Рунексперимент.</span><span class="sxs-lookup"><span data-stu-id="b48d4-116">Result from RunExperiment.</span></span>

<span data-ttu-id="b48d4-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**рунактионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b48d4-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span></span>  
<span data-ttu-id="b48d4-118">Результат из Рунактион.</span><span class="sxs-lookup"><span data-stu-id="b48d4-118">Result from RunAction.</span></span>

<span data-ttu-id="b48d4-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**невфрамескаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b48d4-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span></span>  
<span data-ttu-id="b48d4-120">Значение, которое указывает обратный вызов, вызываемый при записи и готовности к отображению новых кадров.</span><span class="sxs-lookup"><span data-stu-id="b48d4-120">A value that indicates a callback to be called when new frames have been captured and ready to display.</span></span>

<span data-ttu-id="b48d4-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**бегинкоммуникатионкаллбакклегаци**</span><span class="sxs-lookup"><span data-stu-id="b48d4-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span></span>  
<span data-ttu-id="b48d4-122">Результаты из более старой версии Бегинкоммуникатион, используемой в Windows 7 и Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b48d4-122">Results from an older version of BeginCommunication used on Windows 7 and Windows 8.</span></span>

<span data-ttu-id="b48d4-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**рунекспериментстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b48d4-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span></span>  
<span data-ttu-id="b48d4-124">Результат из Рунекспериементпрогресс.</span><span class="sxs-lookup"><span data-stu-id="b48d4-124">Result from RunExperiementProgress.</span></span>

## <a name="requirements"></a><span data-ttu-id="b48d4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b48d4-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b48d4-126">Header</span><span class="sxs-lookup"><span data-stu-id="b48d4-126">Header</span></span></p></td><td><span data-ttu-id="b48d4-127">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="b48d4-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



