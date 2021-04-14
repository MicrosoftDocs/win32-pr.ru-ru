---
title: Системмонитор. Монитордупликатеинстанцес, свойство
description: Возвращает или задает значение, которое определяет, можно ли отслеживать несколько экземпляров счетчика.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Сисмон свойство Монитордупликатеинстанцес
- Монитордупликатеинстанцес Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Монитордупликатеинстанцес
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415329"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a><span data-ttu-id="ad275-106">Системмонитор. Монитордупликатеинстанцес, свойство</span><span class="sxs-lookup"><span data-stu-id="ad275-106">SystemMonitor.MonitorDuplicateInstances property</span></span>

<span data-ttu-id="ad275-107">Возвращает или задает значение, которое определяет, можно ли отслеживать несколько экземпляров счетчика.</span><span class="sxs-lookup"><span data-stu-id="ad275-107">Retrieves or sets a value that determines whether multiple instances of a counter can be monitored.</span></span>

<span data-ttu-id="ad275-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ad275-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad275-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad275-109">Syntax</span></span>


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ad275-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ad275-110">Property value</span></span>

<span data-ttu-id="ad275-111">Значение true указывает, что можно отслеживать несколько экземпляров счетчика (значение по умолчанию — true).</span><span class="sxs-lookup"><span data-stu-id="ad275-111">True indicates that multiple instances of a counter can be monitored (True is the default).</span></span> <span data-ttu-id="ad275-112">Значение false указывает, что можно отслеживать только один экземпляр счетчика.</span><span class="sxs-lookup"><span data-stu-id="ad275-112">False indicates that only one instance of a counter can be monitored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad275-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad275-113">Remarks</span></span>

<span data-ttu-id="ad275-114">Системный монитор добавляет \# n к каждому имени экземпляра, кроме первого, если существует несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="ad275-114">System Monitor appends \#n to every instance name, except the first, if multiple instances exist.</span></span> <span data-ttu-id="ad275-115">Серийный номер n начинается с единицы и увеличивается на единицу для каждого нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad275-115">The serial number, n, begins with one and is incremented by one for each new instance.</span></span> <span data-ttu-id="ad275-116">Например, если указать " \\ процесс ( \* ) \\ % загруженности процессора", коллекция счетчиков должна содержать несколько экземпляров svchost.</span><span class="sxs-lookup"><span data-stu-id="ad275-116">For example, if you specify "\\Process(\*)\\% Processor Time", the counter collection should contain multiple instances of svchost.</span></span> <span data-ttu-id="ad275-117">Первое вхождение — svchost, далее — svchost \# 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="ad275-117">The first occurrence will be svchost, the next occurrence will be svchost\#1, and so on.</span></span>

<span data-ttu-id="ad275-118">Отслеживание повторяющихся экземпляров выполняется только в том случае, если в качестве имени экземпляра используется подстановочный знак ( \* ).</span><span class="sxs-lookup"><span data-stu-id="ad275-118">Duplicate instances are monitored only if you use the wildcard character (\*) for the instance name.</span></span> <span data-ttu-id="ad275-119">Если указано " \\ Process (SVCHOST) \\ % загруженности процессора", то отслеживается только первый экземпляр svchost, а не все экземпляры svchost.</span><span class="sxs-lookup"><span data-stu-id="ad275-119">If you specified "\\Process(svchost)\\% Processor Time" only the first instance found of svchost is monitored, not all instances of svchost.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad275-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ad275-120">Requirements</span></span>



| <span data-ttu-id="ad275-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ad275-121">Requirement</span></span> | <span data-ttu-id="ad275-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ad275-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad275-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad275-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ad275-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad275-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ad275-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad275-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ad275-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad275-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad275-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ad275-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad275-128"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ad275-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad275-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad275-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad275-130">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="ad275-130">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





