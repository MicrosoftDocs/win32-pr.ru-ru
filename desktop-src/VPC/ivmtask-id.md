---
title: Свойство идентификатора Ивмтаск (Впккоминтерфацес. h)
description: Извлекает уникальный идентификатор для этой задачи.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- Идентификатор свойства Virtual PC
- Свойство ID Virtual PC, интерфейс Ивмтаск
- Ивмтаск интерфейс Virtual PC, свойство ID
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892497"
---
# <a name="ivmtaskid-property"></a><span data-ttu-id="87cda-106">Свойство Ивмтаск:: ID</span><span class="sxs-lookup"><span data-stu-id="87cda-106">IVMTask::ID property</span></span>

<span data-ttu-id="87cda-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="87cda-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="87cda-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="87cda-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="87cda-109">Извлекает уникальный идентификатор для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="87cda-109">Retrieves a unique identifier for this task.</span></span>

<span data-ttu-id="87cda-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87cda-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cda-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87cda-111">Syntax</span></span>


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a><span data-ttu-id="87cda-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="87cda-112">Property value</span></span>

<span data-ttu-id="87cda-113">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="87cda-113">The unique identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="87cda-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="87cda-114">Error codes</span></span>



| <span data-ttu-id="87cda-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="87cda-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="87cda-116">Значение</span><span class="sxs-lookup"><span data-stu-id="87cda-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="87cda-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="87cda-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="87cda-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="87cda-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="87cda-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="87cda-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="87cda-120">Значение параметра равно **null**.</span><span class="sxs-lookup"><span data-stu-id="87cda-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="87cda-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="87cda-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="87cda-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="87cda-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="87cda-123">Требования</span><span class="sxs-lookup"><span data-stu-id="87cda-123">Requirements</span></span>



| <span data-ttu-id="87cda-124">Требование</span><span class="sxs-lookup"><span data-stu-id="87cda-124">Requirement</span></span> | <span data-ttu-id="87cda-125">Значение</span><span class="sxs-lookup"><span data-stu-id="87cda-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="87cda-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87cda-126">Minimum supported client</span></span><br/> | <span data-ttu-id="87cda-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="87cda-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87cda-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87cda-128">Minimum supported server</span></span><br/> | <span data-ttu-id="87cda-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="87cda-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="87cda-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="87cda-130">End of client support</span></span><br/>    | <span data-ttu-id="87cda-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="87cda-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="87cda-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="87cda-132">Product</span></span><br/>                  | <span data-ttu-id="87cda-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="87cda-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="87cda-134">Header</span><span class="sxs-lookup"><span data-stu-id="87cda-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="87cda-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="87cda-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="87cda-136">IID</span><span class="sxs-lookup"><span data-stu-id="87cda-136">IID</span></span><br/>                      | <span data-ttu-id="87cda-137">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="87cda-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="87cda-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87cda-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cda-139">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="87cda-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

