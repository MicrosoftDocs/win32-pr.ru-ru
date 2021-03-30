---
title: Свойство NetworkAddresses Ивмхостинфо (Впккоминтерфацес. h)
description: Возвращает перечисляемую коллекцию адресов TCP/IP на хост-компьютере.
ms.assetid: 94716b82-8f35-4702-873d-64507d879dc3
keywords:
- NetworkAddresses свойство Virtual PC
- NetworkAddresses свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство NetworkAddresses
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAddresses
- IVMHostInfo.get_NetworkAddresses
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824bedf8433c1025e1f4afc1e624c27606b8d0d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414693"
---
# <a name="ivmhostinfonetworkaddresses-property"></a><span data-ttu-id="00962-106">Свойство Ивмхостинфо:: NetworkAddresses</span><span class="sxs-lookup"><span data-stu-id="00962-106">IVMHostInfo::NetworkAddresses property</span></span>

<span data-ttu-id="00962-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="00962-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="00962-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="00962-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="00962-109">Возвращает перечисляемую коллекцию адресов TCP/IP на хост-компьютере.</span><span class="sxs-lookup"><span data-stu-id="00962-109">Retrieves an enumerable collection of TCP/IP addresses in the host machine.</span></span>

<span data-ttu-id="00962-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="00962-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="00962-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00962-111">Syntax</span></span>


```C++
HRESULT get_NetworkAddresses(
  [out, retval] VARIANT *hostAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="00962-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="00962-112">Property value</span></span>

<span data-ttu-id="00962-113">Массив адресов TCP/IP в точечно-десятичной нотации.</span><span class="sxs-lookup"><span data-stu-id="00962-113">An array of TCP/IP addresses, in dotted-decimal notation.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00962-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="00962-114">Error codes</span></span>



| <span data-ttu-id="00962-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="00962-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="00962-116">Значение</span><span class="sxs-lookup"><span data-stu-id="00962-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="00962-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="00962-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="00962-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="00962-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="00962-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="00962-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="00962-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="00962-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="00962-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="00962-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="00962-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="00962-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="00962-123">Требования</span><span class="sxs-lookup"><span data-stu-id="00962-123">Requirements</span></span>



| <span data-ttu-id="00962-124">Требование</span><span class="sxs-lookup"><span data-stu-id="00962-124">Requirement</span></span> | <span data-ttu-id="00962-125">Значение</span><span class="sxs-lookup"><span data-stu-id="00962-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="00962-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00962-126">Minimum supported client</span></span><br/> | <span data-ttu-id="00962-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="00962-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00962-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00962-128">Minimum supported server</span></span><br/> | <span data-ttu-id="00962-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="00962-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="00962-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="00962-130">End of client support</span></span><br/>    | <span data-ttu-id="00962-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="00962-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="00962-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="00962-132">Product</span></span><br/>                  | <span data-ttu-id="00962-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="00962-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="00962-134">Header</span><span class="sxs-lookup"><span data-stu-id="00962-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="00962-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="00962-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="00962-136">IID</span><span class="sxs-lookup"><span data-stu-id="00962-136">IID</span></span><br/>                      | <span data-ttu-id="00962-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="00962-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="00962-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00962-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00962-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="00962-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

