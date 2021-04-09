---
title: Свойство имени Ивмпараллелпорт (Впккоминтерфацес. h)
description: Имя параллельного порта.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Имя свойство Virtual PC
- Имя свойство Virtual PC, интерфейс Ивмпараллелпорт
- Ивмпараллелпорт интерфейс Virtual PC, свойство Name
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135038"
---
# <a name="ivmparallelportname-property"></a><span data-ttu-id="94bed-106">Свойство Ивмпараллелпорт:: Name</span><span class="sxs-lookup"><span data-stu-id="94bed-106">IVMParallelPort::Name property</span></span>

<span data-ttu-id="94bed-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="94bed-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="94bed-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="94bed-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="94bed-109">Возвращает и задает имя параллельного порта.</span><span class="sxs-lookup"><span data-stu-id="94bed-109">Retrieves and sets the name of the parallel port.</span></span>

<span data-ttu-id="94bed-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="94bed-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="94bed-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94bed-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="94bed-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="94bed-112">Property value</span></span>

<span data-ttu-id="94bed-113">Задает имя параллельного порта (например, «LPT1»).</span><span class="sxs-lookup"><span data-stu-id="94bed-113">Sets the name of the parallel port (for example, "LPT1").</span></span>

## <a name="error-codes"></a><span data-ttu-id="94bed-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="94bed-114">Error codes</span></span>



| <span data-ttu-id="94bed-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="94bed-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="94bed-116">Значение</span><span class="sxs-lookup"><span data-stu-id="94bed-116">Meaning</span></span>                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="94bed-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="94bed-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="94bed-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="94bed-118">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="94bed-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="94bed-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="94bed-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="94bed-120">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="94bed-121"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="94bed-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="94bed-122">Параметр ссылается на недопустимый параллельный порт.</span><span class="sxs-lookup"><span data-stu-id="94bed-122">The parameter refers to a parallel port that is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="94bed-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="94bed-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="94bed-124">Недопустимая конфигурация для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="94bed-124">The configuration for this virtual machine is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="94bed-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="94bed-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="94bed-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="94bed-126">An unexpected error has occurred.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="94bed-127">Требования</span><span class="sxs-lookup"><span data-stu-id="94bed-127">Requirements</span></span>



| <span data-ttu-id="94bed-128">Требование</span><span class="sxs-lookup"><span data-stu-id="94bed-128">Requirement</span></span> | <span data-ttu-id="94bed-129">Значение</span><span class="sxs-lookup"><span data-stu-id="94bed-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="94bed-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94bed-130">Minimum supported client</span></span><br/> | <span data-ttu-id="94bed-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="94bed-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94bed-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94bed-132">Minimum supported server</span></span><br/> | <span data-ttu-id="94bed-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="94bed-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="94bed-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="94bed-134">End of client support</span></span><br/>    | <span data-ttu-id="94bed-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="94bed-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="94bed-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="94bed-136">Product</span></span><br/>                  | <span data-ttu-id="94bed-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="94bed-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="94bed-138">Header</span><span class="sxs-lookup"><span data-stu-id="94bed-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="94bed-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="94bed-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="94bed-140">IID</span><span class="sxs-lookup"><span data-stu-id="94bed-140">IID</span></span><br/>                      | <span data-ttu-id="94bed-141">IID \_ ивмпараллелпорт определен как 097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="94bed-141">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="94bed-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94bed-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94bed-143">**ивмпараллелпорт**</span><span class="sxs-lookup"><span data-stu-id="94bed-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

