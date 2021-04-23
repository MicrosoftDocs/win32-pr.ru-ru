---
title: Интерфейс Ивмнетворкадаптер (Впккоминтерфацес. h)
description: Служит интерфейсом для виртуальной сетевой карты.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Виртуальный ПК с интерфейсом Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415624"
---
# <a name="ivmnetworkadapter-interface"></a><span data-ttu-id="622ce-105">Интерфейс Ивмнетворкадаптер</span><span class="sxs-lookup"><span data-stu-id="622ce-105">IVMNetworkAdapter interface</span></span>

<span data-ttu-id="622ce-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="622ce-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="622ce-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="622ce-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="622ce-108">Служит интерфейсом для виртуального сетевого адаптера (NIC).</span><span class="sxs-lookup"><span data-stu-id="622ce-108">Serves as the interface to a virtual network interface card (NIC).</span></span> <span data-ttu-id="622ce-109">Он используется для настройки того, как виртуальная машина находится в сети.</span><span class="sxs-lookup"><span data-stu-id="622ce-109">It is used to set up how a virtual machine is networked.</span></span> <span data-ttu-id="622ce-110">Сетевые карты можно добавлять и удалять с помощью [**ивмвиртуалмачине:: адднетворкадаптер**](ivmvirtualmachine-addnetworkadapter.md) и [**Ивмвиртуалмачине:: ремовенетворкадаптер**](ivmvirtualmachine-removenetworkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="622ce-110">Network interface cards can be added and removed by using [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) and [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span></span> <span data-ttu-id="622ce-111">Можно также получить объект **ивмнетворкадаптер** из коллекции [**ивмнетворкадаптерколлектион**](ivmnetworkadaptercollection.md) , возвращенной из свойств [**Ивмвиртуалмачине:: адаптера**](ivmvirtualmachine-networkadapters.md) или [**ивмвиртуалнетворк:: адаптера**](ivmvirtualnetwork-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="622ce-111">You can also retrieve an **IVMNetworkAdapter** object from the [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) collection returned from the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) or [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="622ce-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="622ce-112">Members</span></span>

<span data-ttu-id="622ce-113">Интерфейс **ивмнетворкадаптер** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="622ce-113">The **IVMNetworkAdapter** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="622ce-114">**Ивмнетворкадаптер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="622ce-114">**IVMNetworkAdapter** also has these types of members:</span></span>

-   [<span data-ttu-id="622ce-115">Методы</span><span class="sxs-lookup"><span data-stu-id="622ce-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="622ce-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="622ce-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="622ce-117">Методы</span><span class="sxs-lookup"><span data-stu-id="622ce-117">Methods</span></span>

<span data-ttu-id="622ce-118">Интерфейс **ивмнетворкадаптер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="622ce-118">The **IVMNetworkAdapter** interface has these methods.</span></span>



| <span data-ttu-id="622ce-119">Метод</span><span class="sxs-lookup"><span data-stu-id="622ce-119">Method</span></span>                                                                         | <span data-ttu-id="622ce-120">Описание</span><span class="sxs-lookup"><span data-stu-id="622ce-120">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="622ce-121">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="622ce-121">**\_ID**</span></span>](ivmnetworkadapter--id.md)                                          | <span data-ttu-id="622ce-122">Извлекает внутренний идентификатор этого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="622ce-122">Retrieves the internal identifier of this network interface.</span></span><br/>     |
| [<span data-ttu-id="622ce-123">**аттачтовиртуалнетворк**</span><span class="sxs-lookup"><span data-stu-id="622ce-123">**AttachToVirtualNetwork**</span></span>](ivmnetworkadapter-attachtovirtualnetwork.md)     | <span data-ttu-id="622ce-124">Подключает сетевой интерфейс к указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="622ce-124">Attaches the network interface to the specified virtual network.</span></span><br/> |
| [<span data-ttu-id="622ce-125">**детачфромвиртуалнетворк**</span><span class="sxs-lookup"><span data-stu-id="622ce-125">**DetachFromVirtualNetwork**</span></span>](ivmnetworkadapter-detachfromvirtualnetwork.md) | <span data-ttu-id="622ce-126">Отключает сетевой интерфейс от своей виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="622ce-126">Detaches the network interface from its virtual network.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="622ce-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="622ce-127">Properties</span></span>

<span data-ttu-id="622ce-128">Интерфейс **ивмнетворкадаптер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="622ce-128">The **IVMNetworkAdapter** interface has these properties.</span></span>



| <span data-ttu-id="622ce-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="622ce-129">Property</span></span>                                                                                  | <span data-ttu-id="622ce-130">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="622ce-130">Access type</span></span>           | <span data-ttu-id="622ce-131">Описание</span><span class="sxs-lookup"><span data-stu-id="622ce-131">Description</span></span>                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="622ce-132">**есернетаддресс**</span><span class="sxs-lookup"><span data-stu-id="622ce-132">**EthernetAddress**</span></span>](ivmnetworkadapter-ethernetaddress.md)<br/>                   | <span data-ttu-id="622ce-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="622ce-133">Read/write</span></span><br/> | <span data-ttu-id="622ce-134">Адрес Ethernet (MAC) сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="622ce-134">The Ethernet (MAC) address of the network interface.</span></span><br/>             |
| [<span data-ttu-id="622ce-135">**исесернетаддрессдинамик**</span><span class="sxs-lookup"><span data-stu-id="622ce-135">**IsEthernetAddressDynamic**</span></span>](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | <span data-ttu-id="622ce-136">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="622ce-136">Read/write</span></span><br/> | <span data-ttu-id="622ce-137">Указывает, создается ли адрес Ethernet динамически.</span><span class="sxs-lookup"><span data-stu-id="622ce-137">Indicates whether the Ethernet address is dynamically generated.</span></span><br/> |
| [<span data-ttu-id="622ce-138">**VirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="622ce-138">**VirtualMachine**</span></span>](ivmnetworkadapter-virtualmachine.md)<br/>                     | <span data-ttu-id="622ce-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="622ce-139">Read-only</span></span><br/>  | <span data-ttu-id="622ce-140">Виртуальная машина, связанная с этим сетевым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="622ce-140">The virtual machine associated with this network interface.</span></span><br/>      |
| [<span data-ttu-id="622ce-141">**VirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="622ce-141">**VirtualNetwork**</span></span>](ivmnetworkadapter-virtualnetwork.md)<br/>                     | <span data-ttu-id="622ce-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="622ce-142">Read-only</span></span><br/>  | <span data-ttu-id="622ce-143">Виртуальная сеть, к которой подключен сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="622ce-143">The virtual network to which the network interface is attached.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="622ce-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="622ce-144">Remarks</span></span>

<span data-ttu-id="622ce-145">Адресом Ethernet по умолчанию для сетевого интерфейса является "00-00-00-00-00-00", что в большинстве операционных систем считается недопустимым адресом Ethernet.</span><span class="sxs-lookup"><span data-stu-id="622ce-145">The default Ethernet address for a network interface is "00-00-00-00-00-00", which is considered an invalid Ethernet address by most operating systems.</span></span> <span data-ttu-id="622ce-146">Если для [**исесернетаддрессдинамик**](ivmnetworkadapter-isethernetaddressdynamic.md) задано **значение false**, то [**есернетаддресс**](ivmnetworkadapter-ethernetaddress.md) должен быть инициализирован с допустимым сетевым адресом Ethernet.</span><span class="sxs-lookup"><span data-stu-id="622ce-146">If [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) is set to **FALSE**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) must be initialized with a valid Ethernet network address.</span></span>

<span data-ttu-id="622ce-147">В следующих процедурах объясняется, как использовать интерфейс **ивмнетворкадаптер** .</span><span class="sxs-lookup"><span data-stu-id="622ce-147">The following procedures explain how to use the **IVMNetworkAdapter** interface.</span></span>

<span data-ttu-id="622ce-148">**Подключение виртуального сетевого адаптера к сетевому адаптеру узла**</span><span class="sxs-lookup"><span data-stu-id="622ce-148">**To attach a virtual NIC to a host NIC**</span></span>

-   <span data-ttu-id="622ce-149">Виртуальные сетевые карты не подключены напрямую к сетевому адаптеру узла.</span><span class="sxs-lookup"><span data-stu-id="622ce-149">Virtual (guest) NICs are not attached directly to a host NIC.</span></span> <span data-ttu-id="622ce-150">Вместо этого виртуальный сетевой адаптер подключен к виртуальной сети, подключенной к сетевому адаптеру узла.</span><span class="sxs-lookup"><span data-stu-id="622ce-150">Instead, the virtual NIC is attached to a virtual network that is attached to a host NIC.</span></span> <span data-ttu-id="622ce-151">Дополнительные сведения о настройке виртуальных сетей см. в разделе [**ивмвиртуалнетворк**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="622ce-151">For more information about configuring virtual networks, see [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span> <span data-ttu-id="622ce-152">Чтобы подключить виртуальный сетевой адаптер к виртуальной сети, используйте метод [**аттачтовиртуалнетворк**](ivmnetworkadapter-attachtovirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="622ce-152">To attach the virtual NIC to a virtual network, use the [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) method.</span></span>

<span data-ttu-id="622ce-153">**Отключение виртуального сетевого адаптера от виртуальной сети**</span><span class="sxs-lookup"><span data-stu-id="622ce-153">**To disconnect a virtual NIC from the virtual network**</span></span>

-   <span data-ttu-id="622ce-154">Метод [**детачфромвиртуалнетворк**](ivmnetworkadapter-detachfromvirtualnetwork.md) отключит виртуальный сетевой адаптер от виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="622ce-154">The [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) method will detach the virtual NIC from the virtual network.</span></span> <span data-ttu-id="622ce-155">После вызова этой функции свойство [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) вернет недопустимый идентификатор виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="622ce-155">After this function is called, the [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) property will return a virtual network ID that is not valid.</span></span>

<span data-ttu-id="622ce-156">**Удаление виртуального сетевого адаптера из виртуальной машины при наличии объекта виртуального сетевого адаптера**</span><span class="sxs-lookup"><span data-stu-id="622ce-156">**To remove a virtual NIC from a virtual machine if you have the virtual NIC object**</span></span>

1.  <span data-ttu-id="622ce-157">Получите виртуальную машину, связанную с виртуальным сетевым адаптером, с помощью свойства [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="622ce-157">Get the virtual machine associated with the virtual NIC by using the [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) property.</span></span>
2.  <span data-ttu-id="622ce-158">Используйте текущий объект в качестве параметра для метода [**ивмвиртуалмачине:: ремовенетворкадаптер**](ivmvirtualmachine-removenetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="622ce-158">Use the current object as a parameter to the [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="622ce-159">Требования</span><span class="sxs-lookup"><span data-stu-id="622ce-159">Requirements</span></span>



| <span data-ttu-id="622ce-160">Требование</span><span class="sxs-lookup"><span data-stu-id="622ce-160">Requirement</span></span> | <span data-ttu-id="622ce-161">Значение</span><span class="sxs-lookup"><span data-stu-id="622ce-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ce-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="622ce-162">Minimum supported client</span></span><br/> | <span data-ttu-id="622ce-163">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="622ce-163">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="622ce-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="622ce-164">Minimum supported server</span></span><br/> | <span data-ttu-id="622ce-165">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="622ce-165">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="622ce-166">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="622ce-166">End of client support</span></span><br/>    | <span data-ttu-id="622ce-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="622ce-167">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="622ce-168">Продукт</span><span class="sxs-lookup"><span data-stu-id="622ce-168">Product</span></span><br/>                  | <span data-ttu-id="622ce-169">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="622ce-169">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="622ce-170">Header</span><span class="sxs-lookup"><span data-stu-id="622ce-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="622ce-171"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="622ce-171"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="622ce-172">IID</span><span class="sxs-lookup"><span data-stu-id="622ce-172">IID</span></span><br/>                      | <span data-ttu-id="622ce-173">IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="622ce-173">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



 

