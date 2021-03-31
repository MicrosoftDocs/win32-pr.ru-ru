---
title: Ирдвтаскплугин StartTask, метод
description: Вызывается для запуска задачи обновления на виртуальной машине.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода StartTask
- Службы удаленных рабочих столов метода StartTask, интерфейс Ирдвтаскплугин
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугин, метод StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491319"
---
# <a name="irdvtaskpluginstarttask-method"></a><span data-ttu-id="f20e9-106">Метод Ирдвтаскплугин:: StartTask</span><span class="sxs-lookup"><span data-stu-id="f20e9-106">IRDVTaskPlugin::StartTask method</span></span>

<span data-ttu-id="f20e9-107">Вызывается для запуска задачи обновления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f20e9-107">Called to start the update task on the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f20e9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f20e9-108">Syntax</span></span>


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a><span data-ttu-id="f20e9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f20e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f20e9-110">*Метка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f20e9-110">*Label* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20e9-111">Метка для задачи.</span><span class="sxs-lookup"><span data-stu-id="f20e9-111">The label for the task.</span></span> <span data-ttu-id="f20e9-112">Это метка, которая была передана агенту триггера в методе [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="f20e9-112">This is the label that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f20e9-113">*Идентификатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f20e9-113">*Identifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20e9-114">Идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="f20e9-114">The identifier of the task.</span></span> <span data-ttu-id="f20e9-115">Это идентификатор, который был передан агенту триггера в методе [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="f20e9-115">This is the identifier that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f20e9-116">*Контекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f20e9-116">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20e9-117">Необязательные данные для задачи.</span><span class="sxs-lookup"><span data-stu-id="f20e9-117">Optional data for the task.</span></span> <span data-ttu-id="f20e9-118">Это данные, переданные в агент триггера в методе [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="f20e9-118">This is the data that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f20e9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f20e9-119">Return value</span></span>

<span data-ttu-id="f20e9-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f20e9-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f20e9-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f20e9-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f20e9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f20e9-122">Requirements</span></span>



| <span data-ttu-id="f20e9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f20e9-123">Requirement</span></span> | <span data-ttu-id="f20e9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f20e9-124">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="f20e9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f20e9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f20e9-126">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="f20e9-126">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="f20e9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f20e9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f20e9-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f20e9-128">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f20e9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f20e9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f20e9-130">**ирдвтаскплугин**</span><span class="sxs-lookup"><span data-stu-id="f20e9-130">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





