---
description: Перечисление, используемое для обозначения этапов хода выполнения анализа кадров.
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление ОФФЛИНЕАНАЛИСИССТАЖЕ
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85D0288C-113A-4ABE-8EDB-ABB8F009956A
api_name:
- OFFLINEANALYSISSTAGE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf12b70acf70a654fe74b23d4bd3a196467797fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537181"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span data-ttu-id="1ae78-103"><span id="vspixengine.offlineanalysisstage"></span>Перечисление ОФФЛИНЕАНАЛИСИССТАЖЕ</span><span class="sxs-lookup"><span data-stu-id="1ae78-103"><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE enumeration</span></span>

<span data-ttu-id="1ae78-104">Перечисление, используемое для обозначения этапов хода выполнения анализа кадров.</span><span class="sxs-lookup"><span data-stu-id="1ae78-104">An enum used to indicate stages of progress in frame analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ae78-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="1ae78-106">Константы</span><span class="sxs-lookup"><span data-stu-id="1ae78-106">Constants</span></span>

<span data-ttu-id="1ae78-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**Оффлинеаналисисстаже \_ NotStarted**</span><span class="sxs-lookup"><span data-stu-id="1ae78-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage\_NotStarted**</span></span>  
<span data-ttu-id="1ae78-108">Анализ кадров еще не запущен.</span><span class="sxs-lookup"><span data-stu-id="1ae78-108">Frame analysis not yet started.</span></span>

<span data-ttu-id="1ae78-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**\_Инициализация оффлинеаналисисстаже**</span><span class="sxs-lookup"><span data-stu-id="1ae78-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage\_Initializing**</span></span>  
<span data-ttu-id="1ae78-110">Инициализация анализа кадров (запрос выдан).</span><span class="sxs-lookup"><span data-stu-id="1ae78-110">Frame analysis initializing (request issued).</span></span>

<span data-ttu-id="1ae78-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**Оффлинеаналисисстаже \_ инициализация \_ линкок**</span><span class="sxs-lookup"><span data-stu-id="1ae78-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage\_Initializing\_LinkOk**</span></span>  
<span data-ttu-id="1ae78-112">Инициализация анализа кадров (связь установлена).</span><span class="sxs-lookup"><span data-stu-id="1ae78-112">Frame analysis initializing (link established).</span></span>

<span data-ttu-id="1ae78-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**Оффлинеаналисисстаже \_ инициализация \_ манифесток**</span><span class="sxs-lookup"><span data-stu-id="1ae78-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage\_Initializing\_ManifestOk**</span></span>  
<span data-ttu-id="1ae78-114">Инициализация анализа кадров (манифест успешно проанализирован).</span><span class="sxs-lookup"><span data-stu-id="1ae78-114">Frame analysis initializing (manifest parsed successfully).</span></span>

<span data-ttu-id="1ae78-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**Оффлинеаналисисстаже \_ инициализация \_ тулок**</span><span class="sxs-lookup"><span data-stu-id="1ae78-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage\_Initializing\_ToolOk**</span></span>  
<span data-ttu-id="1ae78-116">Инициализация анализа кадров (Загрузка анализатора).</span><span class="sxs-lookup"><span data-stu-id="1ae78-116">Frame analysis initializing (analyzer loading).</span></span>

<span data-ttu-id="1ae78-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**\_Анализ оффлинеаналисисстаже**</span><span class="sxs-lookup"><span data-stu-id="1ae78-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage\_Analyzing**</span></span>  
<span data-ttu-id="1ae78-118">Анализ кадров работает.</span><span class="sxs-lookup"><span data-stu-id="1ae78-118">Frame analysis is running.</span></span>

<span data-ttu-id="1ae78-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**Оффлинеаналисисстаже \_ аналисискомплетед**</span><span class="sxs-lookup"><span data-stu-id="1ae78-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage\_AnalysisCompleted**</span></span>  
<span data-ttu-id="1ae78-120">Анализ кадров завершен (отправлено событие "завершено").</span><span class="sxs-lookup"><span data-stu-id="1ae78-120">Frame analysis completed ('complete' event sent).</span></span>

<span data-ttu-id="1ae78-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**Оффлинеаналисисстаже \_ аналисискомплетед \_ успешно**</span><span class="sxs-lookup"><span data-stu-id="1ae78-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage\_AnalysisCompleted\_Successful**</span></span>  
<span data-ttu-id="1ae78-122">Анализ кадров успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="1ae78-122">Frame analysis completed successfully.</span></span>

<span data-ttu-id="1ae78-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**Оффлинеаналисисстаже \_ аналисискомплетед \_ аутпутфиликсистс**</span><span class="sxs-lookup"><span data-stu-id="1ae78-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage\_AnalysisCompleted\_OutputFileExists**</span></span>  
<span data-ttu-id="1ae78-124">Анализ кадра завершен, и выходной файл существует.</span><span class="sxs-lookup"><span data-stu-id="1ae78-124">Frame analysis completed and output file exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae78-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1ae78-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1ae78-126">Header</span><span class="sxs-lookup"><span data-stu-id="1ae78-126">Header</span></span></p></td><td><span data-ttu-id="1ae78-127">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="1ae78-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



