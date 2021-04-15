---
description: Представляет параметры для службы миграции виртуальной системы на узле.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Класс Msvm_VirtualSystemMigrationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662233"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a><span data-ttu-id="1f33b-103">\_Класс мсвм виртуалсистеммигратионсервицесеттингдата</span><span class="sxs-lookup"><span data-stu-id="1f33b-103">Msvm\_VirtualSystemMigrationServiceSettingData class</span></span>

<span data-ttu-id="1f33b-104">Представляет параметры для службы миграции виртуальной системы на узле.</span><span class="sxs-lookup"><span data-stu-id="1f33b-104">Represents the settings for the virtual system migration service on a host.</span></span> <span data-ttu-id="1f33b-105">Свойства этого класса нельзя изменить напрямую.</span><span class="sxs-lookup"><span data-stu-id="1f33b-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="1f33b-106">Клиент должен вызвать метод **мсвм \_ Виртуалсистеммигратионсервице. модифисервицесеттингс** , чтобы изменить любое из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="1f33b-106">The client must call the **Msvm\_VirtualSystemMigrationService.ModifyServiceSettings** method to modify any of these properties.</span></span>

<span data-ttu-id="1f33b-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1f33b-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f33b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f33b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a><span data-ttu-id="1f33b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1f33b-109">Members</span></span>

<span data-ttu-id="1f33b-110">Класс **мсвм \_ виртуалсистеммигратионсервицесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1f33b-110">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1f33b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f33b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f33b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f33b-112">Properties</span></span>

<span data-ttu-id="1f33b-113">Класс **мсвм \_ виртуалсистеммигратионсервицесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1f33b-113">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f33b-114">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="1f33b-114">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-115">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f33b-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f33b-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-117">Указывает механизм проверки подлинности, используемый для сетевых подключений миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="1f33b-117">Specifies the authentication mechanism used for virtual system migration network connections.</span></span> <span data-ttu-id="1f33b-118">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1f33b-118">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

<span data-ttu-id="1f33b-119">**CredSSP** (0)</span><span class="sxs-lookup"><span data-stu-id="1f33b-119">**CredSSP** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

<span data-ttu-id="1f33b-120">**Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="1f33b-120">**Kerberos** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1f33b-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1f33b-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f33b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f33b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-124">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1f33b-124">A short description of the object.</span></span> <span data-ttu-id="1f33b-125">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="1f33b-125">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="1f33b-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f33b-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f33b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f33b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-129">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1f33b-129">A description of the object.</span></span> <span data-ttu-id="1f33b-130">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1f33b-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f33b-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1f33b-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f33b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f33b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-134">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="1f33b-134">A display name for the object.</span></span> <span data-ttu-id="1f33b-135">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f33b-135">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1f33b-136">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="1f33b-136">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-137">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1f33b-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1f33b-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-139">Указывает, включен или отключен сжатие трафика динамической миграции.</span><span class="sxs-lookup"><span data-stu-id="1f33b-139">Indicates whether compression of live migration traffic is enabled or disabled.</span></span> <span data-ttu-id="1f33b-140">Значение true указывает, что включен.</span><span class="sxs-lookup"><span data-stu-id="1f33b-140">True indicates enabled.</span></span>

<span data-ttu-id="1f33b-141">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1f33b-141">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="1f33b-142">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1f33b-142">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1f33b-143">**енаблесмбтранспорт**</span><span class="sxs-lookup"><span data-stu-id="1f33b-143">**EnableSmbTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1f33b-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1f33b-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-146">Указывает, включена или отключена ли возможность использования SMB в качестве транспортного типа для передачи состояния виртуальной машины между узлами Hyper-V во время миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="1f33b-146">Indicates whether use of SMB as a transport type for transferring VM state between the Hyper-V hosts during virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="1f33b-147">**Значение true** указывает, что включен.</span><span class="sxs-lookup"><span data-stu-id="1f33b-147">**True** indicates enabled.</span></span> <span data-ttu-id="1f33b-148">Более высокая производительность достигается, если сетевые адаптеры RDMA настроены для транспорта SMB во время динамической миграции виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1f33b-148">A higher performance is achieved if RDMA NICs are configured for SMB transport during VM live migration.</span></span> <span data-ttu-id="1f33b-149">Если **енаблесмбтранспорт** имеет значение true, значение **EnableCompression** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1f33b-149">If **EnableSmbTransport** value is true, the value of **EnableCompression** is ignored.</span></span>

<span data-ttu-id="1f33b-150">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1f33b-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="1f33b-151">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1f33b-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1f33b-152">**енаблевиртуалсистеммигратион**</span><span class="sxs-lookup"><span data-stu-id="1f33b-152">**EnableVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-153">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1f33b-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f33b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-155">Указывает, включена или отключена миграция виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="1f33b-155">Specifies whether virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="1f33b-156">Миграция хранилища всегда включена.</span><span class="sxs-lookup"><span data-stu-id="1f33b-156">Storage migration is always enabled.</span></span> <span data-ttu-id="1f33b-157">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1f33b-157">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1f33b-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1f33b-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f33b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f33b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-161">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="1f33b-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-162">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="1f33b-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1f33b-163">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1f33b-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f33b-164">**максимумактивесторажемигратион**</span><span class="sxs-lookup"><span data-stu-id="1f33b-164">**MaximumActiveStorageMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f33b-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f33b-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-167">Указывает максимальное количество разрешенных миграций Active Storage.</span><span class="sxs-lookup"><span data-stu-id="1f33b-167">Specifies the maximum number of active storage migrations allowed.</span></span> <span data-ttu-id="1f33b-168">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1f33b-168">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1f33b-169">**максимумактивевиртуалсистеммигратион**</span><span class="sxs-lookup"><span data-stu-id="1f33b-169">**MaximumActiveVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f33b-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f33b-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f33b-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f33b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f33b-172">Указывает максимальное разрешенное количество активных миграций виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="1f33b-172">Specifies the maximum number of active virtual system migrations allowed.</span></span> <span data-ttu-id="1f33b-173">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1f33b-173">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f33b-174">Требования</span><span class="sxs-lookup"><span data-stu-id="1f33b-174">Requirements</span></span>



| <span data-ttu-id="1f33b-175">Требование</span><span class="sxs-lookup"><span data-stu-id="1f33b-175">Requirement</span></span> | <span data-ttu-id="1f33b-176">Значение</span><span class="sxs-lookup"><span data-stu-id="1f33b-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f33b-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f33b-177">Minimum supported client</span></span><br/> | <span data-ttu-id="1f33b-178">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f33b-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1f33b-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f33b-179">Minimum supported server</span></span><br/> | <span data-ttu-id="1f33b-180">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1f33b-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f33b-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1f33b-181">Namespace</span></span><br/>                | <span data-ttu-id="1f33b-182">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1f33b-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1f33b-183">MOF</span><span class="sxs-lookup"><span data-stu-id="1f33b-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f33b-184"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f33b-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f33b-185">DLL</span><span class="sxs-lookup"><span data-stu-id="1f33b-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f33b-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f33b-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1f33b-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f33b-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f33b-188">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1f33b-188">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="1f33b-189">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="1f33b-189">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

