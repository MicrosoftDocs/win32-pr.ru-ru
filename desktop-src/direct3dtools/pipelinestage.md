---
description: Представляет стадию конвейера, включая сведения об используемом шейдере.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Пипелинестаже
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990062"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span data-ttu-id="72c29-103"><span id="vspixengine.pipelinestage"></span>Структура Пипелинестаже</span><span class="sxs-lookup"><span data-stu-id="72c29-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage structure</span></span>

<span data-ttu-id="72c29-104">Представляет стадию конвейера, включая сведения об используемом шейдере.</span><span class="sxs-lookup"><span data-stu-id="72c29-104">Represents a pipeline stage, including details of the shader used.</span></span>

## <a name="syntax"></a><span data-ttu-id="72c29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72c29-105">Syntax</span></span>


```C++
} PipeLineStage;
```

## <a name="members"></a><span data-ttu-id="72c29-106">Члены</span><span class="sxs-lookup"><span data-stu-id="72c29-106">Members</span></span>

<span data-ttu-id="72c29-107">**стажеид**</span><span class="sxs-lookup"><span data-stu-id="72c29-107">**StageId**</span></span>  
<span data-ttu-id="72c29-108">Идентификатор этапа конвейера.</span><span class="sxs-lookup"><span data-stu-id="72c29-108">The ID of the pipeline stage.</span></span>

<span data-ttu-id="72c29-109">**Отлаживаемых**</span><span class="sxs-lookup"><span data-stu-id="72c29-109">**Debuggable**</span></span>  
<span data-ttu-id="72c29-110">значение true, если этап конвейера поддерживает отладку; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="72c29-110">true if the pipeline stage supports debugging; otherwise, false.</span></span>

<span data-ttu-id="72c29-111">**StageName**</span><span class="sxs-lookup"><span data-stu-id="72c29-111">**StageName**</span></span>  
<span data-ttu-id="72c29-112">Строка COM, содержащая имя этапа конвейера.</span><span class="sxs-lookup"><span data-stu-id="72c29-112">A COM string containing the name of the pipeline stage.</span></span>

<span data-ttu-id="72c29-113">**гуарантидаутпут**</span><span class="sxs-lookup"><span data-stu-id="72c29-113">**GuaranteedOutput**</span></span>  
<span data-ttu-id="72c29-114">значение true, если на этапе конвейера всегда есть выходные данные конвейера; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="72c29-114">true if the pipeline stage always has pipeline output; otherwise, false.</span></span>

<span data-ttu-id="72c29-115">**дебужентрипоинт**</span><span class="sxs-lookup"><span data-stu-id="72c29-115">**DebugEntryPoint**</span></span>  
<span data-ttu-id="72c29-116">Строка COM, содержащая имя точки входа шейдера, если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="72c29-116">A COM string containing the name of the shader entry point, if there is one.</span></span>

<span data-ttu-id="72c29-117">**шадерфиле**</span><span class="sxs-lookup"><span data-stu-id="72c29-117">**ShaderFile**</span></span>  
<span data-ttu-id="72c29-118">Строка COM, содержащая путь к файлу исходного кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="72c29-118">A COM string containing the filepath of the shader source file.</span></span>

<span data-ttu-id="72c29-119">**шадербитестреамптр**</span><span class="sxs-lookup"><span data-stu-id="72c29-119">**ShaderByteStreamPtr**</span></span>  
<span data-ttu-id="72c29-120">ФИЛЕПТР для потока байтов шейдера.</span><span class="sxs-lookup"><span data-stu-id="72c29-120">A FILEPTR for the shader byte stream.</span></span> <span data-ttu-id="72c29-121">Это значение передается обратно для отладки.</span><span class="sxs-lookup"><span data-stu-id="72c29-121">This is passed back in order to debug.</span></span>

## <a name="requirements"></a><span data-ttu-id="72c29-122">Требования</span><span class="sxs-lookup"><span data-stu-id="72c29-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="72c29-123">Header</span><span class="sxs-lookup"><span data-stu-id="72c29-123">Header</span></span></p></td><td><span data-ttu-id="72c29-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="72c29-124">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



