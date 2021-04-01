---
description: '&Win32 \_ UserAccount \# 32; Класс WMI содержит сведения об учетной записи пользователя в компьютерной системе под Windows.'
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Класс Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072389"
---
# <a name="win32_useraccount-class"></a><span data-ttu-id="84f07-103">\_Класс Win32 UserAccount</span><span class="sxs-lookup"><span data-stu-id="84f07-103">Win32\_UserAccount class</span></span>

<span data-ttu-id="84f07-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ UserAccount для Win32** содержит сведения об учетной записи пользователя в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="84f07-104">The **Win32\_UserAccount** [WMI class](../wmisdk/retrieving-a-class.md) contains information about a user account on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="84f07-105">Так как **имя** и **домен** являются ключевыми свойствами, перечисление **Win32 \_ UserAccount** в большой сети может негативно сказаться на производительности.</span><span class="sxs-lookup"><span data-stu-id="84f07-105">Because both the **Name** and **Domain** are key properties, enumerating **Win32\_UserAccount** on a large network can negatively affect performance.</span></span> <span data-ttu-id="84f07-106">Вызов **GetObject** или выполнение запросов к конкретному экземпляру оказывает меньшее влияние.</span><span class="sxs-lookup"><span data-stu-id="84f07-106">Calling **GetObject** or querying for a specific instance has less impact.</span></span>

 

<span data-ttu-id="84f07-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="84f07-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="84f07-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="84f07-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f07-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84f07-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="84f07-110">Члены</span><span class="sxs-lookup"><span data-stu-id="84f07-110">Members</span></span>

<span data-ttu-id="84f07-111">Класс **Win32 \_ UserAccount** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="84f07-111">The **Win32\_UserAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="84f07-112">Методы</span><span class="sxs-lookup"><span data-stu-id="84f07-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="84f07-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="84f07-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="84f07-114">Методы</span><span class="sxs-lookup"><span data-stu-id="84f07-114">Methods</span></span>

<span data-ttu-id="84f07-115">Класс **Win32 \_ UserAccount** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="84f07-115">The **Win32\_UserAccount** class has these methods.</span></span>



| <span data-ttu-id="84f07-116">Метод</span><span class="sxs-lookup"><span data-stu-id="84f07-116">Method</span></span>                                                     | <span data-ttu-id="84f07-117">Описание</span><span class="sxs-lookup"><span data-stu-id="84f07-117">Description</span></span>                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="84f07-118">**Имени**</span><span class="sxs-lookup"><span data-stu-id="84f07-118">**Rename**</span></span>](rename-method-in-class-win32-useraccount.md) | <span data-ttu-id="84f07-119">Позволяет переименование учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="84f07-119">Allows for the renaming of the user account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="84f07-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="84f07-120">Properties</span></span>

<span data-ttu-id="84f07-121">Класс **Win32 \_ UserAccount** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="84f07-121">The **Win32\_UserAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84f07-122">**AccountType**</span><span class="sxs-lookup"><span data-stu-id="84f07-122">**AccountType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-123">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84f07-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-125">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ Flags")</span><span class="sxs-lookup"><span data-stu-id="84f07-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|usri2\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-126">Флаги, описывающие характеристики учетной записи пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="84f07-126">Flags that describe the characteristics of a Windows user account.</span></span>

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="84f07-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Временная повторяющаяся учетная запись** (256)</span><span class="sxs-lookup"><span data-stu-id="84f07-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporary duplicate account** (256)</span></span>


</dt> <dd>

<span data-ttu-id="84f07-128">**УФ \_ временная \_ \_ учетная запись повторения**</span><span class="sxs-lookup"><span data-stu-id="84f07-128">**UF\_TEMP\_DUPLICATE\_ACCOUNT**</span></span>

<span data-ttu-id="84f07-129">Локальная учетная запись пользователя для пользователей, имеющих основную учетную запись в другом домене.</span><span class="sxs-lookup"><span data-stu-id="84f07-129">Local user account for users who have a primary account in another domain.</span></span> <span data-ttu-id="84f07-130">Эта учетная запись предоставляет пользователю доступ только к этому домену — не к домену, который доверяет данному домену.</span><span class="sxs-lookup"><span data-stu-id="84f07-130">This account provides user access to this domain only—not to any domain that trusts this domain.</span></span>

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="84f07-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Обычная учетная запись** (512)</span><span class="sxs-lookup"><span data-stu-id="84f07-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normal account** (512)</span></span>


