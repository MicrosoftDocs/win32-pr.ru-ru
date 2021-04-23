---
description: '&Win32 \_ SystemAccount \# 8194; Класс WMI представляет системную учетную запись.'
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Класс Win32_SystemAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656007"
---
# <a name="win32_systemaccount-class"></a><span data-ttu-id="1edd1-103">\_Класс Win32 SystemAccount</span><span class="sxs-lookup"><span data-stu-id="1edd1-103">Win32\_SystemAccount class</span></span>

<span data-ttu-id="1edd1-104">Класс **WMI \_ SystemAccount** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет системную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="1edd1-104">The **Win32\_SystemAccount** [WMI class](../wmisdk/retrieving-a-class.md) represents a system account.</span></span> <span data-ttu-id="1edd1-105">Системная учетная запись используется операционной системой и службами.</span><span class="sxs-lookup"><span data-stu-id="1edd1-105">The system account is used by the operating system and services.</span></span> <span data-ttu-id="1edd1-106">В Windows существует множество служб и процессов, которым требуется возможность внутреннего входа в систему, например во время установки Windows.</span><span class="sxs-lookup"><span data-stu-id="1edd1-106">There are many services and processes within Windows that need the capability to logon internally, for example, during a Windows installation.</span></span> <span data-ttu-id="1edd1-107">Системная учетная запись была разработана для этой цели.</span><span class="sxs-lookup"><span data-stu-id="1edd1-107">The system account was designed for that purpose.</span></span>

<span data-ttu-id="1edd1-108">Системная учетная запись — это внутренняя учетная запись, которая не отображается в диспетчере пользователей, не может быть добавлена в группы и не может иметь назначенные права пользователя.</span><span class="sxs-lookup"><span data-stu-id="1edd1-108">The system account is an internal account that does not show up in User Manager, cannot be added to any groups, and cannot have user rights assigned to it.</span></span> <span data-ttu-id="1edd1-109">Однако системная учетная запись отображается на томе файловой системы NTFS в диспетчере файлов, который находится в разделе "разрешения" меню "безопасность".</span><span class="sxs-lookup"><span data-stu-id="1edd1-109">However, the system account does show up on an NTFS file system volume in file manager, which is located in the Permissions section of the Security menu.</span></span> <span data-ttu-id="1edd1-110">По умолчанию системным учетным записям предоставляется полный доступ ко всем файлам на томе файловой системы NTFS. Это означает, что учетная запись System имеет те же функциональные привилегии, что и учетная запись администратора.</span><span class="sxs-lookup"><span data-stu-id="1edd1-110">By default, the system account is granted full control to all files on an NTFS file system volume, which means that the system account has the same functional privileges as the administrator account.</span></span>

<span data-ttu-id="1edd1-111">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1edd1-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1edd1-112">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="1edd1-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1edd1-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1edd1-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="1edd1-114">Члены</span><span class="sxs-lookup"><span data-stu-id="1edd1-114">Members</span></span>

<span data-ttu-id="1edd1-115">Класс **Win32 \_ SystemAccount** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1edd1-115">The **Win32\_SystemAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="1edd1-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="1edd1-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1edd1-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="1edd1-117">Properties</span></span>

<span data-ttu-id="1edd1-118">Класс **Win32 \_ SystemAccount** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1edd1-118">The **Win32\_SystemAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1edd1-119">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1edd1-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1edd1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-122">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1edd1-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-123">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1edd1-123">A short textual description of the object.</span></span>

<span data-ttu-id="1edd1-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1edd1-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1edd1-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1edd1-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1edd1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-128">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="1edd1-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-129">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1edd1-129">A textual description of the object.</span></span>

