---
title: Системмонитор Бровсекаунтерс, метод
description: Отображает диалоговое окно Добавление счетчиков.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Метод Бровсекаунтерс Сисмон
- Метод Бровсекаунтерс Сисмон, интерфейс Системмонитор
- Интерфейс Системмонитор Сисмон, метод Бровсекаунтерс
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071080"
---
# <a name="systemmonitorbrowsecounters-method"></a><span data-ttu-id="6ef5f-106">Метод Системмонитор:: Бровсекаунтерс</span><span class="sxs-lookup"><span data-stu-id="6ef5f-106">SystemMonitor::BrowseCounters method</span></span>

<span data-ttu-id="6ef5f-107">Отображает диалоговое окно **Добавление счетчиков** .</span><span class="sxs-lookup"><span data-stu-id="6ef5f-107">Displays the **Add Counters** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef5f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ef5f-108">Syntax</span></span>


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a><span data-ttu-id="6ef5f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ef5f-109">Parameters</span></span>

<span data-ttu-id="6ef5f-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6ef5f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ef5f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ef5f-111">Return value</span></span>

<span data-ttu-id="6ef5f-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6ef5f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef5f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ef5f-113">Remarks</span></span>

<span data-ttu-id="6ef5f-114">Это диалоговое окно позволяет пользователю выбрать локальные или удаленные счетчики производительности из списка объектов производительности.</span><span class="sxs-lookup"><span data-stu-id="6ef5f-114">This dialog box lets the user select local or remote performance counters from a list of performance objects.</span></span> <span data-ttu-id="6ef5f-115">Выбранные счетчики добавляются в коллекцию [**счетчиков**](counters.md) и отображаются в диаграмме или отчете.</span><span class="sxs-lookup"><span data-stu-id="6ef5f-115">The selected counters are added to the [**Counters**](counters.md) collection and displayed in the graph or report.</span></span>

<span data-ttu-id="6ef5f-116">Чтобы получить уведомление при добавлении счетчика, реализуйте событие [**онкаунтераддед**](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="6ef5f-116">To receive notification when a counter is added, implement the [**OnCounterAdded**](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef5f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6ef5f-117">Requirements</span></span>



| <span data-ttu-id="6ef5f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6ef5f-118">Requirement</span></span> | <span data-ttu-id="6ef5f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6ef5f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef5f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ef5f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef5f-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6ef5f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6ef5f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ef5f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef5f-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6ef5f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ef5f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6ef5f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ef5f-125"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6ef5f-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef5f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ef5f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef5f-127">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="6ef5f-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="6ef5f-128">**Счетчики. Добавить**</span><span class="sxs-lookup"><span data-stu-id="6ef5f-128">**Counters.Add**</span></span>](counters-add.md)
</dt> </dl>

 

 