</dt> <dd>

<span data-ttu-id="84f07-132">**\_Обычная \_ учетная запись УФ**</span><span class="sxs-lookup"><span data-stu-id="84f07-132">**UF\_NORMAL\_ACCOUNT**</span></span>

<span data-ttu-id="84f07-133">Тип учетной записи по умолчанию, представляющий обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="84f07-133">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="84f07-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Учетная запись междоменного доверия** (2048)</span><span class="sxs-lookup"><span data-stu-id="84f07-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Interdomain trust account** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="84f07-135">**\_ \_ учетная запись междоменного доверия УФ \_**</span><span class="sxs-lookup"><span data-stu-id="84f07-135">**UF\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="84f07-136">Учетная запись для системного домена, который доверяет другим доменам.</span><span class="sxs-lookup"><span data-stu-id="84f07-136">Account for a system domain that trusts other domains.</span></span>

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="84f07-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Учетная запись доверия рабочей станции** (4096)</span><span class="sxs-lookup"><span data-stu-id="84f07-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Workstation trust account** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="84f07-138">**\_ \_ учетная запись доверия рабочей станции УФ \_**</span><span class="sxs-lookup"><span data-stu-id="84f07-138">**UF\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="84f07-139">Учетная запись компьютера для компьютера под Windows, который является членом этого домена.</span><span class="sxs-lookup"><span data-stu-id="84f07-139">Computer account for a computer system running Windows that is a member of this domain.</span></span>

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="84f07-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Учетная запись доверия сервера** (8192)</span><span class="sxs-lookup"><span data-stu-id="84f07-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server trust account** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="84f07-141">**\_ \_ \_ учетная запись доверия сервера УФ**</span><span class="sxs-lookup"><span data-stu-id="84f07-141">**UF\_SERVER\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="84f07-142">Учетная запись для системного контроллера домена резервного копирования, который является членом этого домена.</span><span class="sxs-lookup"><span data-stu-id="84f07-142">Account for a system backup domain controller that is a member of this domain.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84f07-143">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="84f07-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84f07-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-146">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="84f07-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-147">Домен и имя пользователя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="84f07-147">Domain and username of the account.</span></span>

<span data-ttu-id="84f07-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84f07-149">**Описание**</span><span class="sxs-lookup"><span data-stu-id="84f07-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84f07-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-152">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="84f07-152">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-153">Описание учетной записи.</span><span class="sxs-lookup"><span data-stu-id="84f07-153">Description of the account.</span></span>

<span data-ttu-id="84f07-154">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84f07-155">**Отключено**</span><span class="sxs-lookup"><span data-stu-id="84f07-155">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-156">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="84f07-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84f07-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="84f07-158">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| user \_ info \| УФ \_ аккаунтдисабле")</span><span class="sxs-lookup"><span data-stu-id="84f07-158">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|USER\_INFO\|UF\_ACCOUNTDISABLE")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-159">Учетная запись пользователя Windows отключена.</span><span class="sxs-lookup"><span data-stu-id="84f07-159">Windows user account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="84f07-160">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="84f07-160">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84f07-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-163">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("домен"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management functions \| имя_домена")</span><span class="sxs-lookup"><span data-stu-id="84f07-163">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-164">Имя домена Windows, к которому принадлежит учетная запись пользователя, например "НД-SALES".</span><span class="sxs-lookup"><span data-stu-id="84f07-164">Name of the Windows domain to which a user account belongs, for example: "NA-SALES".</span></span>

</dd> <dt>

