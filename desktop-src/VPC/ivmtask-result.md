---
title: Свойство результата Ивмтаск (Впккоминтерфацес. h)
description: Возвращает результат задачи.
ms.assetid: 640279ef-94b8-4e8f-88f3-a97cec54c121
keywords:
- Виртуальный ПК со свойством результата
- Свойство результата Virtual PC, интерфейс Ивмтаск
- Интерфейс Ивмтаск Virtual PC, свойство Result
topic_type:
- apiref
api_name:
- IVMTask.Result
- IVMTask.get_Result
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4dc36d1529633a850bc10e5c89e8c07147aea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989032"
---
# <a name="ivmtaskresult-property"></a><span data-ttu-id="87784-106">Свойство Ивмтаск:: result</span><span class="sxs-lookup"><span data-stu-id="87784-106">IVMTask::Result property</span></span>

<span data-ttu-id="87784-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="87784-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="87784-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="87784-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="87784-109">Возвращает результат задачи.</span><span class="sxs-lookup"><span data-stu-id="87784-109">Retrieves the result of the task.</span></span>

<span data-ttu-id="87784-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87784-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="87784-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87784-111">Syntax</span></span>


```C++
HRESULT get_Result(
  [out, retval] VMTaskResult *result
);
```



## <a name="property-value"></a><span data-ttu-id="87784-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="87784-112">Property value</span></span>

<span data-ttu-id="87784-113">Результат задачи.</span><span class="sxs-lookup"><span data-stu-id="87784-113">The result of the task.</span></span> <span data-ttu-id="87784-114">Список значений см. в разделе [**вмтаскресулт**](vmtaskresult.md).</span><span class="sxs-lookup"><span data-stu-id="87784-114">For a list of values, see [**VMTaskResult**](vmtaskresult.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="87784-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="87784-115">Error codes</span></span>



| <span data-ttu-id="87784-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="87784-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="87784-117">Значение</span><span class="sxs-lookup"><span data-stu-id="87784-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="87784-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="87784-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="87784-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="87784-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="87784-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="87784-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="87784-121">Значение параметра равно **null**.</span><span class="sxs-lookup"><span data-stu-id="87784-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="87784-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="87784-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="87784-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="87784-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="87784-124">Требования</span><span class="sxs-lookup"><span data-stu-id="87784-124">Requirements</span></span>



| <span data-ttu-id="87784-125">Требование</span><span class="sxs-lookup"><span data-stu-id="87784-125">Requirement</span></span> | <span data-ttu-id="87784-126">Значение</span><span class="sxs-lookup"><span data-stu-id="87784-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="87784-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87784-127">Minimum supported client</span></span><br/> | <span data-ttu-id="87784-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="87784-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87784-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87784-129">Minimum supported server</span></span><br/> | <span data-ttu-id="87784-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="87784-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="87784-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="87784-131">End of client support</span></span><br/>    | <span data-ttu-id="87784-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="87784-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="87784-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="87784-133">Product</span></span><br/>                  | <span data-ttu-id="87784-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="87784-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="87784-135">Header</span><span class="sxs-lookup"><span data-stu-id="87784-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="87784-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="87784-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="87784-137">IID</span><span class="sxs-lookup"><span data-stu-id="87784-137">IID</span></span><br/>                      | <span data-ttu-id="87784-138">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="87784-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="87784-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87784-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87784-140">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="87784-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

