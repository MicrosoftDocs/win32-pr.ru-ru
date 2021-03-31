---
title: Свойство VirtualNetwork Ивмнетворкадаптер (Впккоминтерфацес. h)
description: Извлекает виртуальную сеть, к которой подключен сетевой интерфейс.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork свойство Virtual PC
- VirtualNetwork свойство Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, свойство VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071062"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a><span data-ttu-id="73548-106">Свойство Ивмнетворкадаптер:: VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73548-106">IVMNetworkAdapter::VirtualNetwork property</span></span>

<span data-ttu-id="73548-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="73548-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="73548-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="73548-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="73548-109">Извлекает виртуальную сеть, к которой подключен сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="73548-109">Retrieves the virtual network to which the network interface is attached.</span></span>

<span data-ttu-id="73548-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="73548-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73548-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73548-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="73548-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="73548-112">Property value</span></span>

<span data-ttu-id="73548-113">Интерфейс [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) , представляющий виртуальную сеть, к которой подключен этот виртуальный сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="73548-113">An [**IVMVirtualNetwork**](ivmvirtualnetwork.md) interface that represents the virtual network to which this virtual network interface is attached.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73548-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="73548-114">Error codes</span></span>



| <span data-ttu-id="73548-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="73548-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="73548-116">Значение</span><span class="sxs-lookup"><span data-stu-id="73548-116">Meaning</span></span>                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73548-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="73548-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="73548-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="73548-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="73548-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="73548-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="73548-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="73548-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="73548-121"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="73548-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="73548-122">Этот сетевой интерфейс не подключен и не подключен к виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="73548-122">This network interface is unplugged and is not connected to a virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="73548-123"><dt>Виртуальная машина \_ E \_ Недопустимый \_ \_ \_ идентификатор виртуальной сети</dt> <dt>0xA00400702</dt></span><span class="sxs-lookup"><span data-stu-id="73548-123"><dt>VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID</dt> <dt>0xA00400702</dt></span></span> </dl> | <span data-ttu-id="73548-124">Этот интерфейс подключен к виртуальной сети с недопустимым ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="73548-124">This interface is connected to a virtual network with an invalid ID.</span></span><br/>           |
| <dl> <span data-ttu-id="73548-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="73548-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="73548-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="73548-126">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="73548-127">Требования</span><span class="sxs-lookup"><span data-stu-id="73548-127">Requirements</span></span>



| <span data-ttu-id="73548-128">Требование</span><span class="sxs-lookup"><span data-stu-id="73548-128">Requirement</span></span> | <span data-ttu-id="73548-129">Значение</span><span class="sxs-lookup"><span data-stu-id="73548-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73548-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73548-130">Minimum supported client</span></span><br/> | <span data-ttu-id="73548-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="73548-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73548-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73548-132">Minimum supported server</span></span><br/> | <span data-ttu-id="73548-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="73548-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="73548-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="73548-134">End of client support</span></span><br/>    | <span data-ttu-id="73548-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73548-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="73548-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="73548-136">Product</span></span><br/>                  | <span data-ttu-id="73548-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="73548-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="73548-138">Header</span><span class="sxs-lookup"><span data-stu-id="73548-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="73548-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="73548-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="73548-140">IID</span><span class="sxs-lookup"><span data-stu-id="73548-140">IID</span></span><br/>                      | <span data-ttu-id="73548-141">IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="73548-141">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="73548-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73548-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73548-143">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="73548-143">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