<span data-ttu-id="84f07-165">**FullName**</span><span class="sxs-lookup"><span data-stu-id="84f07-165">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84f07-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84f07-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="84f07-168">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетями \| [**\_ сведения о пользователе \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ полное \_ имя**")</span><span class="sxs-lookup"><span data-stu-id="84f07-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**usri2\_full\_name**")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-169">Полное имя локального пользователя, например: "Уилсон (".</span><span class="sxs-lookup"><span data-stu-id="84f07-169">Full name of a local user, for example: "Dan Wilson".</span></span>

</dd> <dt>

<span data-ttu-id="84f07-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84f07-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-171">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f07-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-173">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="84f07-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-174">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="84f07-174">Date the object is installed.</span></span> <span data-ttu-id="84f07-175">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="84f07-175">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="84f07-176">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84f07-177">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="84f07-177">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-178">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="84f07-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-180">Квалификаторы: [ **fixed**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="84f07-180">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="84f07-181">Если **значение — true**, учетная запись определена на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="84f07-181">If **true**, the account is defined on the local computer.</span></span>

<span data-ttu-id="84f07-182">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-182">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="84f07-183">**Блокирование**</span><span class="sxs-lookup"><span data-stu-id="84f07-183">**Lockout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="84f07-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-185">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84f07-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="84f07-186">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **УФ \_ Блокировка**")</span><span class="sxs-lookup"><span data-stu-id="84f07-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_LOCKOUT**")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-187">Если **значение — true**, учетная запись пользователя заблокирована для операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="84f07-187">If **true**, the user account is locked out of the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="84f07-188">**Name**</span><span class="sxs-lookup"><span data-stu-id="84f07-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84f07-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-191">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("имя"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| ")</span><span class="sxs-lookup"><span data-stu-id="84f07-191">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-192">Имя учетной записи пользователя Windows в домене, указанном в свойстве **domain** данного класса.</span><span class="sxs-lookup"><span data-stu-id="84f07-192">Name of the Windows user account on the domain that the **Domain** property of this class specifies.</span></span>

<span data-ttu-id="84f07-193">Пример: "данвилсон".</span><span class="sxs-lookup"><span data-stu-id="84f07-193">Example: "danwilson".</span></span>

<span data-ttu-id="84f07-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84f07-195">**пассвордчанжеабле**</span><span class="sxs-lookup"><span data-stu-id="84f07-195">**PasswordChangeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="84f07-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-197">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84f07-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="84f07-198">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **УФ \_ PASSWD не \_ удается \_ изменить**")</span><span class="sxs-lookup"><span data-stu-id="84f07-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_CANT\_CHANGE**")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-199">Если **значение — true**, пароль этой учетной записи пользователя можно изменить.</span><span class="sxs-lookup"><span data-stu-id="84f07-199">If **true**, the password on this user account can be changed.</span></span>

</dd> <dt>

<span data-ttu-id="84f07-200">**пассвордекспирес**</span><span class="sxs-lookup"><span data-stu-id="84f07-200">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-201">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="84f07-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84f07-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="84f07-203">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **УФ \_ не \_ Expires WITH \_ PASSWD**")</span><span class="sxs-lookup"><span data-stu-id="84f07-203">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_DONT\_EXPIRE\_PASSWD**")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-204">Если задано **значение true**, то срок действия пароля учетной записи пользователя истекает.</span><span class="sxs-lookup"><span data-stu-id="84f07-204">If **true**, the password on this user account expires.</span></span>

</dd> <dt>

<span data-ttu-id="84f07-205">**пассвордрекуиред**</span><span class="sxs-lookup"><span data-stu-id="84f07-205">**PasswordRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-206">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="84f07-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-207">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84f07-207">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="84f07-208">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **УФ \_ PASSWD \_ нотрекд**")</span><span class="sxs-lookup"><span data-stu-id="84f07-208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_NOTREQD**")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-209">Если задано **значение true**, то для учетной записи пользователя Windows требуется пароль.</span><span class="sxs-lookup"><span data-stu-id="84f07-209">If **true**, a password is required on a Windows user account.</span></span> <span data-ttu-id="84f07-210">Если задано **значение false**, то для этой учетной записи пароль не требуется.</span><span class="sxs-lookup"><span data-stu-id="84f07-210">If **false**, this account does not require a password.</span></span>

</dd> <dt>

