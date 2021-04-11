---
description: Представляет параметры искусственной трехмерной службы, присутствующей в одной системе узла.
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Класс Msvm_Synthetic3DServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155919"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a><span data-ttu-id="78c59-103">\_Класс мсвм Synthetic3DServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="78c59-103">Msvm\_Synthetic3DServiceSettingData class</span></span>

<span data-ttu-id="78c59-104">Представляет параметры искусственной трехмерной службы, присутствующей в одной системе узла.</span><span class="sxs-lookup"><span data-stu-id="78c59-104">Represents the settings for the synthetic 3-D service present on a single host system.</span></span> <span data-ttu-id="78c59-105">Свойства этого класса нельзя изменить напрямую.</span><span class="sxs-lookup"><span data-stu-id="78c59-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="78c59-106">Клиент должен вызвать метод [**мсвм \_ Synthetic3DService. модифисервицесеттингс**](modifyservicesettings-msvm-synthetic3dservice.md) , чтобы изменить любое из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="78c59-106">The client must call the [**Msvm\_Synthetic3DService.ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="78c59-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="78c59-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c59-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78c59-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="78c59-109">Члены</span><span class="sxs-lookup"><span data-stu-id="78c59-109">Members</span></span>

<span data-ttu-id="78c59-110">Класс **мсвм \_ Synthetic3DServiceSettingData** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="78c59-110">The **Msvm\_Synthetic3DServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="78c59-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="78c59-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78c59-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="78c59-112">Properties</span></span>

<span data-ttu-id="78c59-113">Класс **мсвм \_ Synthetic3DServiceSettingData** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="78c59-113">The **Msvm\_Synthetic3DServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78c59-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="78c59-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c59-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78c59-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c59-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78c59-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c59-117">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="78c59-117">A short description of the object.</span></span> <span data-ttu-id="78c59-118">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="78c59-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="78c59-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="78c59-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c59-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78c59-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c59-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78c59-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c59-122">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="78c59-122">A description of the object.</span></span> <span data-ttu-id="78c59-123">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="78c59-123">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="78c59-124">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="78c59-124">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c59-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78c59-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c59-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78c59-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c59-127">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="78c59-127">A display name for the object.</span></span> <span data-ttu-id="78c59-128">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="78c59-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="78c59-129">**гпуоверкоммитенаблед**</span><span class="sxs-lookup"><span data-stu-id="78c59-129">**GPUOvercommitEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c59-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="78c59-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78c59-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78c59-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c59-132">Определяет, учитывает ли назначение виртуальной машины ограничения памяти GPU.</span><span class="sxs-lookup"><span data-stu-id="78c59-132">Controls whether virtual machine assignment takes GPU memory limitations into account.</span></span>

</dd> <dt>

<span data-ttu-id="78c59-133">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="78c59-133">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c59-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78c59-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c59-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78c59-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78c59-136">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="78c59-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="78c59-137">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="78c59-137">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="78c59-138">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="78c59-138">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78c59-139">Требования</span><span class="sxs-lookup"><span data-stu-id="78c59-139">Requirements</span></span>



| <span data-ttu-id="78c59-140">Требование</span><span class="sxs-lookup"><span data-stu-id="78c59-140">Requirement</span></span> | <span data-ttu-id="78c59-141">Значение</span><span class="sxs-lookup"><span data-stu-id="78c59-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c59-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78c59-142">Minimum supported client</span></span><br/> | <span data-ttu-id="78c59-143">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="78c59-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="78c59-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78c59-144">Minimum supported server</span></span><br/> | <span data-ttu-id="78c59-145">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="78c59-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78c59-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="78c59-146">Namespace</span></span><br/>                | <span data-ttu-id="78c59-147">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="78c59-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="78c59-148">MOF</span><span class="sxs-lookup"><span data-stu-id="78c59-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78c59-149"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78c59-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78c59-150">DLL</span><span class="sxs-lookup"><span data-stu-id="78c59-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78c59-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78c59-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

