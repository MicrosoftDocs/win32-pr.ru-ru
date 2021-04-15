---
title: SystemMonitor.Batметод Чинглокк
description: Блокирует системный монитор, чтобы предотвратить выборку данных счетчиков из вновь добавленного файла счетчика или журнала.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Метод Батчинглокк Сисмон
- Метод Батчинглокк Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, метод Батчинглокк
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661927"
---
# <a name="systemmonitorbatchinglock-method"></a><span data-ttu-id="0dcdc-106">SystemMonitor.Batметод Чинглокк</span><span class="sxs-lookup"><span data-stu-id="0dcdc-106">SystemMonitor.BatchingLock method</span></span>

<span data-ttu-id="0dcdc-107">Блокирует системный монитор, чтобы предотвратить выборку данных счетчиков из вновь добавленного файла счетчика или журнала.</span><span class="sxs-lookup"><span data-stu-id="0dcdc-107">Locks the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dcdc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dcdc-108">Syntax</span></span>


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a><span data-ttu-id="0dcdc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dcdc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dcdc-110">*Блокировка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0dcdc-110">*lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dcdc-111">Задайте значение true, чтобы заблокировать системный монитор, чтобы предотвратить выборку данных счетчиков из вновь добавленного файла счетчика или журнала.</span><span class="sxs-lookup"><span data-stu-id="0dcdc-111">Set to True to lock the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span> <span data-ttu-id="0dcdc-112">Установите значение false, чтобы снять блокировку.</span><span class="sxs-lookup"><span data-stu-id="0dcdc-112">Set to False to remove the lock.</span></span>

</dd> <dt>

<span data-ttu-id="0dcdc-113">*батчреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0dcdc-113">*batchReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dcdc-114">Определяет источник данных, которые вы блокируете.</span><span class="sxs-lookup"><span data-stu-id="0dcdc-114">Identifies the source of the data that you are locking.</span></span> <span data-ttu-id="0dcdc-115">Используйте одно и то же значение причины при блокировке и разблокировке ресурса.</span><span class="sxs-lookup"><span data-stu-id="0dcdc-115">Use the same reason value when locking and unlocking the resource.</span></span> <span data-ttu-id="0dcdc-116">Возможные значения см. в разделе Перечисление [**сисмонбатчреасон**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .</span><span class="sxs-lookup"><span data-stu-id="0dcdc-116">For possible values, see the [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dcdc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dcdc-117">Return value</span></span>

<span data-ttu-id="0dcdc-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0dcdc-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dcdc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0dcdc-119">Remarks</span></span>

<span data-ttu-id="0dcdc-120">Этот метод необходимо вызывать дважды, один раз, чтобы заблокировать источник (true) и один раз для разблокировки источника (false).</span><span class="sxs-lookup"><span data-stu-id="0dcdc-120">You must call this method twice, once to lock the source (True) and once to unlock the source (False).</span></span>

<span data-ttu-id="0dcdc-121">Можно поместить только одну блокировку.</span><span class="sxs-lookup"><span data-stu-id="0dcdc-121">You can place only one lock.</span></span> <span data-ttu-id="0dcdc-122">Например, если установить блокировку для Сисмонбатчаддфилес, а затем выполнить второй вызов с использованием Сисмонбатчаддкаунтерс в качестве причины, второй вызов удаляет блокировку, помещенную первым вызовом.</span><span class="sxs-lookup"><span data-stu-id="0dcdc-122">For example, if you set the lock for SysmonBatchAddFiles and then make a second call using SysmonBatchAddCounters as the reason, the second call removes the lock placed by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dcdc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0dcdc-123">Requirements</span></span>



| <span data-ttu-id="0dcdc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0dcdc-124">Requirement</span></span> | <span data-ttu-id="0dcdc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0dcdc-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0dcdc-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0dcdc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0dcdc-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0dcdc-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0dcdc-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0dcdc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0dcdc-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0dcdc-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0dcdc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0dcdc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dcdc-131"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="0dcdc-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dcdc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0dcdc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dcdc-133">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="0dcdc-133">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





