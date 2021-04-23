---
title: Интерфейс Имсрдпинпутсинк
description: Приемник входных данных удаленного рабочего стола.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпинпутсинк
- Службы удаленных рабочих столов интерфейса Имсрдпинпутсинк, описание
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988403"
---
# <a name="imsrdpinputsink-interface"></a><span data-ttu-id="ebd93-105">Интерфейс Имсрдпинпутсинк</span><span class="sxs-lookup"><span data-stu-id="ebd93-105">IMsRdpInputSink interface</span></span>

<span data-ttu-id="ebd93-106">Приемник входных данных удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ebd93-106">Remote desktop input sink.</span></span>

## <a name="members"></a><span data-ttu-id="ebd93-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="ebd93-107">Members</span></span>

<span data-ttu-id="ebd93-108">Интерфейс **имсрдпинпутсинк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ebd93-108">The **IMsRdpInputSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ebd93-109">**Имсрдпинпутсинк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ebd93-109">**IMsRdpInputSink** also has these types of members:</span></span>

-   [<span data-ttu-id="ebd93-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ebd93-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ebd93-111">Методы</span><span class="sxs-lookup"><span data-stu-id="ebd93-111">Methods</span></span>

<span data-ttu-id="ebd93-112">Интерфейс **имсрдпинпутсинк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ebd93-112">The **IMsRdpInputSink** interface has these methods.</span></span>



| <span data-ttu-id="ebd93-113">Метод</span><span class="sxs-lookup"><span data-stu-id="ebd93-113">Method</span></span>                                                               | <span data-ttu-id="ebd93-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ebd93-114">Description</span></span>                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| <span data-ttu-id="ebd93-115">[**аддтаучинпут**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebd93-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span></span>               | <span data-ttu-id="ebd93-116">Добавляет сенсорный ввод.</span><span class="sxs-lookup"><span data-stu-id="ebd93-116">Adds touch input.</span></span><br/>         |
| <span data-ttu-id="ebd93-117">[**бегинтаучфраме**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebd93-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span></span>           | <span data-ttu-id="ebd93-118">Начало рамки касания.</span><span class="sxs-lookup"><span data-stu-id="ebd93-118">Begin touch frame.</span></span><br/>        |
| <span data-ttu-id="ebd93-119">[**ендтаучфраме**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebd93-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span></span>               | <span data-ttu-id="ebd93-120">Конечный кадр касания.</span><span class="sxs-lookup"><span data-stu-id="ebd93-120">End touch frame.</span></span><br/>          |
| <span data-ttu-id="ebd93-121">[**сендкэйбоардевент**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebd93-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span></span>       | <span data-ttu-id="ebd93-122">Отправляет событие клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ebd93-122">Sends keyboard event.</span></span><br/>     |
| <span data-ttu-id="ebd93-123">[**сендмаусебуттоневент**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebd93-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span></span> | <span data-ttu-id="ebd93-124">Отправляет событие кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="ebd93-124">Sends mouse button event.</span></span><br/> |
| <span data-ttu-id="ebd93-125">[**сендмаусемовивент**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebd93-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span></span>     | <span data-ttu-id="ebd93-126">Отправляет событие перемещения указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="ebd93-126">Sends mouse move event.</span></span><br/>   |
| <span data-ttu-id="ebd93-127">[**сендмаусевхилевент**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebd93-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span></span>   | <span data-ttu-id="ebd93-128">Отправляет событие колесика мыши.</span><span class="sxs-lookup"><span data-stu-id="ebd93-128">Sends mouse wheel event.</span></span><br/>  |
| <span data-ttu-id="ebd93-129">[**сендсинцевент**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebd93-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span></span>               | <span data-ttu-id="ebd93-130">Отправляет событие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ebd93-130">Sends sync event.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="ebd93-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ebd93-131">Requirements</span></span>



| <span data-ttu-id="ebd93-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ebd93-132">Requirement</span></span> | <span data-ttu-id="ebd93-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ebd93-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd93-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebd93-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd93-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ebd93-135">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="ebd93-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebd93-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd93-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ebd93-137">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="ebd93-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ebd93-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebd93-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd93-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebd93-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd93-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd93-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd93-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebd93-142">IID</span><span class="sxs-lookup"><span data-stu-id="ebd93-142">IID</span></span><br/>                      | <span data-ttu-id="ebd93-143">IID \_ имсрдпинпутсинк определен как 4606850E-76A7-4E28-A47E-C7174F619351</span><span class="sxs-lookup"><span data-stu-id="ebd93-143">IID\_IMsRdpInputSink is defined as 4606850E-76A7-4E28-A47E-C7174F619351</span></span><br/>     |



 

