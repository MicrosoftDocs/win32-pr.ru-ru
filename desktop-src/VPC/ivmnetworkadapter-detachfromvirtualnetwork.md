---
title: Метод Ивмнетворкадаптер Детачфромвиртуалнетворк (Впккоминтерфацес. h)
description: Отключает сетевой интерфейс от своей виртуальной сети.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- Метод Детачфромвиртуалнетворк Virtual PC
- Метод Детачфромвиртуалнетворк Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, метод Детачфромвиртуалнетворк
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415680"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a><span data-ttu-id="c7fb0-106">Ивмнетворкадаптер: метод:D Етачфромвиртуалнетворк</span><span class="sxs-lookup"><span data-stu-id="c7fb0-106">IVMNetworkAdapter::DetachFromVirtualNetwork method</span></span>

<span data-ttu-id="c7fb0-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c7fb0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c7fb0-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c7fb0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c7fb0-109">Отключает сетевой интерфейс от своей виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c7fb0-109">Detaches the network interface from its virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fb0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7fb0-110">Syntax</span></span>


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a><span data-ttu-id="c7fb0-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7fb0-111">Parameters</span></span>

<span data-ttu-id="c7fb0-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c7fb0-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7fb0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7fb0-113">Return value</span></span>

<span data-ttu-id="c7fb0-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c7fb0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c7fb0-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c7fb0-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="c7fb0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c7fb0-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c7fb0-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c7fb0-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c7fb0-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c7fb0-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c7fb0-119"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c7fb0-119"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c7fb0-120">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c7fb0-120">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7fb0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c7fb0-121">Requirements</span></span>



| <span data-ttu-id="c7fb0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c7fb0-122">Requirement</span></span> | <span data-ttu-id="c7fb0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c7fb0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fb0-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7fb0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fb0-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c7fb0-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7fb0-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7fb0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fb0-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c7fb0-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c7fb0-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c7fb0-128">End of client support</span></span><br/>    | <span data-ttu-id="c7fb0-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c7fb0-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c7fb0-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="c7fb0-130">Product</span></span><br/>                  | <span data-ttu-id="c7fb0-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c7fb0-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c7fb0-132">Header</span><span class="sxs-lookup"><span data-stu-id="c7fb0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7fb0-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fb0-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c7fb0-134">IID</span><span class="sxs-lookup"><span data-stu-id="c7fb0-134">IID</span></span><br/>                      | <span data-ttu-id="c7fb0-135">IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="c7fb0-135">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c7fb0-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7fb0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fb0-137">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="c7fb0-137">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

