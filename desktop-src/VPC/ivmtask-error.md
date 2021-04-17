---
title: Свойство ошибки Ивмтаск (Впккоминтерфацес. h)
description: Возвращает ошибку, записанную для этой задачи.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Ошибка свойства Virtual PC
- Свойство ошибки Virtual PC, интерфейс Ивмтаск
- Интерфейс Ивмтаск Virtual PC, свойство Error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691866"
---
# <a name="ivmtaskerror-property"></a><span data-ttu-id="3bf41-106">Свойство Ивмтаск:: Error</span><span class="sxs-lookup"><span data-stu-id="3bf41-106">IVMTask::Error property</span></span>

<span data-ttu-id="3bf41-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3bf41-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3bf41-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3bf41-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3bf41-109">Возвращает ошибку, записанную для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="3bf41-109">Retrieves the error recorded for this task.</span></span>

<span data-ttu-id="3bf41-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3bf41-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf41-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bf41-111">Syntax</span></span>


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a><span data-ttu-id="3bf41-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3bf41-112">Property value</span></span>

<span data-ttu-id="3bf41-113">Записанная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3bf41-113">The recorded error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3bf41-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3bf41-114">Error codes</span></span>

<span data-ttu-id="3bf41-115">Экземпляры [**ивмтаск**](ivmtask.md) , возвращаемые другими интерфейсами, могут возвращать дополнительные значения.</span><span class="sxs-lookup"><span data-stu-id="3bf41-115">Instances of [**IVMTask**](ivmtask.md) returned by other interfaces may return additional values.</span></span> <span data-ttu-id="3bf41-116">Дополнительные сведения см. в документации по методам, которые возвращают экземпляр **ивмтаск** .</span><span class="sxs-lookup"><span data-stu-id="3bf41-116">For details, see the documentation of the methods that return a **IVMTask** instance.</span></span>



| <span data-ttu-id="3bf41-117">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="3bf41-117">Name/value</span></span>                                                                                                                                                                        | <span data-ttu-id="3bf41-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3bf41-118">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="3bf41-119"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3bf41-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                           | <span data-ttu-id="3bf41-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3bf41-120">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="3bf41-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="3bf41-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                             | <span data-ttu-id="3bf41-122">Значение параметра равно **null**.</span><span class="sxs-lookup"><span data-stu-id="3bf41-122">The parameter value is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="3bf41-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3bf41-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                     | <span data-ttu-id="3bf41-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3bf41-124">An unexpected error has occurred.</span></span><br/>                          |
| <dl> <span data-ttu-id="3bf41-125"><dt>Виртуальная машина \_ E \_ вмвиртуалпк \_ более старая \_ версия</dt> <dt>0xA0040952</dt></span><span class="sxs-lookup"><span data-stu-id="3bf41-125"><dt>VM\_E\_VMVIRTUALPC\_OLDER\_VERSION</dt> <dt>0xA0040952</dt></span></span> </dl>     | <span data-ttu-id="3bf41-126">Установлены виртуальные компьютеры 2007 и Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="3bf41-126">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <dl> <span data-ttu-id="3bf41-127"><dt>Виртуальная машина \_ \_Другие 0xA0040953 \_ \_ по виртуализации</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3bf41-127"><dt>VM\_E\_OTHER\_VIRTUALIZATION\_SOFTWARE</dt> <dt>0xA0040953</dt></span></span> </dl> | <span data-ttu-id="3bf41-128">Установлено другое программное обеспечение виртуализации.</span><span class="sxs-lookup"><span data-stu-id="3bf41-128">Other virtualization software is installed.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="3bf41-129">Требования</span><span class="sxs-lookup"><span data-stu-id="3bf41-129">Requirements</span></span>



| <span data-ttu-id="3bf41-130">Требование</span><span class="sxs-lookup"><span data-stu-id="3bf41-130">Requirement</span></span> | <span data-ttu-id="3bf41-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3bf41-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf41-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3bf41-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3bf41-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3bf41-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bf41-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3bf41-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3bf41-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3bf41-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3bf41-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3bf41-136">End of client support</span></span><br/>    | <span data-ttu-id="3bf41-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3bf41-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3bf41-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="3bf41-138">Product</span></span><br/>                  | <span data-ttu-id="3bf41-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3bf41-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3bf41-140">Header</span><span class="sxs-lookup"><span data-stu-id="3bf41-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bf41-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bf41-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3bf41-142">IID</span><span class="sxs-lookup"><span data-stu-id="3bf41-142">IID</span></span><br/>                      | <span data-ttu-id="3bf41-143">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="3bf41-143">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="3bf41-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3bf41-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bf41-145">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="3bf41-145">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

