---
title: Метод Cancel Ивмтаск (Впккоминтерфацес. h)
description: Отменяет задачу.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Отмена метода Virtual PC
- Отмена метода Virtual PC, интерфейс Ивмтаск
- Интерфейс Ивмтаск Virtual PC, метод Cancel
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341235"
---
# <a name="ivmtaskcancel-method"></a><span data-ttu-id="c587d-106">Метод Ивмтаск:: Cancel</span><span class="sxs-lookup"><span data-stu-id="c587d-106">IVMTask::Cancel method</span></span>

<span data-ttu-id="c587d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c587d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c587d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c587d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c587d-109">Отменяет задачу.</span><span class="sxs-lookup"><span data-stu-id="c587d-109">Cancels the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="c587d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c587d-110">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="c587d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c587d-111">Parameters</span></span>

<span data-ttu-id="c587d-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c587d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c587d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c587d-113">Return value</span></span>

<span data-ttu-id="c587d-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c587d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c587d-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c587d-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="c587d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c587d-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c587d-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c587d-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c587d-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c587d-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c587d-119"><dt>**Д \_ Сбой**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="c587d-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="c587d-120">Задачу нельзя отменить.</span><span class="sxs-lookup"><span data-stu-id="c587d-120">The task cannot be canceled.</span></span><br/>      |
| <dl> <span data-ttu-id="c587d-121"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c587d-121"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c587d-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c587d-122">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c587d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c587d-123">Requirements</span></span>



| <span data-ttu-id="c587d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c587d-124">Requirement</span></span> | <span data-ttu-id="c587d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c587d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c587d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c587d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c587d-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c587d-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c587d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c587d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c587d-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c587d-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c587d-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c587d-130">End of client support</span></span><br/>    | <span data-ttu-id="c587d-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c587d-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c587d-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="c587d-132">Product</span></span><br/>                  | <span data-ttu-id="c587d-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c587d-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c587d-134">Header</span><span class="sxs-lookup"><span data-stu-id="c587d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c587d-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c587d-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c587d-136">IID</span><span class="sxs-lookup"><span data-stu-id="c587d-136">IID</span></span><br/>                      | <span data-ttu-id="c587d-137">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="c587d-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="c587d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c587d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c587d-139">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="c587d-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

