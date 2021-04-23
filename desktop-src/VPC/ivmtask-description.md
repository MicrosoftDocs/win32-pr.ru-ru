---
title: Свойство Description Ивмтаск (Впккоминтерфацес. h)
description: Извлекает описание задачи.
ms.assetid: f1d5c7a2-b29e-4a8d-9cbd-263c168ec658
keywords:
- Свойство описания Virtual PC
- Свойство описания Virtual PC, интерфейс Ивмтаск
- Интерфейс Ивмтаск Virtual PC, свойство Description
topic_type:
- apiref
api_name:
- IVMTask.Description
- IVMTask.get_Description
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62123174a61aa9b1c58ec36be69774e10e75de59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650394"
---
# <a name="ivmtaskdescription-property"></a><span data-ttu-id="74f88-106">Ивмтаск: свойство Описание:D</span><span class="sxs-lookup"><span data-stu-id="74f88-106">IVMTask::Description property</span></span>

<span data-ttu-id="74f88-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="74f88-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="74f88-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="74f88-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="74f88-109">Извлекает описание задачи.</span><span class="sxs-lookup"><span data-stu-id="74f88-109">Retrieves a description of the task.</span></span>

<span data-ttu-id="74f88-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="74f88-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f88-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74f88-111">Syntax</span></span>


```C++
HRESULT get_Description(
  [out, retval] BSTR *description
);
```



## <a name="property-value"></a><span data-ttu-id="74f88-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="74f88-112">Property value</span></span>

<span data-ttu-id="74f88-113">Описание задачи, заданное виртуальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="74f88-113">The description of the task, as set by Virtual PC.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74f88-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="74f88-114">Error codes</span></span>



| <span data-ttu-id="74f88-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="74f88-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="74f88-116">Значение</span><span class="sxs-lookup"><span data-stu-id="74f88-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="74f88-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="74f88-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="74f88-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="74f88-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="74f88-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="74f88-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="74f88-120">Значение параметра равно **null**.</span><span class="sxs-lookup"><span data-stu-id="74f88-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="74f88-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="74f88-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="74f88-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="74f88-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="74f88-123">Требования</span><span class="sxs-lookup"><span data-stu-id="74f88-123">Requirements</span></span>



| <span data-ttu-id="74f88-124">Требование</span><span class="sxs-lookup"><span data-stu-id="74f88-124">Requirement</span></span> | <span data-ttu-id="74f88-125">Значение</span><span class="sxs-lookup"><span data-stu-id="74f88-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f88-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74f88-126">Minimum supported client</span></span><br/> | <span data-ttu-id="74f88-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="74f88-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74f88-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74f88-128">Minimum supported server</span></span><br/> | <span data-ttu-id="74f88-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74f88-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="74f88-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="74f88-130">End of client support</span></span><br/>    | <span data-ttu-id="74f88-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74f88-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="74f88-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="74f88-132">Product</span></span><br/>                  | <span data-ttu-id="74f88-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="74f88-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="74f88-134">Header</span><span class="sxs-lookup"><span data-stu-id="74f88-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f88-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="74f88-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="74f88-136">IID</span><span class="sxs-lookup"><span data-stu-id="74f88-136">IID</span></span><br/>                      | <span data-ttu-id="74f88-137">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="74f88-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="74f88-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74f88-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f88-139">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="74f88-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

