---
title: Свойство Хостадаптер Ивмвиртуалнетворк (Впккоминтерфацес. h)
description: Имя адаптера, к которому подключена виртуальная сеть.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Хостадаптер свойство Virtual PC
- Хостадаптер свойство Virtual PC, интерфейс Ивмвиртуалнетворк
- Ивмвиртуалнетворк интерфейс Virtual PC, свойство Хостадаптер
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071881"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a><span data-ttu-id="12fa5-106">Свойство Ивмвиртуалнетворк:: Хостадаптер</span><span class="sxs-lookup"><span data-stu-id="12fa5-106">IVMVirtualNetwork::HostAdapter property</span></span>

<span data-ttu-id="12fa5-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="12fa5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="12fa5-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="12fa5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="12fa5-109">Извлекает имя адаптера, к которому подключена виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="12fa5-109">Retrieves the name of the adapter to which the virtual network is connected.</span></span>

<span data-ttu-id="12fa5-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="12fa5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fa5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12fa5-111">Syntax</span></span>


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a><span data-ttu-id="12fa5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="12fa5-112">Property value</span></span>

<span data-ttu-id="12fa5-113">Имя адаптера узла, к которому подключена виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="12fa5-113">The name of the host adapter to which the virtual network is connected.</span></span>

## <a name="error-codes"></a><span data-ttu-id="12fa5-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="12fa5-114">Error codes</span></span>



| <span data-ttu-id="12fa5-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="12fa5-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="12fa5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="12fa5-116">Meaning</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12fa5-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="12fa5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="12fa5-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="12fa5-118">The operation was successful.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="12fa5-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="12fa5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="12fa5-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="12fa5-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="12fa5-121"><dt>Виртуальная машина \_ \_Адаптер E \_ не \_ найден</dt> <dt>0xA0040700</dt></span><span class="sxs-lookup"><span data-stu-id="12fa5-121"><dt>VM\_E\_ADAPTER\_NOT\_FOUND</dt> <dt>0xA0040700</dt></span></span> </dl> | <span data-ttu-id="12fa5-122">Ethernet-адаптер узла, к которому была подключена эта виртуальная сеть, больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="12fa5-122">The host Ethernet adapter to which this virtual network was connected is no longer available.</span></span> <span data-ttu-id="12fa5-123">Возможно, адаптер Ethernet узла был удален или отключен.</span><span class="sxs-lookup"><span data-stu-id="12fa5-123">The host Ethernet adapter may have been removed or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="12fa5-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="12fa5-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="12fa5-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="12fa5-125">An unexpected error has occurred.</span></span><br/>                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="12fa5-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12fa5-126">Remarks</span></span>

<span data-ttu-id="12fa5-127">Виртуальный сетевой адаптер позволяет виртуальной сети взаимодействовать с внешними сетями.</span><span class="sxs-lookup"><span data-stu-id="12fa5-127">The virtual network adapter allows a virtual network to talk to external networks.</span></span> <span data-ttu-id="12fa5-128">Обычно на хост-компьютере установлен один адаптер для каждого адаптера Ethernet.</span><span class="sxs-lookup"><span data-stu-id="12fa5-128">There is normally one adapter per Ethernet adapter installed in the host machine.</span></span> <span data-ttu-id="12fa5-129">Например, предположим, что на главном компьютере был адаптер с меткой "10/100 ЕНЕТ".</span><span class="sxs-lookup"><span data-stu-id="12fa5-129">For example, let's say a host machine had an adapter labeled "10/100 ENET".</span></span> <span data-ttu-id="12fa5-130">Чтобы подключить виртуальный сетевой адаптер к сети, подключенной к "10/100 ЕНЕТ", задайте для свойства **Хостадаптер** сети виртуальной сети значение "10/100 енет" и подключите виртуальный сетевой адаптер к этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="12fa5-130">To connect a virtual NIC to the network attached to "10/100 ENET", set the virtual network's Network **HostAdapter** property to "10/100 ENET" and connect the virtual NIC to this virtual network.</span></span>

<span data-ttu-id="12fa5-131">Если для свойства **хостадаптер** задана пустая строка (""), адаптер виртуального сетевого адаптера подключается к сети "внутренняя сеть" или "Общая сеть (NAT)".</span><span class="sxs-lookup"><span data-stu-id="12fa5-131">If the **HostAdapter** property is set to an empty string (""), the virtual NIC adapter is connected to the "Internal Network" or "Shared Networking (NAT)" network.</span></span> <span data-ttu-id="12fa5-132">Виртуальные сетевые карты, подключенные к сети "внутренняя сеть", не будут иметь доступа к внешним сетям на узле системы.</span><span class="sxs-lookup"><span data-stu-id="12fa5-132">Virtual NICs attached to the "Internal Network" network will have no access to external networks on the system host.</span></span> <span data-ttu-id="12fa5-133">Однако виртуальные сетевые карты, подключенные к этой виртуальной сети, по-прежнему могут взаимодействовать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="12fa5-133">However, the virtual NICs attached to this virtual network are still able to communicate with each other.</span></span>

<span data-ttu-id="12fa5-134">Полный список адаптеров можно получить с помощью свойства [**ивмхостинфо:: адаптера**](ivmhostinfo-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="12fa5-134">The complete list of adapters can be accessed through the [**IVMHostInfo::NetworkAdapters**](ivmhostinfo-networkadapters.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="12fa5-135">Требования</span><span class="sxs-lookup"><span data-stu-id="12fa5-135">Requirements</span></span>



| <span data-ttu-id="12fa5-136">Требование</span><span class="sxs-lookup"><span data-stu-id="12fa5-136">Requirement</span></span> | <span data-ttu-id="12fa5-137">Значение</span><span class="sxs-lookup"><span data-stu-id="12fa5-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="12fa5-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12fa5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="12fa5-139">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="12fa5-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12fa5-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12fa5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="12fa5-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="12fa5-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="12fa5-142">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="12fa5-142">End of client support</span></span><br/>    | <span data-ttu-id="12fa5-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="12fa5-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="12fa5-144">Продукт</span><span class="sxs-lookup"><span data-stu-id="12fa5-144">Product</span></span><br/>                  | <span data-ttu-id="12fa5-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="12fa5-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="12fa5-146">Header</span><span class="sxs-lookup"><span data-stu-id="12fa5-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="12fa5-147"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fa5-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="12fa5-148">IID</span><span class="sxs-lookup"><span data-stu-id="12fa5-148">IID</span></span><br/>                      | <span data-ttu-id="12fa5-149">IID \_ ивмвиртуалнетворк определен как 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="12fa5-149">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="12fa5-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12fa5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fa5-151">**ивмвиртуалнетворк**</span><span class="sxs-lookup"><span data-stu-id="12fa5-151">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

