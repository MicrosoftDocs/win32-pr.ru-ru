---
description: Сообщает о состоянии работоспособности приложения, которое выполняется на виртуальной машине, с компонентами интеграции Hyper-V, работающими на той же виртуальной машине.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Интерфейс Ивмаппликатионхеалсмонитор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683100"
---
# <a name="ivmapplicationhealthmonitor-interface"></a><span data-ttu-id="e6b25-103">Интерфейс Ивмаппликатионхеалсмонитор</span><span class="sxs-lookup"><span data-stu-id="e6b25-103">IVmApplicationHealthMonitor interface</span></span>

<span data-ttu-id="e6b25-104">Сообщает о состоянии работоспособности приложения, которое выполняется на виртуальной машине, с компонентами интеграции Hyper-V, работающими на той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e6b25-104">Reports the health status of an application that is running in a virtual machine to the Hyper-V integration components running in the same virtual machine.</span></span> <span data-ttu-id="e6b25-105">Состояние приложений, выполняющихся на виртуальной машине, отражается в  \[ \] значении свойства OperationalStatus 1 класса [**мсвм \_ хеартбеаткомпонент**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="e6b25-105">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span> <span data-ttu-id="e6b25-106">Этот интерфейс также предоставляет способ сброса всех состояний приложений, накопленных в Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e6b25-106">This interface also provides a way to reset all of the application state accumulated in Hyper-V.</span></span>

<span data-ttu-id="e6b25-107">Этот интерфейс реализуется компонентами интеграции Windows 8 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e6b25-107">This interface is implemented by the Windows 8 Hyper-V integration components.</span></span> <span data-ttu-id="e6b25-108">Экземпляр этого интерфейса получается путем создания экземпляра CLSID **397a2e5f-348c-482d-b9a3-57d383b483cd** .</span><span class="sxs-lookup"><span data-stu-id="e6b25-108">An instance of this interface is obtained by creating an instance of the **397a2e5f-348c-482d-b9a3-57d383b483cd** CLSID.</span></span>

## <a name="members"></a><span data-ttu-id="e6b25-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="e6b25-109">Members</span></span>

<span data-ttu-id="e6b25-110">Интерфейс **ивмаппликатионхеалсмонитор** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e6b25-110">The **IVmApplicationHealthMonitor** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e6b25-111">**Ивмаппликатионхеалсмонитор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e6b25-111">**IVmApplicationHealthMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="e6b25-112">Методы</span><span class="sxs-lookup"><span data-stu-id="e6b25-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e6b25-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e6b25-113">Methods</span></span>

<span data-ttu-id="e6b25-114">Интерфейс **ивмаппликатионхеалсмонитор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e6b25-114">The **IVmApplicationHealthMonitor** interface has these methods.</span></span>



| <span data-ttu-id="e6b25-115">Метод</span><span class="sxs-lookup"><span data-stu-id="e6b25-115">Method</span></span>                                                                                   | <span data-ttu-id="e6b25-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e6b25-116">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6b25-117">**ресеталлаппликатионстате**</span><span class="sxs-lookup"><span data-stu-id="e6b25-117">**ResetAllApplicationState**</span></span>](ivmapplicationhealthmonitor-resetallapplicationstate.md) | <span data-ttu-id="e6b25-118">Сбрасывает состояние работоспособности для всех приложений в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e6b25-118">Resets the health state for all applications in a virtual machine.</span></span><br/>            |
| [<span data-ttu-id="e6b25-119">**сетаппликатионстате**</span><span class="sxs-lookup"><span data-stu-id="e6b25-119">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)           | <span data-ttu-id="e6b25-120">Задает состояние работоспособности приложения, которое выполняется на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e6b25-120">Sets the health state of an application that is running in a virtual machine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6b25-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6b25-121">Remarks</span></span>

<span data-ttu-id="e6b25-122">Чтобы использовать этот программный элемент, на виртуальной машине, в которой выполняется приложение, должны быть установлены компоненты интеграции Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6b25-122">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b25-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e6b25-123">Requirements</span></span>



| <span data-ttu-id="e6b25-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e6b25-124">Requirement</span></span> | <span data-ttu-id="e6b25-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e6b25-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b25-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6b25-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e6b25-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e6b25-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="e6b25-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6b25-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e6b25-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e6b25-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                           |
| <span data-ttu-id="e6b25-130">Версия</span><span class="sxs-lookup"><span data-stu-id="e6b25-130">Version</span></span><br/>                  | <span data-ttu-id="e6b25-131">Компоненты интеграции для Windows 8</span><span class="sxs-lookup"><span data-stu-id="e6b25-131">Integration components for Windows 8</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e6b25-132">IDL</span><span class="sxs-lookup"><span data-stu-id="e6b25-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6b25-133"><dt>Вмаппликатионхеалсмонитор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6b25-133"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e6b25-134">IID</span><span class="sxs-lookup"><span data-stu-id="e6b25-134">IID</span></span><br/>                      | <span data-ttu-id="e6b25-135">IID \_ ивмаппликатионхеалсмонитор определен как 267a0284-848f-447e-a096-5e10a1a76bca</span><span class="sxs-lookup"><span data-stu-id="e6b25-135">IID\_IVmApplicationHealthMonitor is defined as 267a0284-848f-447e-a096-5e10a1a76bca</span></span><br/> <span data-ttu-id="e6b25-136">Идентификатор объекта определен как 397a2e5f-348c-482d-b9a3-57d383b483cd</span><span class="sxs-lookup"><span data-stu-id="e6b25-136">Object Identifier is defined as 397a2e5f-348c-482d-b9a3-57d383b483cd</span></span><br/> |



 

