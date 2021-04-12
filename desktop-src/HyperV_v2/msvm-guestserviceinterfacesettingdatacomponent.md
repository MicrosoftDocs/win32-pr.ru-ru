---
description: Класс ассоциации между компонентом интерфейса гостевой службы и ресурсом гостевой службы.
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Класс Msvm_GuestServiceInterfaceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 988975fea1fd519a5e3917faeb73d345334d74b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263243"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a><span data-ttu-id="2d39e-103">\_Класс мсвм гуестсервицеинтерфацесеттингдатакомпонент</span><span class="sxs-lookup"><span data-stu-id="2d39e-103">Msvm\_GuestServiceInterfaceSettingDataComponent class</span></span>

<span data-ttu-id="2d39e-104">Класс ассоциации между компонентом интерфейса гостевой службы и ресурсом гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="2d39e-104">Association class between a guest service interface component and the guest service resource.</span></span>

<span data-ttu-id="2d39e-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2d39e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d39e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d39e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2d39e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="2d39e-107">Members</span></span>

<span data-ttu-id="2d39e-108">Класс **мсвм \_ гуестсервицеинтерфацесеттингдатакомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2d39e-108">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2d39e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d39e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d39e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d39e-110">Properties</span></span>

<span data-ttu-id="2d39e-111">Класс **мсвм \_ гуестсервицеинтерфацесеттингдатакомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2d39e-111">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d39e-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="2d39e-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d39e-113">Тип данных: **мсвм \_ гуестсервицеинтерфацекомпонентсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="2d39e-113">Data type: **Msvm\_GuestServiceInterfaceComponentSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2d39e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d39e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d39e-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="2d39e-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2d39e-116">[**Мсвм \_ гуестсервицеинтерфацекомпонентсеттингдата**](msvm-guestserviceinterfacecomponentsettingdata.md) , ссылающийся на компонент интерфейса гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="2d39e-116">A [**Msvm\_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) referencing the guest service interface component.</span></span>

</dd> <dt>

<span data-ttu-id="2d39e-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2d39e-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d39e-118">Тип данных: **\_ SettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="2d39e-118">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2d39e-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d39e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d39e-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="2d39e-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2d39e-121">Значение [**\_ SettingData CIM**](cim-settingdata.md) , которое ссылается на ресурс гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="2d39e-121">A [**CIM\_SettingData**](cim-settingdata.md) that references the guest service resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d39e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2d39e-122">Requirements</span></span>



| <span data-ttu-id="2d39e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2d39e-123">Requirement</span></span> | <span data-ttu-id="2d39e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2d39e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d39e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d39e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d39e-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2d39e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2d39e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d39e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d39e-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2d39e-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2d39e-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2d39e-129">Namespace</span></span><br/>                | <span data-ttu-id="2d39e-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2d39e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d39e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2d39e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d39e-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d39e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d39e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2d39e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d39e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d39e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d39e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d39e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d39e-136">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="2d39e-136">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

