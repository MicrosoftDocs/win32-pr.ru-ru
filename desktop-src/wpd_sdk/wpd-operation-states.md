---
description: Операция WPD \_ \_ указывает, что значения перечисления описывают текущее состояние выполняемой операции.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Перечисление WPD_OPERATION_STATES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698826"
---
# <a name="wpd_operation_states-enumeration"></a><span data-ttu-id="08fa0-103">\_ \_ Перечисление состояний операций WPD</span><span class="sxs-lookup"><span data-stu-id="08fa0-103">WPD\_OPERATION\_STATES enumeration</span></span>

<span data-ttu-id="08fa0-104">**Операция WPD \_ \_ указывает** , что значения перечисления описывают текущее состояние выполняемой операции.</span><span class="sxs-lookup"><span data-stu-id="08fa0-104">The **WPD\_OPERATION\_STATES** enumeration values describe the current state of an operation in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="08fa0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08fa0-105">Syntax</span></span>


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a><span data-ttu-id="08fa0-106">Константы</span><span class="sxs-lookup"><span data-stu-id="08fa0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="08fa0-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**\_состояние операции WPD не \_ \_ указано**</span><span class="sxs-lookup"><span data-stu-id="08fa0-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**WPD\_OPERATION\_STATE\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="08fa0-108">Текущая операция находится в неопределенном состоянии (не задано) и неизвестно.</span><span class="sxs-lookup"><span data-stu-id="08fa0-108">The current operation is in an unspecified state (not set) and unknown.</span></span>

</dd> <dt>

<span data-ttu-id="08fa0-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**\_состояние операции \_ WPD \_ запущено**</span><span class="sxs-lookup"><span data-stu-id="08fa0-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD\_OPERATION\_STATE\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="08fa0-110">Операция запущена.</span><span class="sxs-lookup"><span data-stu-id="08fa0-110">The operation is started.</span></span>

</dd> <dt>

<span data-ttu-id="08fa0-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**\_выполняется операция \_ с состоянием "WPD" \_**</span><span class="sxs-lookup"><span data-stu-id="08fa0-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD\_OPERATION\_STATE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="08fa0-112">Операция выполняется.</span><span class="sxs-lookup"><span data-stu-id="08fa0-112">The operation is running.</span></span>

</dd> <dt>

<span data-ttu-id="08fa0-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**\_состояние операции \_ WPD \_ приостановлено**</span><span class="sxs-lookup"><span data-stu-id="08fa0-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD\_OPERATION\_STATE\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="08fa0-114">Операция приостановлена.</span><span class="sxs-lookup"><span data-stu-id="08fa0-114">The operation is paused.</span></span>

</dd> <dt>

<span data-ttu-id="08fa0-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**\_состояние операции \_ WPD \_ отменено**</span><span class="sxs-lookup"><span data-stu-id="08fa0-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD\_OPERATION\_STATE\_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="08fa0-116">Операция отменена.</span><span class="sxs-lookup"><span data-stu-id="08fa0-116">The operation is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="08fa0-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**\_состояние операции \_ WPD \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="08fa0-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD\_OPERATION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="08fa0-118">Операция завершена.</span><span class="sxs-lookup"><span data-stu-id="08fa0-118">The operation is finished.</span></span>

</dd> <dt>

<span data-ttu-id="08fa0-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**\_состояние операции \_ WPD \_ прервано**</span><span class="sxs-lookup"><span data-stu-id="08fa0-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD\_OPERATION\_STATE\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="08fa0-120">Операция прервана.</span><span class="sxs-lookup"><span data-stu-id="08fa0-120">The operation is aborted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08fa0-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08fa0-121">Remarks</span></span>

<span data-ttu-id="08fa0-122">Эти значения принимаются в определяемом приложением обратном вызове ([**ипортабледевицеевенткаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span><span class="sxs-lookup"><span data-stu-id="08fa0-122">These values are received in the application-defined callback ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span></span>

## <a name="requirements"></a><span data-ttu-id="08fa0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="08fa0-123">Requirements</span></span>



| <span data-ttu-id="08fa0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="08fa0-124">Requirement</span></span> | <span data-ttu-id="08fa0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="08fa0-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="08fa0-126">Header</span><span class="sxs-lookup"><span data-stu-id="08fa0-126">Header</span></span><br/> | <dl> <span data-ttu-id="08fa0-127"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="08fa0-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08fa0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08fa0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08fa0-129">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="08fa0-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




