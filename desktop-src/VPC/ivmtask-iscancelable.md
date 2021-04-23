---
title: Свойство Ивмтаск (Впккоминтерфацес. h)
description: Определяет, может ли задача быть отменена.
ms.assetid: abb8a29a-7f5b-45ba-ae79-d422dfb2f39d
keywords:
- Свойство, которое доменяется Virtual PC
- Свойство, которое доменяется Virtual PC, интерфейс Ивмтаск
- Ивмтаск интерфейс Virtual PC, свойство, которое доменяется
topic_type:
- apiref
api_name:
- IVMTask.IsCancelable
- IVMTask.get_IsCancelable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd06db3fc338277d7551233b0d609ceae03f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137223"
---
# <a name="ivmtaskiscancelable-property"></a><span data-ttu-id="c4cbc-106">Свойство Ивмтаск::, которое следует отменять</span><span class="sxs-lookup"><span data-stu-id="c4cbc-106">IVMTask::IsCancelable property</span></span>

<span data-ttu-id="c4cbc-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c4cbc-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c4cbc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c4cbc-109">Определяет, может ли задача быть отменена.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-109">Determines whether the task can be canceled.</span></span>

<span data-ttu-id="c4cbc-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4cbc-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4cbc-111">Syntax</span></span>


```C++
HRESULT get_IsCancelable(
  [out, retval] VARIANT_BOOL *isCancelable
);
```



## <a name="property-value"></a><span data-ttu-id="c4cbc-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c4cbc-112">Property value</span></span>

<span data-ttu-id="c4cbc-113">**Значение true** , если задачу можно отменить до завершения, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-113">**TRUE** if the task can be canceled before completion and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4cbc-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c4cbc-114">Error codes</span></span>



| <span data-ttu-id="c4cbc-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c4cbc-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c4cbc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c4cbc-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c4cbc-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c4cbc-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c4cbc-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c4cbc-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c4cbc-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c4cbc-120">Значение параметра равно **null**.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="c4cbc-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c4cbc-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c4cbc-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c4cbc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c4cbc-123">Requirements</span></span>



| <span data-ttu-id="c4cbc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c4cbc-124">Requirement</span></span> | <span data-ttu-id="c4cbc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c4cbc-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4cbc-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4cbc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c4cbc-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c4cbc-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4cbc-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4cbc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c4cbc-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c4cbc-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c4cbc-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c4cbc-130">End of client support</span></span><br/>    | <span data-ttu-id="c4cbc-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c4cbc-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c4cbc-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="c4cbc-132">Product</span></span><br/>                  | <span data-ttu-id="c4cbc-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c4cbc-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c4cbc-134">Header</span><span class="sxs-lookup"><span data-stu-id="c4cbc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4cbc-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4cbc-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c4cbc-136">IID</span><span class="sxs-lookup"><span data-stu-id="c4cbc-136">IID</span></span><br/>                      | <span data-ttu-id="c4cbc-137">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="c4cbc-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="c4cbc-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4cbc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4cbc-139">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="c4cbc-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