<span data-ttu-id="84f07-211">**SID**</span><span class="sxs-lookup"><span data-stu-id="84f07-211">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-212">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84f07-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-214">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| идентификаторы безопасности Win32API (SID)")</span><span class="sxs-lookup"><span data-stu-id="84f07-214">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-215">Идентификатор безопасности (SID) для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="84f07-215">Security identifier (SID) for this account.</span></span> <span data-ttu-id="84f07-216">Идентификатор безопасности — это строковое значение переменной длины, используемое для распознавания доверенного лица.</span><span class="sxs-lookup"><span data-stu-id="84f07-216">A SID is a string value of variable length that is used to identify a trustee.</span></span> <span data-ttu-id="84f07-217">Каждая учетная запись имеет уникальный идентификатор безопасности, который имеет такой же центр, как домен Windows.</span><span class="sxs-lookup"><span data-stu-id="84f07-217">Each account has a unique SID that an authority, such as a Windows domain, issues.</span></span> <span data-ttu-id="84f07-218">Идентификатор безопасности хранится в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="84f07-218">The SID is stored in the security database.</span></span> <span data-ttu-id="84f07-219">Когда пользователь входит в систему, система получает SID пользователя из базы данных, помещает идентификатор безопасности в маркер доступа пользователя, а затем использует идентификатор безопасности в маркере доступа пользователя для обнаружения пользователя во всех последующих взаимодействиях с системой безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="84f07-219">When a user logs on, the system retrieves the user SID from the database, places the SID in the user access token, and then uses the SID in the user access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="84f07-220">Каждый идентификатор безопасности является уникальным идентификатором для пользователя или группы, а другой пользователь или группа не могут иметь одинаковый идентификатор безопасности.</span><span class="sxs-lookup"><span data-stu-id="84f07-220">Each SID is a unique identifier for a user or group, and a different user or group cannot have the same SID.</span></span>

<span data-ttu-id="84f07-221">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-221">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="84f07-222">**Идентификатор типа безопасности**</span><span class="sxs-lookup"><span data-stu-id="84f07-222">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-223">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="84f07-223">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-225">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| управления доступом для типов перечисления \| [**SID \_ \_ use**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span><span class="sxs-lookup"><span data-stu-id="84f07-225">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|[**SID\_NAME\_USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-226">Перечислимое значение, указывающее тип идентификатора безопасности.</span><span class="sxs-lookup"><span data-stu-id="84f07-226">Enumerated value that specifies the type of SID.</span></span>

<span data-ttu-id="84f07-227">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-227">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="84f07-228">**Сидтипеусер** (1)</span><span class="sxs-lookup"><span data-stu-id="84f07-228">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="84f07-229">**Сидтипеграуп** (2)</span><span class="sxs-lookup"><span data-stu-id="84f07-229">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="84f07-230">**Сидтипедомаин** (3)</span><span class="sxs-lookup"><span data-stu-id="84f07-230">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="84f07-231">**Сидтипеалиас** (4)</span><span class="sxs-lookup"><span data-stu-id="84f07-231">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="84f07-232">**Сидтипевеллкновнграуп** (5)</span><span class="sxs-lookup"><span data-stu-id="84f07-232">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="84f07-233">**Сидтипеделетедаккаунт** (6)</span><span class="sxs-lookup"><span data-stu-id="84f07-233">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="84f07-234">**Сидтипеинвалид** (7)</span><span class="sxs-lookup"><span data-stu-id="84f07-234">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="84f07-235">**Сидтипеункновн** (8)</span><span class="sxs-lookup"><span data-stu-id="84f07-235">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="84f07-236">**Сидтипекомпутер** (9)</span><span class="sxs-lookup"><span data-stu-id="84f07-236">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84f07-237">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="84f07-237">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f07-238">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84f07-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f07-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84f07-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f07-240">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="84f07-240">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="84f07-241">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="84f07-241">Current status of an object.</span></span> <span data-ttu-id="84f07-242">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="84f07-242">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="84f07-243">В число рабочих состояний входят: "ОК", "пониженное состояние" и "пред-ошибка" — такой элемент, как жесткий диск с поддержкой SMART, который может работать должным образом, но прогнозирует сбой в ближайшем будущем.</span><span class="sxs-lookup"><span data-stu-id="84f07-243">Operational statuses include: "OK", "Degraded", and "Pred Fail", which is an element such as a SMART-enabled hard disk drive that may be functioning properly, but predicts a failure in the near future.</span></span> <span data-ttu-id="84f07-244">Нерабочие состояния: "ошибка", "Запуск", "остановка" и "служба", которые могут применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="84f07-244">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service", which can apply during mirror resilvering of a disk, reloading a user permissions list, or other administrative work.</span></span>

<span data-ttu-id="84f07-245">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-245">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="84f07-246">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="84f07-246">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="84f07-247">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="84f07-247">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="84f07-248">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="84f07-248">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="84f07-249">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="84f07-249">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84f07-250">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="84f07-250">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="84f07-251">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="84f07-251">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="84f07-252">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="84f07-252">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="84f07-253">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="84f07-253">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="84f07-254">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="84f07-254">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="84f07-255">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="84f07-255">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="84f07-256">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="84f07-256">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="84f07-257">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="84f07-257">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="84f07-258">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="84f07-258">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="84f07-259"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="84f07-259"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="84f07-260">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84f07-260">Remarks</span></span>

