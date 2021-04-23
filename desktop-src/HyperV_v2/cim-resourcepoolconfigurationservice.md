---
description: Управляет конфигурацией пулов ресурсов с помощью заданий.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: Класс CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897633"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="d0ac5-103">\_Класс CIM ресаурцепулконфигуратионсервице</span><span class="sxs-lookup"><span data-stu-id="d0ac5-103">CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="d0ac5-104">Управляет конфигурацией пулов ресурсов с помощью заданий.</span><span class="sxs-lookup"><span data-stu-id="d0ac5-104">Manages the configuration of resource pools by using jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ac5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0ac5-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="d0ac5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d0ac5-106">Members</span></span>

<span data-ttu-id="d0ac5-107">Класс **CIM \_ ресаурцепулконфигуратионсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d0ac5-107">The **CIM\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="d0ac5-108">Методы</span><span class="sxs-lookup"><span data-stu-id="d0ac5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d0ac5-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d0ac5-109">Methods</span></span>

<span data-ttu-id="d0ac5-110">Класс **CIM \_ ресаурцепулконфигуратионсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d0ac5-110">The **CIM\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="d0ac5-111">Метод</span><span class="sxs-lookup"><span data-stu-id="d0ac5-111">Method</span></span>                                                                                                          | <span data-ttu-id="d0ac5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d0ac5-112">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="d0ac5-113">**аддресаурцесторесаурцепул**</span><span class="sxs-lookup"><span data-stu-id="d0ac5-113">**AddResourcesToResourcePool**</span></span>](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | <span data-ttu-id="d0ac5-114">Запускает задание по добавлению ресурсов в пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0ac5-114">Starts a job to add resources to a resource pool.</span></span><br/>                  |
| [<span data-ttu-id="d0ac5-115">**чанжепарентресаурцепул**</span><span class="sxs-lookup"><span data-stu-id="d0ac5-115">**ChangeParentResourcePool**</span></span>](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | <span data-ttu-id="d0ac5-116">Запустите задание, чтобы изменить родительский пул ресурсов пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0ac5-116">Start a job to change the parent resource pool of a resource pool.</span></span><br/> |
| [<span data-ttu-id="d0ac5-117">**креатечилдресаурцепул**</span><span class="sxs-lookup"><span data-stu-id="d0ac5-117">**CreateChildResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | <span data-ttu-id="d0ac5-118">Запустите задание, чтобы создать пул ресурсов из родительского пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0ac5-118">Start a job to create a resource pool from a parent resource pool.</span></span><br/> |
| [<span data-ttu-id="d0ac5-119">**CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="d0ac5-119">**CreateResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | <span data-ttu-id="d0ac5-120">Запускает задание для создания пула корневых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0ac5-120">Starts a job to create a root resource pool.</span></span><br/>                       |
| [<span data-ttu-id="d0ac5-121">**делетересаурцепул**</span><span class="sxs-lookup"><span data-stu-id="d0ac5-121">**DeleteResourcePool**</span></span>](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | <span data-ttu-id="d0ac5-122">Запуск задания для удаления пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0ac5-122">Start a job to delete a resource pool.</span></span><br/>                             |
| [<span data-ttu-id="d0ac5-123">**ремовересаурцесфромресаурцепул**</span><span class="sxs-lookup"><span data-stu-id="d0ac5-123">**RemoveResourcesFromResourcePool**</span></span>](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | <span data-ttu-id="d0ac5-124">Запускает задание по удалению ресурсов из пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0ac5-124">Starts a job to remove resources from a resource pool.</span></span><br/>             |



 

## <a name="requirements"></a><span data-ttu-id="d0ac5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d0ac5-125">Requirements</span></span>



| <span data-ttu-id="d0ac5-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d0ac5-126">Requirement</span></span> | <span data-ttu-id="d0ac5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d0ac5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ac5-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0ac5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ac5-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d0ac5-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d0ac5-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0ac5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ac5-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d0ac5-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d0ac5-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d0ac5-132">Namespace</span></span><br/>                | <span data-ttu-id="d0ac5-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d0ac5-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d0ac5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d0ac5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0ac5-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0ac5-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0ac5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d0ac5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0ac5-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d0ac5-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d0ac5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0ac5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ac5-139">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="d0ac5-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




