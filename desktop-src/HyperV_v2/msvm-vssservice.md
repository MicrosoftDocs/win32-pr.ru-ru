---
description: Представляет гостевую службу VSS. Он используется для запроса данных гостевого кластера с узла Hyper-V.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Класс Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342772"
---
# <a name="msvm_vssservice-class"></a><span data-ttu-id="5ad78-104">\_Класс мсвм всссервице</span><span class="sxs-lookup"><span data-stu-id="5ad78-104">Msvm\_VssService class</span></span>

<span data-ttu-id="5ad78-105">Представляет гостевую службу VSS.</span><span class="sxs-lookup"><span data-stu-id="5ad78-105">Represents the guest VSS service.</span></span> <span data-ttu-id="5ad78-106">Он используется для запроса данных гостевого кластера с узла Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="5ad78-106">It is used for querying guest cluster information from the Hyper-V host.</span></span>

<span data-ttu-id="5ad78-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5ad78-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad78-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ad78-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a><span data-ttu-id="5ad78-109">Члены</span><span class="sxs-lookup"><span data-stu-id="5ad78-109">Members</span></span>

<span data-ttu-id="5ad78-110">Класс **мсвм \_ всссервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5ad78-110">The **Msvm\_VssService** class has these types of members:</span></span>

-   [<span data-ttu-id="5ad78-111">Методы</span><span class="sxs-lookup"><span data-stu-id="5ad78-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5ad78-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5ad78-112">Methods</span></span>

<span data-ttu-id="5ad78-113">Класс **мсвм \_ всссервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5ad78-113">The **Msvm\_VssService** class has these methods.</span></span>



| <span data-ttu-id="5ad78-114">Метод</span><span class="sxs-lookup"><span data-stu-id="5ad78-114">Method</span></span>                                                                               | <span data-ttu-id="5ad78-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5ad78-115">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="5ad78-116">**куеригуестклустеринформатион**</span><span class="sxs-lookup"><span data-stu-id="5ad78-116">**QueryGuestClusterInformation**</span></span>](msvm-vssservice-queryguestclusterinformation.md) | <span data-ttu-id="5ad78-117">Запрос сведений о кластере от узла Hyper-V к гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="5ad78-117">Querying cluster information from the Hyper-V host to the guest.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5ad78-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5ad78-118">Requirements</span></span>



| <span data-ttu-id="5ad78-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5ad78-119">Requirement</span></span> | <span data-ttu-id="5ad78-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5ad78-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad78-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ad78-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5ad78-122">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5ad78-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5ad78-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ad78-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5ad78-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5ad78-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5ad78-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5ad78-125">Namespace</span></span><br/>                | <span data-ttu-id="5ad78-126">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5ad78-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ad78-127">MOF</span><span class="sxs-lookup"><span data-stu-id="5ad78-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ad78-128"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ad78-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ad78-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5ad78-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ad78-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ad78-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ad78-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ad78-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad78-132">**Мсвм \_ гуестсервице**</span><span class="sxs-lookup"><span data-stu-id="5ad78-132">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




