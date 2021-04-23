---
title: Свойство Ивмтаск (Впккоминтерфацес. h)
description: Определяет, завершена ли задача.
ms.assetid: 181fa220-4de2-4ab3-950b-fffc4fe4de64
keywords:
- Virtual PC свойства завершения
- Свойство AutoComplete Virtual PC, интерфейс Ивмтаск
- Интерфейс Ивмтаск Virtual PC, свойство AutoComplete
topic_type:
- apiref
api_name:
- IVMTask.IsComplete
- IVMTask.get_IsComplete
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbf046b4a16ef4e907f1fec0126d08815ca2955
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988779"
---
# <a name="ivmtaskiscomplete-property"></a><span data-ttu-id="dacc7-106">Свойство Ивмтаск:: AutoComplete</span><span class="sxs-lookup"><span data-stu-id="dacc7-106">IVMTask::IsComplete property</span></span>

<span data-ttu-id="dacc7-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dacc7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dacc7-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dacc7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dacc7-109">Определяет, завершена ли задача.</span><span class="sxs-lookup"><span data-stu-id="dacc7-109">Determines whether the task has completed.</span></span>

<span data-ttu-id="dacc7-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dacc7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dacc7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dacc7-111">Syntax</span></span>


```C++
HRESULT get_IsComplete(
  [out, retval] VARIANT_BOOL *isComplete
);
```



## <a name="property-value"></a><span data-ttu-id="dacc7-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dacc7-112">Property value</span></span>

<span data-ttu-id="dacc7-113">**Значение true** , если задача завершена, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dacc7-113">**TRUE** if the task has completed and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dacc7-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dacc7-114">Error codes</span></span>



| <span data-ttu-id="dacc7-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="dacc7-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="dacc7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dacc7-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dacc7-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dacc7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dacc7-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dacc7-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="dacc7-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="dacc7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="dacc7-120">Значение параметра равно **null**.</span><span class="sxs-lookup"><span data-stu-id="dacc7-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="dacc7-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dacc7-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="dacc7-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="dacc7-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="dacc7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="dacc7-123">Requirements</span></span>



| <span data-ttu-id="dacc7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="dacc7-124">Requirement</span></span> | <span data-ttu-id="dacc7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="dacc7-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dacc7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dacc7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dacc7-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dacc7-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dacc7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dacc7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dacc7-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dacc7-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dacc7-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dacc7-130">End of client support</span></span><br/>    | <span data-ttu-id="dacc7-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dacc7-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dacc7-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="dacc7-132">Product</span></span><br/>                  | <span data-ttu-id="dacc7-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dacc7-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dacc7-134">Header</span><span class="sxs-lookup"><span data-stu-id="dacc7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dacc7-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="dacc7-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dacc7-136">IID</span><span class="sxs-lookup"><span data-stu-id="dacc7-136">IID</span></span><br/>                      | <span data-ttu-id="dacc7-137">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="dacc7-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="dacc7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dacc7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dacc7-139">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="dacc7-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

