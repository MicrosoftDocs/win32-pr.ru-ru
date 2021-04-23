---
description: Представляет состояние конфигурации параметров слияния диска для виртуальной машины.
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Класс Msvm_DiskMergeSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664330"
---
# <a name="msvm_diskmergesettingdata-class"></a><span data-ttu-id="63301-103">\_Класс мсвм дискмержесеттингдата</span><span class="sxs-lookup"><span data-stu-id="63301-103">Msvm\_DiskMergeSettingData class</span></span>

<span data-ttu-id="63301-104">Представляет состояние конфигурации параметров слияния диска для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="63301-104">Represents the configuration state of the disk merge settings for a virtual machine.</span></span>

<span data-ttu-id="63301-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="63301-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63301-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63301-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a><span data-ttu-id="63301-107">Члены</span><span class="sxs-lookup"><span data-stu-id="63301-107">Members</span></span>

<span data-ttu-id="63301-108">Класс **мсвм \_ дискмержесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="63301-108">The **Msvm\_DiskMergeSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="63301-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="63301-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63301-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="63301-110">Properties</span></span>

<span data-ttu-id="63301-111">Класс **мсвм \_ дискмержесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="63301-111">The **Msvm\_DiskMergeSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63301-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="63301-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63301-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63301-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63301-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63301-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63301-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="63301-115">A short description of the object.</span></span> <span data-ttu-id="63301-116">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и всегда имеет значение "данные параметров слияния диска".</span><span class="sxs-lookup"><span data-stu-id="63301-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="63301-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="63301-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63301-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63301-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63301-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63301-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63301-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="63301-120">A description of the object.</span></span> <span data-ttu-id="63301-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "данные параметров слияния диска Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="63301-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="63301-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="63301-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63301-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63301-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63301-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63301-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63301-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="63301-125">A display name for the object.</span></span> <span data-ttu-id="63301-126">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "данные параметров слияния диска".</span><span class="sxs-lookup"><span data-stu-id="63301-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Disk Merge Setting Data".</span></span> <span data-ttu-id="63301-127">Изменение этого свойства приведет к изменению свойства **ElementName** связанного производного класса [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .</span><span class="sxs-lookup"><span data-stu-id="63301-127">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="63301-128">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="63301-128">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="63301-129">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="63301-129">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63301-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63301-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63301-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63301-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63301-132">Указывает включенное состояние функции слияния диска.</span><span class="sxs-lookup"><span data-stu-id="63301-132">Specifies the enabled state of the disk merge functionality.</span></span>

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

<span data-ttu-id="63301-133">**Временно отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="63301-133">**Temporarily disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="63301-134">**Включено** (1)</span><span class="sxs-lookup"><span data-stu-id="63301-134">**Enabled** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63301-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63301-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63301-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63301-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63301-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63301-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63301-138">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="63301-138">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="63301-139">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="63301-139">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="63301-140">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)) и всегда имеет значение "Microsoft:*GUID* \\ *девицеспеЦификдата*".</span><span class="sxs-lookup"><span data-stu-id="63301-140">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63301-141">Требования</span><span class="sxs-lookup"><span data-stu-id="63301-141">Requirements</span></span>



| <span data-ttu-id="63301-142">Требование</span><span class="sxs-lookup"><span data-stu-id="63301-142">Requirement</span></span> | <span data-ttu-id="63301-143">Значение</span><span class="sxs-lookup"><span data-stu-id="63301-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63301-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63301-144">Minimum supported client</span></span><br/> | <span data-ttu-id="63301-145">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="63301-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="63301-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63301-146">Minimum supported server</span></span><br/> | <span data-ttu-id="63301-147">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="63301-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63301-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="63301-148">Namespace</span></span><br/>                | <span data-ttu-id="63301-149">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="63301-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="63301-150">MOF</span><span class="sxs-lookup"><span data-stu-id="63301-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63301-151"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63301-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63301-152">DLL</span><span class="sxs-lookup"><span data-stu-id="63301-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63301-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63301-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

