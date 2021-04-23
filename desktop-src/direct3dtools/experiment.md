---
description: Представляет сведения о эксперименте (захвате).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура эксперимента
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805981"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span data-ttu-id="79fde-103"><span id="vspixengine.experiment"></span>Структура эксперимента</span><span class="sxs-lookup"><span data-stu-id="79fde-103"><span id="vspixengine.experiment"></span>Experiment structure</span></span>

<span data-ttu-id="79fde-104">Представляет сведения о эксперименте (захвате).</span><span class="sxs-lookup"><span data-stu-id="79fde-104">Represents information about an experiment (capture).</span></span>

## <a name="syntax"></a><span data-ttu-id="79fde-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79fde-105">Syntax</span></span>


```C++
} Experiment;
```

## <a name="members"></a><span data-ttu-id="79fde-106">Члены</span><span class="sxs-lookup"><span data-stu-id="79fde-106">Members</span></span>

<span data-ttu-id="79fde-107">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="79fde-107">**processId**</span></span>  
<span data-ttu-id="79fde-108">Идентификатор связанного процесса.</span><span class="sxs-lookup"><span data-stu-id="79fde-108">The associated process ID.</span></span>

<span data-ttu-id="79fde-109">**applicationName**</span><span class="sxs-lookup"><span data-stu-id="79fde-109">**applicationName**</span></span>  
<span data-ttu-id="79fde-110">Строка COM, содержащая имя приложения для запуска эксперимента.</span><span class="sxs-lookup"><span data-stu-id="79fde-110">A COM string containing the name of the application to run the experiment on.</span></span>

<span data-ttu-id="79fde-111">**коммандлинеаргументс**</span><span class="sxs-lookup"><span data-stu-id="79fde-111">**commandLineArguments**</span></span>  
<span data-ttu-id="79fde-112">Строка COM, содержащая аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="79fde-112">A COM string containing the command line arguments.</span></span>

<span data-ttu-id="79fde-113">**workingDirectory**</span><span class="sxs-lookup"><span data-stu-id="79fde-113">**workingDirectory**</span></span>  
<span data-ttu-id="79fde-114">Строка COM, содержащая путь к рабочему каталогу.</span><span class="sxs-lookup"><span data-stu-id="79fde-114">A COM string containing the path of the working directory.</span></span>

<span data-ttu-id="79fde-115">**темппиксрунфиле**</span><span class="sxs-lookup"><span data-stu-id="79fde-115">**tempPixRunFile**</span></span>  
<span data-ttu-id="79fde-116">Строка COM, содержащая путь к временному файлу, используемому для выполнения эксперимента.</span><span class="sxs-lookup"><span data-stu-id="79fde-116">A COM string containing the filepath of the temporary file used to perform the experiment.</span></span>

<span data-ttu-id="79fde-117">**стартоптион**</span><span class="sxs-lookup"><span data-stu-id="79fde-117">**startOption**</span></span>  
<span data-ttu-id="79fde-118">Параметр запуска, связанный с экспериментом.</span><span class="sxs-lookup"><span data-stu-id="79fde-118">The start option associated with the experiment.</span></span>

<span data-ttu-id="79fde-119">**експерименттипе**</span><span class="sxs-lookup"><span data-stu-id="79fde-119">**experimentType**</span></span>  
<span data-ttu-id="79fde-120">Тип эксперимента (захват).</span><span class="sxs-lookup"><span data-stu-id="79fde-120">The kind of experiment (capture).</span></span>

<span data-ttu-id="79fde-121">**уилокале**</span><span class="sxs-lookup"><span data-stu-id="79fde-121">**uiLocale**</span></span>  
<span data-ttu-id="79fde-122">Идентификатор локали, используемый для элементов наложения пользовательского интерфейса во время експериемент (записи).</span><span class="sxs-lookup"><span data-stu-id="79fde-122">The ID of the locale used for UI overlay elements during the experiement (capture).</span></span> <span data-ttu-id="79fde-123">Это передается из узла (например, Visual Studio диагностика графики) в подсистему записи.</span><span class="sxs-lookup"><span data-stu-id="79fde-123">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

<span data-ttu-id="79fde-124">**регистрирут**</span><span class="sxs-lookup"><span data-stu-id="79fde-124">**registryRoot**</span></span>  
<span data-ttu-id="79fde-125">Строка COM, содержащая корень реестра.</span><span class="sxs-lookup"><span data-stu-id="79fde-125">A COM string containing the registry root.</span></span> <span data-ttu-id="79fde-126">Это передается из узла (например, Visual Studio диагностика графики) в подсистему записи.</span><span class="sxs-lookup"><span data-stu-id="79fde-126">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="79fde-127">Требования</span><span class="sxs-lookup"><span data-stu-id="79fde-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="79fde-128">Header</span><span class="sxs-lookup"><span data-stu-id="79fde-128">Header</span></span></p></td><td><span data-ttu-id="79fde-129">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="79fde-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