<span data-ttu-id="1edd1-130">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1edd1-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1edd1-131">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="1edd1-131">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1edd1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-134">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("домен"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management functions \| имя_домена")</span><span class="sxs-lookup"><span data-stu-id="1edd1-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-135">Имя домена Windows, к которому принадлежит системная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="1edd1-135">Name of the Windows domain to which the system account belongs.</span></span>

<span data-ttu-id="1edd1-136">Пример: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="1edd1-136">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="1edd1-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1edd1-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-138">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1edd1-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-140">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="1edd1-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-141">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="1edd1-141">Indicates when the object was installed.</span></span> <span data-ttu-id="1edd1-142">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="1edd1-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1edd1-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1edd1-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1edd1-144">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="1edd1-144">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1edd1-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-147">Квалификаторы: [ **fixed**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1edd1-147">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-148">Если **значение — true**, учетная запись определена на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1edd1-148">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="1edd1-149">Чтобы получить только учетные записи, определенные на локальном компьютере, создайте запрос, включающий условие «LocalAccount =**true**».</span><span class="sxs-lookup"><span data-stu-id="1edd1-149">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="1edd1-150">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="1edd1-150">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="1edd1-151">**Name**</span><span class="sxs-lookup"><span data-stu-id="1edd1-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1edd1-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-154">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("имя"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| ")</span><span class="sxs-lookup"><span data-stu-id="1edd1-154">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-155">Имя системной учетной записи Windows в домене, указанном свойством **domain** данного класса.</span><span class="sxs-lookup"><span data-stu-id="1edd1-155">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="1edd1-156">**SID**</span><span class="sxs-lookup"><span data-stu-id="1edd1-156">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1edd1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-159">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| идентификаторы безопасности Win32API (SID)")</span><span class="sxs-lookup"><span data-stu-id="1edd1-159">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-160">Идентификатор безопасности (SID) для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1edd1-160">Security identifier (SID) for this account.</span></span> <span data-ttu-id="1edd1-161">Идентификатор безопасности — это строковое значение переменной длины, используемое для распознавания доверенного лица.</span><span class="sxs-lookup"><span data-stu-id="1edd1-161">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="1edd1-162">Каждая учетная запись имеет уникальный идентификатор безопасности, выданный центром сертификации (например, доменом Windows), который хранится в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="1edd1-162">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="1edd1-163">Когда пользователь входит в систему, система получает SID пользователя из базы данных и помещает ее в маркер доступа пользователя.</span><span class="sxs-lookup"><span data-stu-id="1edd1-163">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="1edd1-164">Система использует идентификатор безопасности в маркере доступа пользователя для обнаружения пользователя во всех последующих взаимодействиях с системой безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="1edd1-164">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="1edd1-165">Если идентификатор безопасности используется в качестве уникального идентификатора пользователя или группы, он не может быть использован для идентификации другого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="1edd1-165">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="1edd1-166">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="1edd1-166">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="1edd1-167">**Идентификатор типа безопасности**</span><span class="sxs-lookup"><span data-stu-id="1edd1-167">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-168">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1edd1-168">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-170">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| управления доступом для типов \| перечисления \_ SID \_ use")</span><span class="sxs-lookup"><span data-stu-id="1edd1-170">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-171">Перечислимые значения, указывающие тип идентификатора безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="1edd1-171">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="1edd1-172">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="1edd1-172">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="1edd1-173">**Сидтипеусер** (1)</span><span class="sxs-lookup"><span data-stu-id="1edd1-173">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="1edd1-174">**Сидтипеграуп** (2)</span><span class="sxs-lookup"><span data-stu-id="1edd1-174">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="1edd1-175">**Сидтипедомаин** (3)</span><span class="sxs-lookup"><span data-stu-id="1edd1-175">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="1edd1-176">**Сидтипеалиас** (4)</span><span class="sxs-lookup"><span data-stu-id="1edd1-176">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="1edd1-177">**Сидтипевеллкновнграуп** (5)</span><span class="sxs-lookup"><span data-stu-id="1edd1-177">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="1edd1-178">**Сидтипеделетедаккаунт** (6)</span><span class="sxs-lookup"><span data-stu-id="1edd1-178">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="1edd1-179">**Сидтипеинвалид** (7)</span><span class="sxs-lookup"><span data-stu-id="1edd1-179">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="1edd1-180">**Сидтипеункновн** (8)</span><span class="sxs-lookup"><span data-stu-id="1edd1-180">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="1edd1-181">**Сидтипекомпутер** (9)</span><span class="sxs-lookup"><span data-stu-id="1edd1-181">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1edd1-182">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1edd1-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1edd1-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1edd1-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1edd1-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1edd1-185">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="1edd1-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1edd1-186">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1edd1-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="1edd1-187">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="1edd1-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="1edd1-188">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="1edd1-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="1edd1-189">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="1edd1-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="1edd1-190">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="1edd1-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1edd1-191">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="1edd1-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1edd1-192">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="1edd1-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1edd1-193">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1edd1-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1edd1-194">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="1edd1-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1edd1-195">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="1edd1-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1edd1-196">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="1edd1-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1edd1-197">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="1edd1-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1edd1-198">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1edd1-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1edd1-199">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="1edd1-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1edd1-200">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="1edd1-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1edd1-201">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="1edd1-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1edd1-202">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="1edd1-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1edd1-203">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="1edd1-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1edd1-204">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="1edd1-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1edd1-205">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="1edd1-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1edd1-206">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="1edd1-206">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="1edd1-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1edd1-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="1edd1-208">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1edd1-208">Remarks</span></span>

<span data-ttu-id="1edd1-209">Класс **Win32 \_ SystemAccount** является производным от [**\_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="1edd1-209">The **Win32\_SystemAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1edd1-210">Требования</span><span class="sxs-lookup"><span data-stu-id="1edd1-210">Requirements</span></span>



| <span data-ttu-id="1edd1-211">Требование</span><span class="sxs-lookup"><span data-stu-id="1edd1-211">Requirement</span></span> | <span data-ttu-id="1edd1-212">Значение</span><span class="sxs-lookup"><span data-stu-id="1edd1-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1edd1-213">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1edd1-213">Minimum supported client</span></span><br/> | <span data-ttu-id="1edd1-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1edd1-214">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1edd1-215">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1edd1-215">Minimum supported server</span></span><br/> | <span data-ttu-id="1edd1-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1edd1-216">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1edd1-217">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1edd1-217">Namespace</span></span><br/>                | <span data-ttu-id="1edd1-218">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1edd1-218">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1edd1-219">MOF</span><span class="sxs-lookup"><span data-stu-id="1edd1-219">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1edd1-220"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1edd1-220"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1edd1-221">DLL</span><span class="sxs-lookup"><span data-stu-id="1edd1-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1edd1-222"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1edd1-222"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1edd1-223">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1edd1-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1edd1-224">**\_Учетная запись Win32**</span><span class="sxs-lookup"><span data-stu-id="1edd1-224">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="1edd1-225">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="1edd1-225">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
