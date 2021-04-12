---
description: Представляет запись авторизации для сервера восстановления.
ms.assetid: 8c057b39-7102-4fbf-b4be-f18627a88834
title: Класс Msvm_ReplicationAuthorizationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationAuthorizationSettingData
- Msvm_ReplicationAuthorizationSettingData.InstanceID
- Msvm_ReplicationAuthorizationSettingData.Caption
- Msvm_ReplicationAuthorizationSettingData.Description
- Msvm_ReplicationAuthorizationSettingData.ElementName
- Msvm_ReplicationAuthorizationSettingData.AllowedPrimaryHostSystem
- Msvm_ReplicationAuthorizationSettingData.TrustGroup
- Msvm_ReplicationAuthorizationSettingData.ReplicaStorageLocation
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ba069de1bbe005e8a2a06891db8218ab313baa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264720"
---
# <a name="msvm_replicationauthorizationsettingdata-class"></a><span data-ttu-id="0c1c9-103">\_Класс мсвм репликатионаусоризатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="0c1c9-103">Msvm\_ReplicationAuthorizationSettingData class</span></span>

<span data-ttu-id="0c1c9-104">Представляет запись авторизации для сервера восстановления.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-104">Represents an authorization entry for a recovery server.</span></span>

<span data-ttu-id="0c1c9-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c1c9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationAuthorizationSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string AllowedPrimaryHostSystem;
  string TrustGroup;
  string ReplicaStorageLocation;
};
```

## <a name="members"></a><span data-ttu-id="0c1c9-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0c1c9-107">Members</span></span>

<span data-ttu-id="0c1c9-108">Класс **мсвм \_ репликатионаусоризатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0c1c9-108">The **Msvm\_ReplicationAuthorizationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0c1c9-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c1c9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c1c9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c1c9-110">Properties</span></span>

<span data-ttu-id="0c1c9-111">Класс **мсвм \_ репликатионаусоризатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-111">The **Msvm\_ReplicationAuthorizationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c1c9-112">**алловедпримарихостсистем**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-112">**AllowedPrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1c9-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c1c9-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c1c9-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0c1c9-115">Полное доменное имя или имя группы серверов источника, которые разрешено реплицировать на этот сервер восстановления.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-115">The fully qualified domain name or group name of the primary servers that are allowed to replicate to this recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="0c1c9-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1c9-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c1c9-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c1c9-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c1c9-119">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-119">A short description of the object.</span></span> <span data-ttu-id="0c1c9-120">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c1c9-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c1c9-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1c9-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c1c9-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c1c9-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c1c9-124">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-124">A description of the object.</span></span> <span data-ttu-id="0c1c9-125">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c1c9-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c1c9-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1c9-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c1c9-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c1c9-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c1c9-129">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-129">A display name for the object.</span></span> <span data-ttu-id="0c1c9-130">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c1c9-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c1c9-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1c9-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c1c9-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c1c9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c1c9-134">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0c1c9-135">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0c1c9-136">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c1c9-137">**репликасторажелокатион**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-137">**ReplicaStorageLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1c9-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c1c9-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c1c9-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0c1c9-140">Расположение, куда будут храниться файлы репликации из **алловедпримарихостсистем** .</span><span class="sxs-lookup"><span data-stu-id="0c1c9-140">The location where replication files from the **AllowedPrimaryHostSystem** will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="0c1c9-141">**трустграуп**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-141">**TrustGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1c9-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c1c9-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c1c9-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0c1c9-144">Имя группы доверия для записи авторизации.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-144">The name of the trust group for the authorization entry.</span></span> <span data-ttu-id="0c1c9-145">Определяет несколько записей авторизации, сгруппированных вместе.</span><span class="sxs-lookup"><span data-stu-id="0c1c9-145">This identifies the multiple authorization entries that are grouped together.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c1c9-146">Требования</span><span class="sxs-lookup"><span data-stu-id="0c1c9-146">Requirements</span></span>



| <span data-ttu-id="0c1c9-147">Требование</span><span class="sxs-lookup"><span data-stu-id="0c1c9-147">Requirement</span></span> | <span data-ttu-id="0c1c9-148">Значение</span><span class="sxs-lookup"><span data-stu-id="0c1c9-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1c9-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c1c9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0c1c9-150">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0c1c9-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c1c9-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c1c9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0c1c9-152">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0c1c9-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c1c9-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0c1c9-153">Namespace</span></span><br/>                | <span data-ttu-id="0c1c9-154">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0c1c9-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c1c9-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0c1c9-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c1c9-156"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c1c9-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c1c9-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0c1c9-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c1c9-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c1c9-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c1c9-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c1c9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1c9-160">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-160">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="0c1c9-161">**аддаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-161">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="0c1c9-162">**модифяусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-162">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="0c1c9-163">**ремовеаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="0c1c9-163">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> </dl>

 

