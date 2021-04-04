---
description: Представляет службу безопасности. Он используется для настройки параметров безопасности виртуальной системы.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Класс Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998637"
---
# <a name="msvm_securityservice-class"></a><span data-ttu-id="b4e92-104">\_Класс мсвм SecurityService</span><span class="sxs-lookup"><span data-stu-id="b4e92-104">Msvm\_SecurityService class</span></span>

<span data-ttu-id="b4e92-105">Представляет службу безопасности.</span><span class="sxs-lookup"><span data-stu-id="b4e92-105">Represents the security service.</span></span> <span data-ttu-id="b4e92-106">Он используется для настройки параметров безопасности виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="b4e92-106">It is used for configuring virtual system security settings.</span></span>

<span data-ttu-id="b4e92-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b4e92-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e92-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4e92-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="b4e92-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b4e92-109">Members</span></span>

<span data-ttu-id="b4e92-110">Класс **мсвм \_ SecurityService** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b4e92-110">The **Msvm\_SecurityService** class has these types of members:</span></span>

-   [<span data-ttu-id="b4e92-111">Методы</span><span class="sxs-lookup"><span data-stu-id="b4e92-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b4e92-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b4e92-112">Methods</span></span>

<span data-ttu-id="b4e92-113">Класс **мсвм \_ SecurityService** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b4e92-113">The **Msvm\_SecurityService** class has these methods.</span></span>



| <span data-ttu-id="b4e92-114">Метод</span><span class="sxs-lookup"><span data-stu-id="b4e92-114">Method</span></span>                                                                                            | <span data-ttu-id="b4e92-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b4e92-115">Description</span></span>                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="b4e92-116">**жеткэйпротектор**</span><span class="sxs-lookup"><span data-stu-id="b4e92-116">**GetKeyProtector**</span></span>](msvm-securityservice-getkeyprotector.md)                                   | <span data-ttu-id="b4e92-117">Метод для получения предохранителя ключа для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="b4e92-117">Method to retrieve the key protector for a virtual system.</span></span><br/>   |
| [<span data-ttu-id="b4e92-118">**модифисекуритисеттингс**</span><span class="sxs-lookup"><span data-stu-id="b4e92-118">**ModifySecuritySettings**</span></span>](msvm-securityservice-modifysecuritysettings.md)                     | <span data-ttu-id="b4e92-119">Изменяет текущие параметры безопасности виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b4e92-119">Modifies the current security settings of a virtual machine.</span></span><br/> |
| [<span data-ttu-id="b4e92-120">**рестореласткновнгудкэйпротектор**</span><span class="sxs-lookup"><span data-stu-id="b4e92-120">**RestoreLastKnownGoodKeyProtector**</span></span>](msvm-securityservice-restorelastknowngoodkeyprotector.md) | <span data-ttu-id="b4e92-121">Метод восстановления до последнего известного предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="b4e92-121">Method to restore back to the last known good key protector.</span></span><br/> |
| [<span data-ttu-id="b4e92-122">**сеткэйпротектор**</span><span class="sxs-lookup"><span data-stu-id="b4e92-122">**SetKeyProtector**</span></span>](msvm-securityservice-setkeyprotector.md)                                   | <span data-ttu-id="b4e92-123">Метод для задания предохранителя ключа виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="b4e92-123">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="b4e92-124">**сетсекуритиполици**</span><span class="sxs-lookup"><span data-stu-id="b4e92-124">**SetSecurityPolicy**</span></span>](msvm-securityservice-setsecuritypolicy.md)                               | <span data-ttu-id="b4e92-125">Метод для задания предохранителя ключа виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="b4e92-125">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="b4e92-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="b4e92-126">**StartService**</span></span>](msvm-securityservice-startservice.md)                                         | <span data-ttu-id="b4e92-127">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="b4e92-127">Starts the service.</span></span><br/>                                          |
| [<span data-ttu-id="b4e92-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="b4e92-128">**StopService**</span></span>](msvm-securityservice-stopservice.md)                                           | <span data-ttu-id="b4e92-129">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="b4e92-129">Stops the service.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="b4e92-130">Требования</span><span class="sxs-lookup"><span data-stu-id="b4e92-130">Requirements</span></span>



| <span data-ttu-id="b4e92-131">Требование</span><span class="sxs-lookup"><span data-stu-id="b4e92-131">Requirement</span></span> | <span data-ttu-id="b4e92-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e92-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e92-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4e92-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b4e92-134">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="b4e92-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b4e92-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4e92-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b4e92-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b4e92-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b4e92-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b4e92-137">Namespace</span></span><br/>                | <span data-ttu-id="b4e92-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b4e92-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b4e92-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b4e92-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4e92-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4e92-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4e92-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b4e92-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4e92-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4e92-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b4e92-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4e92-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e92-144">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="b4e92-144">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




