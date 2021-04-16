---
description: Предлагаемые последовательности действий для базовой таблицы Инсталуисекуенце в базе данных установщик Windows.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: Предложенные Инсталлуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650847"
---
# <a name="suggested-installuisequence"></a><span data-ttu-id="5c698-103">Предложенные Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="5c698-103">Suggested InstallUISequence</span></span>



| <span data-ttu-id="5c698-104">Действие</span><span class="sxs-lookup"><span data-stu-id="5c698-104">Action</span></span>                                          | <span data-ttu-id="5c698-105">Условие</span><span class="sxs-lookup"><span data-stu-id="5c698-105">Condition</span></span>                                                                                                  | <span data-ttu-id="5c698-106">Последовательность</span><span class="sxs-lookup"><span data-stu-id="5c698-106">Sequence</span></span> |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="5c698-107">фаталеррордлг</span><span class="sxs-lookup"><span data-stu-id="5c698-107">FatalErrorDlg</span></span>                                   |                                                                                                            | <span data-ttu-id="5c698-108">–3</span><span class="sxs-lookup"><span data-stu-id="5c698-108">-3</span></span>       |
| <span data-ttu-id="5c698-109">усерекситдлг</span><span class="sxs-lookup"><span data-stu-id="5c698-109">UserExitDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="5c698-110">-2</span><span class="sxs-lookup"><span data-stu-id="5c698-110">-2</span></span>       |
| <span data-ttu-id="5c698-111">екситдлг</span><span class="sxs-lookup"><span data-stu-id="5c698-111">ExitDlg</span></span>                                         |                                                                                                            | <span data-ttu-id="5c698-112">-1</span><span class="sxs-lookup"><span data-stu-id="5c698-112">-1</span></span>       |
| [<span data-ttu-id="5c698-113">лаунчкондитионс</span><span class="sxs-lookup"><span data-stu-id="5c698-113">LaunchConditions</span></span>](launchconditions-action.md) |                                                                                                            | <span data-ttu-id="5c698-114">100</span><span class="sxs-lookup"><span data-stu-id="5c698-114">100</span></span>      |
| <span data-ttu-id="5c698-115">препаредлг</span><span class="sxs-lookup"><span data-stu-id="5c698-115">PrepareDlg</span></span>                                      |                                                                                                            | <span data-ttu-id="5c698-116">140</span><span class="sxs-lookup"><span data-stu-id="5c698-116">140</span></span>      |
| [<span data-ttu-id="5c698-117">аппсеарч</span><span class="sxs-lookup"><span data-stu-id="5c698-117">AppSearch</span></span>](appsearch-action.md)               |                                                                                                            | <span data-ttu-id="5c698-118">400</span><span class="sxs-lookup"><span data-stu-id="5c698-118">400</span></span>      |
| [<span data-ttu-id="5c698-119">ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="5c698-119">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="5c698-120">НЕ [ **установлено**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="5c698-120">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="5c698-121">500</span><span class="sxs-lookup"><span data-stu-id="5c698-121">500</span></span>      |
| [<span data-ttu-id="5c698-122">рмккпсеарч</span><span class="sxs-lookup"><span data-stu-id="5c698-122">RMCCPSearch</span></span>](rmccpsearch-action.md)           | <span data-ttu-id="5c698-123">НЕ [ **установлено**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="5c698-123">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="5c698-124">600</span><span class="sxs-lookup"><span data-stu-id="5c698-124">600</span></span>      |
| [<span data-ttu-id="5c698-125">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="5c698-125">CostInitialize</span></span>](costinitialize-action.md)     |                                                                                                            | <span data-ttu-id="5c698-126">800</span><span class="sxs-lookup"><span data-stu-id="5c698-126">800</span></span>      |
| [<span data-ttu-id="5c698-127">филекост</span><span class="sxs-lookup"><span data-stu-id="5c698-127">FileCost</span></span>](filecost-action.md)                 |                                                                                                            | <span data-ttu-id="5c698-128">900</span><span class="sxs-lookup"><span data-stu-id="5c698-128">900</span></span>      |
| [<span data-ttu-id="5c698-129">костфинализе</span><span class="sxs-lookup"><span data-stu-id="5c698-129">CostFinalize</span></span>](costfinalize-action.md)         |                                                                                                            | <span data-ttu-id="5c698-130">1000</span><span class="sxs-lookup"><span data-stu-id="5c698-130">1000</span></span>     |
| <span data-ttu-id="5c698-131">велкомедлг</span><span class="sxs-lookup"><span data-stu-id="5c698-131">WelcomeDlg</span></span>                                      | <span data-ttu-id="5c698-132">НЕ [ **установлено**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="5c698-132">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="5c698-133">1230</span><span class="sxs-lookup"><span data-stu-id="5c698-133">1230</span></span>     |
| <span data-ttu-id="5c698-134">ресумедлг</span><span class="sxs-lookup"><span data-stu-id="5c698-134">ResumeDlg</span></span>                                       | <span data-ttu-id="5c698-135">[**Установлено**](installed.md) И ( [**возобновить**](resume.md) или [**выбрать**](preselected.md))</span><span class="sxs-lookup"><span data-stu-id="5c698-135">[**Installed**](installed.md) AND ( [**RESUME**](resume.md) OR [**Preselected**](preselected.md))</span></span>       | <span data-ttu-id="5c698-136">1240</span><span class="sxs-lookup"><span data-stu-id="5c698-136">1240</span></span>     |
| <span data-ttu-id="5c698-137">маинтенанцевелкомедлг</span><span class="sxs-lookup"><span data-stu-id="5c698-137">MaintenanceWelcomeDlg</span></span>                           | <span data-ttu-id="5c698-138">[**Установлено**](installed.md) И не [**возобновлять**](resume.md) и не [**выделять**](preselected.md)</span><span class="sxs-lookup"><span data-stu-id="5c698-138">[**Installed**](installed.md) AND NOT [**RESUME**](resume.md) AND NOT [**Preselected**](preselected.md)</span></span> | <span data-ttu-id="5c698-139">1250</span><span class="sxs-lookup"><span data-stu-id="5c698-139">1250</span></span>     |
| <span data-ttu-id="5c698-140">прогрессдлг</span><span class="sxs-lookup"><span data-stu-id="5c698-140">ProgressDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="5c698-141">1280</span><span class="sxs-lookup"><span data-stu-id="5c698-141">1280</span></span>     |
| [<span data-ttu-id="5c698-142">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="5c698-142">ExecuteAction</span></span>](executeaction-action.md)       |                                                                                                            | <span data-ttu-id="5c698-143">1300</span><span class="sxs-lookup"><span data-stu-id="5c698-143">1300</span></span>     |



 

 

 



