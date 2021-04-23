---
title: Свойство Параллелпортс Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Возвращает перечисляемую коллекцию параллельных портов.
ms.assetid: 458e6e77-3728-4b5c-910b-f958f42785e4
keywords:
- Параллелпортс свойство Virtual PC
- Параллелпортс свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Параллелпортс
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ParallelPorts
- IVMVirtualMachine.get_ParallelPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aba742a206857e73e0d1447f422f7182fb7a304
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137214"
---
# <a name="ivmvirtualmachineparallelports-property"></a><span data-ttu-id="96c35-106">Ивмвиртуалмачине: свойство Араллелпортс:P</span><span class="sxs-lookup"><span data-stu-id="96c35-106">IVMVirtualMachine::ParallelPorts property</span></span>

<span data-ttu-id="96c35-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="96c35-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96c35-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="96c35-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96c35-109">Возвращает перечисляемую коллекцию параллельных портов.</span><span class="sxs-lookup"><span data-stu-id="96c35-109">Retrieves an enumerable collection of parallel ports.</span></span>

<span data-ttu-id="96c35-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="96c35-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c35-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96c35-111">Syntax</span></span>


```C++
HRESULT get_ParallelPorts(
  [out, retval] IVMParallelPortCollection **parallelPortCollection
);
```



## <a name="property-value"></a><span data-ttu-id="96c35-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="96c35-112">Property value</span></span>

<span data-ttu-id="96c35-113">Объект [**ивмпараллелпортколлектион**](ivmparallelportcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="96c35-113">An [**IVMParallelPortCollection**](ivmparallelportcollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="96c35-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="96c35-114">Error codes</span></span>



| <span data-ttu-id="96c35-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="96c35-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="96c35-116">Значение</span><span class="sxs-lookup"><span data-stu-id="96c35-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="96c35-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="96c35-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="96c35-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="96c35-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="96c35-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="96c35-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="96c35-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="96c35-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="96c35-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="96c35-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="96c35-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="96c35-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="96c35-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="96c35-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="96c35-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="96c35-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="96c35-125">Требования</span><span class="sxs-lookup"><span data-stu-id="96c35-125">Requirements</span></span>



| <span data-ttu-id="96c35-126">Требование</span><span class="sxs-lookup"><span data-stu-id="96c35-126">Requirement</span></span> | <span data-ttu-id="96c35-127">Значение</span><span class="sxs-lookup"><span data-stu-id="96c35-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96c35-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96c35-128">Minimum supported client</span></span><br/> | <span data-ttu-id="96c35-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="96c35-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96c35-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96c35-130">Minimum supported server</span></span><br/> | <span data-ttu-id="96c35-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="96c35-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96c35-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="96c35-132">End of client support</span></span><br/>    | <span data-ttu-id="96c35-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96c35-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96c35-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="96c35-134">Product</span></span><br/>                  | <span data-ttu-id="96c35-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96c35-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96c35-136">Header</span><span class="sxs-lookup"><span data-stu-id="96c35-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="96c35-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="96c35-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96c35-138">IID</span><span class="sxs-lookup"><span data-stu-id="96c35-138">IID</span></span><br/>                      | <span data-ttu-id="96c35-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="96c35-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="96c35-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96c35-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c35-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="96c35-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

