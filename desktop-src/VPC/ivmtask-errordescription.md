---
title: Свойство ErrorDescription Ивмтаск (Впккоминтерфацес. h)
description: Извлекает локализованное описание ошибки, записанное для этой задачи.
ms.assetid: 85728775-14b6-4031-9ccd-4c4f8c410705
keywords:
- ErrorDescription свойство Virtual PC
- ErrorDescription свойство Virtual PC, интерфейс Ивмтаск
- Ивмтаск интерфейс Virtual PC, свойство ErrorDescription
topic_type:
- apiref
api_name:
- IVMTask.ErrorDescription
- IVMTask.get_ErrorDescription
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5c95eac383d8e071832fdbf7843c01345278c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803473"
---
# <a name="ivmtaskerrordescription-property"></a><span data-ttu-id="50ecb-106">Свойство Ивмтаск:: ErrorDescription</span><span class="sxs-lookup"><span data-stu-id="50ecb-106">IVMTask::ErrorDescription property</span></span>

<span data-ttu-id="50ecb-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="50ecb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="50ecb-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="50ecb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="50ecb-109">Извлекает локализованное описание ошибки, записанное для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="50ecb-109">Retrieves the localized error description recorded for this task.</span></span>

<span data-ttu-id="50ecb-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="50ecb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ecb-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50ecb-111">Syntax</span></span>


```C++
HRESULT get_ErrorDescription(
  [out, retval] BSTR *outErrorDesc
);
```



## <a name="property-value"></a><span data-ttu-id="50ecb-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="50ecb-112">Property value</span></span>

<span data-ttu-id="50ecb-113">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="50ecb-113">The error description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50ecb-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="50ecb-114">Error codes</span></span>



| <span data-ttu-id="50ecb-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="50ecb-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="50ecb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="50ecb-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="50ecb-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="50ecb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="50ecb-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="50ecb-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="50ecb-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="50ecb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="50ecb-120">Значение параметра равно **null**.</span><span class="sxs-lookup"><span data-stu-id="50ecb-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="50ecb-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="50ecb-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="50ecb-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="50ecb-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="50ecb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="50ecb-123">Requirements</span></span>



| <span data-ttu-id="50ecb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="50ecb-124">Requirement</span></span> | <span data-ttu-id="50ecb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="50ecb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ecb-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50ecb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="50ecb-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="50ecb-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50ecb-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50ecb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="50ecb-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="50ecb-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="50ecb-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="50ecb-130">End of client support</span></span><br/>    | <span data-ttu-id="50ecb-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50ecb-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="50ecb-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="50ecb-132">Product</span></span><br/>                  | <span data-ttu-id="50ecb-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="50ecb-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="50ecb-134">Header</span><span class="sxs-lookup"><span data-stu-id="50ecb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="50ecb-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="50ecb-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="50ecb-136">IID</span><span class="sxs-lookup"><span data-stu-id="50ecb-136">IID</span></span><br/>                      | <span data-ttu-id="50ecb-137">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="50ecb-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="50ecb-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50ecb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ecb-139">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="50ecb-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

