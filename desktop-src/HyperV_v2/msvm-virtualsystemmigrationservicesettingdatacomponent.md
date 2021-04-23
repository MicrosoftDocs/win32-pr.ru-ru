---
description: Ассоциация, используемая для представления параметров сети миграции виртуальной системы для службы миграции виртуальной системы.
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Класс Msvm_VirtualSystemMigrationServiceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662232"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a><span data-ttu-id="83b29-103">\_Класс мсвм виртуалсистеммигратионсервицесеттингдатакомпонент</span><span class="sxs-lookup"><span data-stu-id="83b29-103">Msvm\_VirtualSystemMigrationServiceSettingDataComponent class</span></span>

<span data-ttu-id="83b29-104">Ассоциация, используемая для представления параметров сети миграции виртуальной системы для службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="83b29-104">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span>

<span data-ttu-id="83b29-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="83b29-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b29-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83b29-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="83b29-107">Члены</span><span class="sxs-lookup"><span data-stu-id="83b29-107">Members</span></span>

<span data-ttu-id="83b29-108">Класс **мсвм \_ виртуалсистеммигратионсервицесеттингдатакомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="83b29-108">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="83b29-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="83b29-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83b29-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="83b29-110">Properties</span></span>

<span data-ttu-id="83b29-111">Класс **мсвм \_ виртуалсистеммигратионсервицесеттингдатакомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="83b29-111">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83b29-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="83b29-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b29-113">Тип данных: **мсвм \_ виртуалсистеммигратионсервицесеттингдата**</span><span class="sxs-lookup"><span data-stu-id="83b29-113">Data type: **Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="83b29-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83b29-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83b29-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83b29-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83b29-116">Ссылка на экземпляр класса [**мсвм \_ виртуалсистеммигратионсервицесеттингдата**](msvm-virtualsystemmigrationservicesettingdata.md) , представляющий параметры службы миграции.</span><span class="sxs-lookup"><span data-stu-id="83b29-116">A reference to an instance of the [**Msvm\_VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) class that represents the migration service settings.</span></span>

</dd> <dt>

<span data-ttu-id="83b29-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="83b29-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b29-118">Тип данных: **мсвм \_ виртуалсистеммигратионнетворксеттингдата**</span><span class="sxs-lookup"><span data-stu-id="83b29-118">Data type: **Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="83b29-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83b29-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83b29-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="83b29-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="83b29-121">Ссылка на экземпляр класса [**мсвм \_ виртуалсистеммигратионнетворксеттингдата**](msvm-virtualsystemmigrationnetworksettingdata.md) , представляющий параметры сети миграции.</span><span class="sxs-lookup"><span data-stu-id="83b29-121">A reference to an instance of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represents the migration network settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83b29-122">Требования</span><span class="sxs-lookup"><span data-stu-id="83b29-122">Requirements</span></span>



| <span data-ttu-id="83b29-123">Требование</span><span class="sxs-lookup"><span data-stu-id="83b29-123">Requirement</span></span> | <span data-ttu-id="83b29-124">Значение</span><span class="sxs-lookup"><span data-stu-id="83b29-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83b29-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83b29-125">Minimum supported client</span></span><br/> | <span data-ttu-id="83b29-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="83b29-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="83b29-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83b29-127">Minimum supported server</span></span><br/> | <span data-ttu-id="83b29-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="83b29-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83b29-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="83b29-129">Namespace</span></span><br/>                | <span data-ttu-id="83b29-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="83b29-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="83b29-131">MOF</span><span class="sxs-lookup"><span data-stu-id="83b29-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83b29-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83b29-133">DLL</span><span class="sxs-lookup"><span data-stu-id="83b29-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83b29-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

