---
title: Свойство Перценткомплетед Ивмтаск (Впккоминтерфацес. h)
description: Возвращает процент завершения задачи.
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- Перценткомплетед свойство Virtual PC
- Перценткомплетед свойство Virtual PC, интерфейс Ивмтаск
- Ивмтаск интерфейс Virtual PC, свойство Перценткомплетед
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa820adbbde2fc68632da27a9b146bd0e8f40143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803472"
---
# <a name="ivmtaskpercentcompleted-property"></a><span data-ttu-id="a6a34-106">Ивмтаск: свойство Ерценткомплетед:P</span><span class="sxs-lookup"><span data-stu-id="a6a34-106">IVMTask::PercentCompleted property</span></span>

<span data-ttu-id="a6a34-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a6a34-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a6a34-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a6a34-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a6a34-109">Возвращает процент завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="a6a34-109">Retrieves the completion percentage of the task.</span></span>

<span data-ttu-id="a6a34-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a6a34-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a34-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6a34-111">Syntax</span></span>


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a><span data-ttu-id="a6a34-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a6a34-112">Property value</span></span>

<span data-ttu-id="a6a34-113">Текущий процент завершения.</span><span class="sxs-lookup"><span data-stu-id="a6a34-113">The current completion percentage.</span></span> <span data-ttu-id="a6a34-114">Значение — число от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="a6a34-114">The value is a number between 0 and 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a6a34-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a6a34-115">Error codes</span></span>



| <span data-ttu-id="a6a34-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="a6a34-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a6a34-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a6a34-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a6a34-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a6a34-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a6a34-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a6a34-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a6a34-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="a6a34-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a6a34-121">Значение параметра равно **null**.</span><span class="sxs-lookup"><span data-stu-id="a6a34-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="a6a34-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a6a34-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a6a34-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a6a34-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a6a34-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a6a34-124">Requirements</span></span>



| <span data-ttu-id="a6a34-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a6a34-125">Requirement</span></span> | <span data-ttu-id="a6a34-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a6a34-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a34-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6a34-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a34-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a6a34-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6a34-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6a34-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a34-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a6a34-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a6a34-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a6a34-131">End of client support</span></span><br/>    | <span data-ttu-id="a6a34-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6a34-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a6a34-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="a6a34-133">Product</span></span><br/>                  | <span data-ttu-id="a6a34-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a6a34-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a6a34-135">Header</span><span class="sxs-lookup"><span data-stu-id="a6a34-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a34-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a34-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a6a34-137">IID</span><span class="sxs-lookup"><span data-stu-id="a6a34-137">IID</span></span><br/>                      | <span data-ttu-id="a6a34-138">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="a6a34-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="a6a34-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6a34-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a34-140">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="a6a34-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

