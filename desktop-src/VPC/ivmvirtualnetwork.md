---
title: Интерфейс Ивмвиртуалнетворк (Впккоминтерфацес. h)
description: Определяет виртуальную сеть.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Виртуальный ПК с интерфейсом Ивмвиртуалнетворк
- Ивмвиртуалнетворк интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691940"
---
# <a name="ivmvirtualnetwork-interface"></a><span data-ttu-id="10ede-105">Интерфейс Ивмвиртуалнетворк</span><span class="sxs-lookup"><span data-stu-id="10ede-105">IVMVirtualNetwork interface</span></span>

<span data-ttu-id="10ede-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="10ede-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="10ede-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="10ede-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="10ede-108">Определяет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="10ede-108">Defines a virtual network.</span></span> <span data-ttu-id="10ede-109">Объекты **ивмвиртуалнетворк** возвращаются из метода [**ивмвиртуалпк**](ivmvirtualpc.md) [**финдвиртуалнетворк**](ivmvirtualpc-findvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="10ede-109">**IVMVirtualNetwork** objects are returned from [**IVMVirtualPC**](ivmvirtualpc.md) method [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span></span> <span data-ttu-id="10ede-110">Можно также получить объект **ивмвиртуалнетворк** из объекта [**ивмвиртуалнетворкколлектион**](ivmvirtualnetworkcollection.md) , возвращенного из свойства [**ивмвиртуалпк:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="10ede-110">You can also retrieve an **IVMVirtualNetwork** object from the [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) object returned from the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

<span data-ttu-id="10ede-111">Виртуальная сеть состоит из виртуального коммутатора, который выполняет всю внутреннюю маршрутизацию и несколько соединений, подключенных к виртуальному коммутатору.</span><span class="sxs-lookup"><span data-stu-id="10ede-111">A virtual network consists of a virtual switch, which performs all internal routing, and several connections that are "plugged in" to the virtual switch.</span></span> <span data-ttu-id="10ede-112">Эти подключения могут быть реальным подключением к внешнему узлу, внутренней сетью или общей сетью (NAT).</span><span class="sxs-lookup"><span data-stu-id="10ede-112">These connections can be a real external host connection, an "internal network" or shared networking (NAT).</span></span>

## <a name="members"></a><span data-ttu-id="10ede-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="10ede-113">Members</span></span>

<span data-ttu-id="10ede-114">Интерфейс **ивмвиртуалнетворк** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="10ede-114">The **IVMVirtualNetwork** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="10ede-115">**Ивмвиртуалнетворк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="10ede-115">**IVMVirtualNetwork** also has these types of members:</span></span>

-   [<span data-ttu-id="10ede-116">Методы</span><span class="sxs-lookup"><span data-stu-id="10ede-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="10ede-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="10ede-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10ede-118">Методы</span><span class="sxs-lookup"><span data-stu-id="10ede-118">Methods</span></span>

<span data-ttu-id="10ede-119">Интерфейс **ивмвиртуалнетворк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="10ede-119">The **IVMVirtualNetwork** interface has these methods.</span></span>



| <span data-ttu-id="10ede-120">Метод</span><span class="sxs-lookup"><span data-stu-id="10ede-120">Method</span></span>                                | <span data-ttu-id="10ede-121">Описание</span><span class="sxs-lookup"><span data-stu-id="10ede-121">Description</span></span>                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="10ede-122">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="10ede-122">**\_ID**</span></span>](ivmvirtualnetwork--id.md) | <span data-ttu-id="10ede-123">Извлекает внутренний идентификатор виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="10ede-123">Retrieves the internal identifier of the virtual network.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="10ede-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="10ede-124">Properties</span></span>

<span data-ttu-id="10ede-125">Интерфейс **ивмвиртуалнетворк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="10ede-125">The **IVMVirtualNetwork** interface has these properties.</span></span>



| <span data-ttu-id="10ede-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="10ede-126">Property</span></span>                                                                | <span data-ttu-id="10ede-127">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="10ede-127">Access type</span></span>          | <span data-ttu-id="10ede-128">Описание</span><span class="sxs-lookup"><span data-stu-id="10ede-128">Description</span></span>                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="10ede-129">**хостадаптер**</span><span class="sxs-lookup"><span data-stu-id="10ede-129">**HostAdapter**</span></span>](ivmvirtualnetwork-hostadapter.md)<br/>         | <span data-ttu-id="10ede-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="10ede-130">Read-only</span></span><br/> | <span data-ttu-id="10ede-131">Имя адаптера, к которому подключена виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="10ede-131">The name of the adapter to which the virtual network is connected.</span></span><br/>  |
| <span data-ttu-id="10ede-132">[**Мультимедиа**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10ede-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span></span><br/>             | <span data-ttu-id="10ede-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="10ede-133">Read-only</span></span><br/> | <span data-ttu-id="10ede-134">Определяет, является ли экземпляр виртуальной сети беспроводным.</span><span class="sxs-lookup"><span data-stu-id="10ede-134">Determines whether the virtual network instance is wireless or not.</span></span><br/> |
| [<span data-ttu-id="10ede-135">**Имя**</span><span class="sxs-lookup"><span data-stu-id="10ede-135">**Name**</span></span>](ivmvirtualnetwork-name.md)<br/>                       | <span data-ttu-id="10ede-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="10ede-136">Read-only</span></span><br/> | <span data-ttu-id="10ede-137">Уникальное имя экземпляра виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="10ede-137">The unique name of the virtual network instance.</span></span><br/>                    |
| [<span data-ttu-id="10ede-138">**Адаптера**</span><span class="sxs-lookup"><span data-stu-id="10ede-138">**NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)<br/> | <span data-ttu-id="10ede-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="10ede-139">Read-only</span></span><br/> | <span data-ttu-id="10ede-140">Перечисляемая коллекция сетевых адаптеров, подключенных к виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="10ede-140">An enumerable collection of NICs attached to the virtual network.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="10ede-141">Требования</span><span class="sxs-lookup"><span data-stu-id="10ede-141">Requirements</span></span>



| <span data-ttu-id="10ede-142">Требование</span><span class="sxs-lookup"><span data-stu-id="10ede-142">Requirement</span></span> | <span data-ttu-id="10ede-143">Значение</span><span class="sxs-lookup"><span data-stu-id="10ede-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ede-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10ede-144">Minimum supported client</span></span><br/> | <span data-ttu-id="10ede-145">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="10ede-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10ede-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10ede-146">Minimum supported server</span></span><br/> | <span data-ttu-id="10ede-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="10ede-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="10ede-148">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="10ede-148">End of client support</span></span><br/>    | <span data-ttu-id="10ede-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10ede-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="10ede-150">Продукт</span><span class="sxs-lookup"><span data-stu-id="10ede-150">Product</span></span><br/>                  | <span data-ttu-id="10ede-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="10ede-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="10ede-152">Header</span><span class="sxs-lookup"><span data-stu-id="10ede-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="10ede-153"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="10ede-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="10ede-154">IID</span><span class="sxs-lookup"><span data-stu-id="10ede-154">IID</span></span><br/>                      | <span data-ttu-id="10ede-155">IID \_ ивмвиртуалнетворк определен как 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="10ede-155">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



 

