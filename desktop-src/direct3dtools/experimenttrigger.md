---
description: Представляет сведения о триггере эксперимента.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Експерименттригжер
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894565"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span data-ttu-id="90fa5-103"><span id="vspixengine.experimenttrigger"></span>Структура Експерименттригжер</span><span class="sxs-lookup"><span data-stu-id="90fa5-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger structure</span></span>

<span data-ttu-id="90fa5-104">Представляет сведения о триггере эксперимента.</span><span class="sxs-lookup"><span data-stu-id="90fa5-104">Represents experiment trigger information.</span></span>

## <a name="syntax"></a><span data-ttu-id="90fa5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90fa5-105">Syntax</span></span>


```C++
} ExperimentTrigger;
```

## <a name="members"></a><span data-ttu-id="90fa5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="90fa5-106">Members</span></span>

<span data-ttu-id="90fa5-107">**type**</span><span class="sxs-lookup"><span data-stu-id="90fa5-107">**type**</span></span>  
<span data-ttu-id="90fa5-108">Тип запуска эксперимента (захват).</span><span class="sxs-lookup"><span data-stu-id="90fa5-108">The kind of experiment (capture) triggered.</span></span>

<span data-ttu-id="90fa5-109">**key**</span><span class="sxs-lookup"><span data-stu-id="90fa5-109">**key**</span></span>  
<span data-ttu-id="90fa5-110">Если тип равен ЕКСПЕРИМЕНТТРИГЖЕРТИПЕ:: KEY, ключ, используемый для активации захвата.</span><span class="sxs-lookup"><span data-stu-id="90fa5-110">When type is equal to EXPERIMENTTRIGGERTYPE::KEY, the key used to trigger capture.</span></span>

<span data-ttu-id="90fa5-111">**фраменумбер**</span><span class="sxs-lookup"><span data-stu-id="90fa5-111">**frameNumber**</span></span>  
<span data-ttu-id="90fa5-112">Если тип равен ЕКСПЕРИМЕНТТРИГЖЕРТИПЕ:: ФРАМЕНУМБЕР, то номер кадра, который запустит захват.</span><span class="sxs-lookup"><span data-stu-id="90fa5-112">When type is equal to EXPERIMENTTRIGGERTYPE::FRAMENUMBER, the frame number that will trigger capture.</span></span>

<span data-ttu-id="90fa5-113">**каптурекаунт**</span><span class="sxs-lookup"><span data-stu-id="90fa5-113">**captureCount**</span></span>  
<span data-ttu-id="90fa5-114">Число последовательных кадров для записи.</span><span class="sxs-lookup"><span data-stu-id="90fa5-114">The number of sequential frames to capture.</span></span>

<span data-ttu-id="90fa5-115">**актиониид**</span><span class="sxs-lookup"><span data-stu-id="90fa5-115">**actionIID**</span></span>  
<span data-ttu-id="90fa5-116">Идентификатор события действия (снимок экрана, запись кадра и т. д.).</span><span class="sxs-lookup"><span data-stu-id="90fa5-116">The ID of the action event (screenshot, frame capture, etc).</span></span>

<span data-ttu-id="90fa5-117">**актионплайлоад**</span><span class="sxs-lookup"><span data-stu-id="90fa5-117">**actionPlayload**</span></span>  
<span data-ttu-id="90fa5-118">Указатель на полезные данные события действия.</span><span class="sxs-lookup"><span data-stu-id="90fa5-118">A pointer to the action event payload.</span></span>

## <a name="requirements"></a><span data-ttu-id="90fa5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="90fa5-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="90fa5-120">Header</span><span class="sxs-lookup"><span data-stu-id="90fa5-120">Header</span></span></p></td><td><span data-ttu-id="90fa5-121">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="90fa5-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