<span data-ttu-id="84f07-261">Класс **Win32 \_ UserAccount** является производным от [**\_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="84f07-261">The **Win32\_UserAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

> [!Note]  
> <span data-ttu-id="84f07-262">Ошибка не возвращается для попытки записи в свойство, доступное только для чтения, и значение свойства остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="84f07-262">An error is not returned for an attempt to write to a read-only property, and the value of the property remains unchanged.</span></span>

 

## <a name="examples"></a><span data-ttu-id="84f07-263">Примеры</span><span class="sxs-lookup"><span data-stu-id="84f07-263">Examples</span></span>

<span data-ttu-id="84f07-264">Пример " [список локальных учетных записей пользователей с помощью инструментария WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript" в коллекции TechNet использует **Win32 \_ UserAccount** для возврата сведений о локальных учетных записях пользователей, найденных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="84f07-264">The [List Local User Accounts Using WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript code sample on TechNet Gallery uses **Win32\_UserAccount** to Returns information about the local user accounts found on a computer.</span></span>

<span data-ttu-id="84f07-265">[Преобразование SID в учетную запись пользователя и учетную запись пользователя в sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) Пример кода PowerShell в коллекции TechNet использует **Win32 \_ UserAccount** для преобразования идентификатора безопасности в учетную запись пользователя и (или) учетную запись пользователя в идентификатор безопасности.</span><span class="sxs-lookup"><span data-stu-id="84f07-265">[The Translate SID to User Account and User Account to SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell code sample on TechNet Gallery uses **Win32\_UserAccount** to translate a SID to User Account and/or a User Account to SID.</span></span>

<span data-ttu-id="84f07-266">В следующем примере кода VBScript показано, как получить полное имя пользователя на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="84f07-266">The following VBScript code example shows you how to get the full name of a user on a local computer.</span></span> <span data-ttu-id="84f07-267">Полное имя — это имя человека, например, пользователь может иметь имя «кенсанчез», а полное имя — «Алексей Sanchez)», поэтому вы можете подставить реальное имя домена и имя пользователя для «Мидомаиннаме» и «MyUserName».</span><span class="sxs-lookup"><span data-stu-id="84f07-267">The full name is the human language name, for example, a person may have the user name of "kensanchez" and the full name may be "Ken Sanchez", so you substitute the real domain name and user name for "MyDomainName" and "MyUserName".</span></span> <span data-ttu-id="84f07-268">Для эффективного запроса необходимо указать и свойства домена, и имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="84f07-268">For an efficient query, you must specify both the domain and user name properties.</span></span>

<span data-ttu-id="84f07-269">Если вы являетесь администратором на удаленном компьютере, можно назначить имя удаленного компьютера для strComputer (вместо "."), а затем использовать сценарий следующего типа, чтобы получить полное имя учетной записи пользователя на локальном компьютере — с удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="84f07-269">If you are an administrator on a remote computer, you can assign the name of the remote computer for strComputer (instead of "."), and then use the following type of script to get the full name of a user account on a local computer—from a remote computer.</span></span>


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



## <a name="requirements"></a><span data-ttu-id="84f07-270">Требования</span><span class="sxs-lookup"><span data-stu-id="84f07-270">Requirements</span></span>



| <span data-ttu-id="84f07-271">Требование</span><span class="sxs-lookup"><span data-stu-id="84f07-271">Requirement</span></span> | <span data-ttu-id="84f07-272">Значение</span><span class="sxs-lookup"><span data-stu-id="84f07-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84f07-273">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84f07-273">Minimum supported client</span></span><br/> | <span data-ttu-id="84f07-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84f07-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84f07-275">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84f07-275">Minimum supported server</span></span><br/> | <span data-ttu-id="84f07-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84f07-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84f07-277">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84f07-277">Namespace</span></span><br/>                | <span data-ttu-id="84f07-278">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="84f07-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84f07-279">MOF</span><span class="sxs-lookup"><span data-stu-id="84f07-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f07-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84f07-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f07-281">DLL</span><span class="sxs-lookup"><span data-stu-id="84f07-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f07-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f07-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f07-283">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84f07-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f07-284">**\_Учетная запись Win32**</span><span class="sxs-lookup"><span data-stu-id="84f07-284">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="84f07-285">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="84f07-285">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
