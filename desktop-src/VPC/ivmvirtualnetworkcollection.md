---
title: Интерфейс Ивмвиртуалнетворкколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию объектов Ивмвиртуалнетворк. Чтобы получить объект Ивмвиртуалнетворкколлектион, используйте свойство VirtualNetworks Ивмвиртуалпк.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Виртуальный ПК с интерфейсом Ивмвиртуалнетворкколлектион
- Ивмвиртуалнетворкколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803461"
---
# <a name="ivmvirtualnetworkcollection-interface"></a><span data-ttu-id="63593-106">Интерфейс Ивмвиртуалнетворкколлектион</span><span class="sxs-lookup"><span data-stu-id="63593-106">IVMVirtualNetworkCollection interface</span></span>

<span data-ttu-id="63593-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63593-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63593-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63593-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63593-109">Определяет коллекцию объектов [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="63593-109">Defines a collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="63593-110">Чтобы получить объект **ивмвиртуалнетворкколлектион** , используйте свойство [**Ивмвиртуалпк:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="63593-110">To obtain an **IVMVirtualNetworkCollection** object, use the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="63593-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="63593-111">Members</span></span>

<span data-ttu-id="63593-112">Интерфейс **ивмвиртуалнетворкколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="63593-112">The **IVMVirtualNetworkCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="63593-113">**Ивмвиртуалнетворкколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="63593-113">**IVMVirtualNetworkCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="63593-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="63593-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63593-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="63593-115">Properties</span></span>

<span data-ttu-id="63593-116">Интерфейс **ивмвиртуалнетворкколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="63593-116">The **IVMVirtualNetworkCollection** interface has these properties.</span></span>



| <span data-ttu-id="63593-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="63593-117">Property</span></span>                                                             | <span data-ttu-id="63593-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="63593-118">Access type</span></span>          | <span data-ttu-id="63593-119">Описание</span><span class="sxs-lookup"><span data-stu-id="63593-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63593-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="63593-120">**\_NewEnum**</span></span>](ivmvirtualnetworkcollection--newenum.md)<br/> | <span data-ttu-id="63593-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="63593-121">Read-only</span></span><br/> | <span data-ttu-id="63593-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="63593-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="63593-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="63593-123">**Count**</span></span>](ivmvirtualnetworkcollection-count.md)<br/>        | <span data-ttu-id="63593-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="63593-124">Read-only</span></span><br/> | <span data-ttu-id="63593-125">Число виртуальных сетей в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="63593-125">The number of virtual networks in this collection.</span></span><br/>                                                 |
| [<span data-ttu-id="63593-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="63593-126">**Item**</span></span>](ivmvirtualnetworkcollection-item.md)<br/>          | <span data-ttu-id="63593-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="63593-127">Read-only</span></span><br/> | <span data-ttu-id="63593-128">Объект [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) , соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="63593-128">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="63593-129">Требования</span><span class="sxs-lookup"><span data-stu-id="63593-129">Requirements</span></span>



| <span data-ttu-id="63593-130">Требование</span><span class="sxs-lookup"><span data-stu-id="63593-130">Requirement</span></span> | <span data-ttu-id="63593-131">Значение</span><span class="sxs-lookup"><span data-stu-id="63593-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63593-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63593-132">Minimum supported client</span></span><br/> | <span data-ttu-id="63593-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63593-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63593-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63593-134">Minimum supported server</span></span><br/> | <span data-ttu-id="63593-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="63593-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="63593-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="63593-136">End of client support</span></span><br/>    | <span data-ttu-id="63593-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63593-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="63593-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="63593-138">Product</span></span><br/>                  | <span data-ttu-id="63593-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63593-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="63593-140">Header</span><span class="sxs-lookup"><span data-stu-id="63593-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="63593-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="63593-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="63593-142">IID</span><span class="sxs-lookup"><span data-stu-id="63593-142">IID</span></span><br/>                      | <span data-ttu-id="63593-143">IID \_ ивмвиртуалнетворкколлектион определен как 8ed680be-4242-4b2a-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="63593-143">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



 

