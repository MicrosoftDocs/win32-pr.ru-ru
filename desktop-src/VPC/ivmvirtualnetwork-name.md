---
title: Свойство имени Ивмвиртуалнетворк (Впккоминтерфацес. h)
description: Уникальное имя экземпляра виртуальной сети.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Имя свойство Virtual PC
- Имя свойство Virtual PC, интерфейс Ивмвиртуалнетворк
- Ивмвиртуалнетворк интерфейс Virtual PC, свойство Name
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989206"
---
# <a name="ivmvirtualnetworkname-property"></a><span data-ttu-id="95f35-106">Свойство Ивмвиртуалнетворк:: Name</span><span class="sxs-lookup"><span data-stu-id="95f35-106">IVMVirtualNetwork::Name property</span></span>

<span data-ttu-id="95f35-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="95f35-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="95f35-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="95f35-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="95f35-109">Извлекает уникальное имя экземпляра виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95f35-109">Retrieves the unique name of the virtual network instance.</span></span>

<span data-ttu-id="95f35-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="95f35-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f35-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95f35-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a><span data-ttu-id="95f35-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="95f35-112">Property value</span></span>

<span data-ttu-id="95f35-113">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95f35-113">The name of the virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="95f35-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="95f35-114">Error codes</span></span>



| <span data-ttu-id="95f35-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="95f35-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="95f35-116">Значение</span><span class="sxs-lookup"><span data-stu-id="95f35-116">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95f35-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="95f35-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="95f35-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="95f35-118">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="95f35-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="95f35-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="95f35-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="95f35-120">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="95f35-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="95f35-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="95f35-122">Произошла непредвиденная ошибка, или экземпляр виртуальной сети неизвестен.</span><span class="sxs-lookup"><span data-stu-id="95f35-122">An unexpected error has occurred or the virtual network instance is unknown.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="95f35-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95f35-123">Remarks</span></span>

<span data-ttu-id="95f35-124">Имена виртуальных сетей не учитывают регистр, например "Минетворк" и "минетворк" ссылаются на одну и ту же виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="95f35-124">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="95f35-125">Требования</span><span class="sxs-lookup"><span data-stu-id="95f35-125">Requirements</span></span>



| <span data-ttu-id="95f35-126">Требование</span><span class="sxs-lookup"><span data-stu-id="95f35-126">Requirement</span></span> | <span data-ttu-id="95f35-127">Значение</span><span class="sxs-lookup"><span data-stu-id="95f35-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f35-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95f35-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95f35-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="95f35-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95f35-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95f35-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95f35-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="95f35-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="95f35-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="95f35-132">End of client support</span></span><br/>    | <span data-ttu-id="95f35-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="95f35-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="95f35-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="95f35-134">Product</span></span><br/>                  | <span data-ttu-id="95f35-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="95f35-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="95f35-136">Header</span><span class="sxs-lookup"><span data-stu-id="95f35-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="95f35-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="95f35-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="95f35-138">IID</span><span class="sxs-lookup"><span data-stu-id="95f35-138">IID</span></span><br/>                      | <span data-ttu-id="95f35-139">IID \_ ивмвиртуалнетворк определен как 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="95f35-139">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="95f35-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95f35-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f35-141">**ивмвиртуалнетворк**</span><span class="sxs-lookup"><span data-stu-id="95f35-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

