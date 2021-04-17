---
description: Абстрактный класс, представляющий параметры для данного экземпляра функции коммутатора Ethernet.
ms.assetid: c1720649-585f-45a9-8329-06787bd8b600
title: Класс Msvm_EthernetSwitchFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureSettingData
- Msvm_EthernetSwitchFeatureSettingData.InstanceID
- Msvm_EthernetSwitchFeatureSettingData.Caption
- Msvm_EthernetSwitchFeatureSettingData.Description
- Msvm_EthernetSwitchFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a71d9b4a78ffedb6ffc0a0c1e01562ce7638ef65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684705"
---
# <a name="msvm_ethernetswitchfeaturesettingdata-class"></a><span data-ttu-id="dca80-103">\_Класс мсвм есернетсвитчфеатуресеттингдата</span><span class="sxs-lookup"><span data-stu-id="dca80-103">Msvm\_EthernetSwitchFeatureSettingData class</span></span>

<span data-ttu-id="dca80-104">Абстрактный класс, представляющий параметры для данного экземпляра функции коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="dca80-104">An abstract class that represents settings for a given instance of an Ethernet switch feature.</span></span> <span data-ttu-id="dca80-105">Параметры функций коммутатора Ethernet класс управления должны быть производными от этого абстрактного класса.</span><span class="sxs-lookup"><span data-stu-id="dca80-105">Ethernet Switch Features settings management class must derive from this abstract class.</span></span>

<span data-ttu-id="dca80-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="dca80-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dca80-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dca80-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="dca80-108">Члены</span><span class="sxs-lookup"><span data-stu-id="dca80-108">Members</span></span>

<span data-ttu-id="dca80-109">Класс **мсвм \_ есернетсвитчфеатуресеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dca80-109">The **Msvm\_EthernetSwitchFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="dca80-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="dca80-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dca80-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="dca80-111">Properties</span></span>

<span data-ttu-id="dca80-112">Класс **мсвм \_ есернетсвитчфеатуресеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dca80-112">The **Msvm\_EthernetSwitchFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dca80-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dca80-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dca80-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dca80-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dca80-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dca80-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dca80-116">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dca80-116">A short description of the object.</span></span> <span data-ttu-id="dca80-117">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dca80-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dca80-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dca80-118">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dca80-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dca80-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dca80-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dca80-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dca80-121">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dca80-121">A description of the object.</span></span> <span data-ttu-id="dca80-122">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dca80-122">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dca80-123">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dca80-123">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dca80-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dca80-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dca80-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dca80-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dca80-126">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="dca80-126">A display name for the object.</span></span> <span data-ttu-id="dca80-127">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dca80-127">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dca80-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dca80-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dca80-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dca80-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dca80-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dca80-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dca80-131">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="dca80-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dca80-132">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="dca80-132">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dca80-133">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dca80-133">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dca80-134">Требования</span><span class="sxs-lookup"><span data-stu-id="dca80-134">Requirements</span></span>



| <span data-ttu-id="dca80-135">Требование</span><span class="sxs-lookup"><span data-stu-id="dca80-135">Requirement</span></span> | <span data-ttu-id="dca80-136">Значение</span><span class="sxs-lookup"><span data-stu-id="dca80-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dca80-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dca80-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dca80-138">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dca80-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dca80-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dca80-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dca80-140">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dca80-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dca80-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dca80-141">Namespace</span></span><br/>                | <span data-ttu-id="dca80-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dca80-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dca80-143">MOF</span><span class="sxs-lookup"><span data-stu-id="dca80-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dca80-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dca80-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dca80-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dca80-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dca80-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dca80-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

