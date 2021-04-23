---
description: Управляет назначаемыми устройствами на компьютере узла.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Класс Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684633"
---
# <a name="msvm_assignabledeviceservice-class"></a><span data-ttu-id="cc718-103">\_Класс мсвм ассигнабледевицесервице</span><span class="sxs-lookup"><span data-stu-id="cc718-103">Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="cc718-104">Управляет назначаемыми устройствами на компьютере узла.</span><span class="sxs-lookup"><span data-stu-id="cc718-104">Manages the assignable devices on a host computer system.</span></span>

<span data-ttu-id="cc718-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cc718-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc718-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc718-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="cc718-107">Члены</span><span class="sxs-lookup"><span data-stu-id="cc718-107">Members</span></span>

<span data-ttu-id="cc718-108">Класс **мсвм \_ ассигнабледевицесервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cc718-108">The **Msvm\_AssignableDeviceService** class has these types of members:</span></span>

-   [<span data-ttu-id="cc718-109">Методы</span><span class="sxs-lookup"><span data-stu-id="cc718-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cc718-110">Методы</span><span class="sxs-lookup"><span data-stu-id="cc718-110">Methods</span></span>

<span data-ttu-id="cc718-111">Класс **мсвм \_ ассигнабледевицесервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cc718-111">The **Msvm\_AssignableDeviceService** class has these methods.</span></span>



| <span data-ttu-id="cc718-112">Метод</span><span class="sxs-lookup"><span data-stu-id="cc718-112">Method</span></span>                                                                                    | <span data-ttu-id="cc718-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cc718-113">Description</span></span>                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc718-114">**дисмаунтассигнабледевице**</span><span class="sxs-lookup"><span data-stu-id="cc718-114">**DismountAssignableDevice**</span></span>](msvm-assignabledeviceservice-dismountassignabledevice.md) | <span data-ttu-id="cc718-115">Отключает указанное устройство PCI, чтобы его можно было назначить.</span><span class="sxs-lookup"><span data-stu-id="cc718-115">Dismounts the specified PCI device so that it can be assigned.</span></span><br/>                      |
| [<span data-ttu-id="cc718-116">**маунтассигнабледевице**</span><span class="sxs-lookup"><span data-stu-id="cc718-116">**MountAssignableDevice**</span></span>](msvm-assignabledeviceservice-mountassignabledevice.md)       | <span data-ttu-id="cc718-117">Подключает указанное устройство PCI, чтобы его можно было использовать в системе главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="cc718-117">Mounts the specified PCI device so that it can be used by the host computer system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cc718-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cc718-118">Requirements</span></span>



| <span data-ttu-id="cc718-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cc718-119">Requirement</span></span> | <span data-ttu-id="cc718-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cc718-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc718-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc718-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc718-122">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="cc718-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cc718-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc718-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc718-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cc718-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cc718-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cc718-125">Namespace</span></span><br/>                | <span data-ttu-id="cc718-126">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cc718-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cc718-127">MOF</span><span class="sxs-lookup"><span data-stu-id="cc718-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc718-128"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc718-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc718-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cc718-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc718-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cc718-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cc718-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc718-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc718-132">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="cc718-132">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




