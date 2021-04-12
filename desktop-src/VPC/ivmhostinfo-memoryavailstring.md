---
title: Свойство Меморяваилстринг Ивмхостинфо (Впккоминтерфацес. h)
description: Извлекает объем доступной физической памяти на хост-компьютере в мегабайтах в виде строки.
ms.assetid: a0f17dda-2042-4aec-9968-6662d32684cf
keywords:
- Меморяваилстринг свойство Virtual PC
- Меморяваилстринг свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Меморяваилстринг
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvailString
- IVMHostInfo.get_MemoryAvailString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea003b94d0d4604dfba3daf545a51b9d69b6708c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491307"
---
# <a name="ivmhostinfomemoryavailstring-property"></a><span data-ttu-id="ee2ea-106">Свойство Ивмхостинфо:: Меморяваилстринг</span><span class="sxs-lookup"><span data-stu-id="ee2ea-106">IVMHostInfo::MemoryAvailString property</span></span>

<span data-ttu-id="ee2ea-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ee2ea-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ee2ea-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ee2ea-109">Извлекает объем доступной физической памяти на хост-компьютере в мегабайтах в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-109">Retrieves the amount of available physical memory in the host machine, in megabytes, as a string.</span></span>

<span data-ttu-id="ee2ea-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee2ea-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee2ea-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvailString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="ee2ea-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ee2ea-112">Property value</span></span>

<span data-ttu-id="ee2ea-113">Доступный объем физической памяти в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-113">The available physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee2ea-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ee2ea-114">Error codes</span></span>



| <span data-ttu-id="ee2ea-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="ee2ea-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ee2ea-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ee2ea-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ee2ea-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ee2ea-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ee2ea-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ee2ea-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="ee2ea-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ee2ea-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ee2ea-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ee2ea-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ee2ea-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ee2ea-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ee2ea-123">Requirements</span></span>



| <span data-ttu-id="ee2ea-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ee2ea-124">Requirement</span></span> | <span data-ttu-id="ee2ea-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ee2ea-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee2ea-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee2ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ee2ea-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ee2ea-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee2ea-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee2ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ee2ea-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ee2ea-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ee2ea-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ee2ea-130">End of client support</span></span><br/>    | <span data-ttu-id="ee2ea-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee2ea-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ee2ea-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="ee2ea-132">Product</span></span><br/>                  | <span data-ttu-id="ee2ea-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ee2ea-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ee2ea-134">Header</span><span class="sxs-lookup"><span data-stu-id="ee2ea-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee2ea-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee2ea-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ee2ea-136">IID</span><span class="sxs-lookup"><span data-stu-id="ee2ea-136">IID</span></span><br/>                      | <span data-ttu-id="ee2ea-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="ee2ea-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ee2ea-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee2ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee2ea-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="ee2ea-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

