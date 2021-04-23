---
description: Представляет данные о учетной записи группы.
ms.assetid: a53d1276-3dc9-419a-bbb8-5dd07794a971
ms.tgt_platform: multiple
title: Класс Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group
- Win32_Group.Caption
- Win32_Group.Description
- Win32_Group.InstallDate
- Win32_Group.Status
- Win32_Group.LocalAccount
- Win32_Group.SID
- Win32_Group.SIDType
- Win32_Group.Domain
- Win32_Group.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8849ba149e0de570150682d3afbad3a4ee33f36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142271"
---
# <a name="win32_group-class"></a><span data-ttu-id="501e9-103">\_Класс группы Win32</span><span class="sxs-lookup"><span data-stu-id="501e9-103">Win32\_Group class</span></span>

<span data-ttu-id="501e9-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ группы Win32** представляет данные о учетной записи группы.</span><span class="sxs-lookup"><span data-stu-id="501e9-104">The **Win32\_Group** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents data about a group account.</span></span> <span data-ttu-id="501e9-105">Учетная запись группы позволяет изменять права доступа для списка пользователей.</span><span class="sxs-lookup"><span data-stu-id="501e9-105">A group account allows access privileges to be changed for a list of users.</span></span> <span data-ttu-id="501e9-106">Пример: Marketing2.</span><span class="sxs-lookup"><span data-stu-id="501e9-106">Example: Marketing2.</span></span>

<span data-ttu-id="501e9-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="501e9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="501e9-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="501e9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="501e9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="501e9-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Group : Win32_Account
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

## <a name="members"></a><span data-ttu-id="501e9-110">Члены</span><span class="sxs-lookup"><span data-stu-id="501e9-110">Members</span></span>

<span data-ttu-id="501e9-111">Класс **\_ группы Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="501e9-111">The **Win32\_Group** class has these types of members:</span></span>

-   [<span data-ttu-id="501e9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="501e9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="501e9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="501e9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="501e9-114">Методы</span><span class="sxs-lookup"><span data-stu-id="501e9-114">Methods</span></span>

<span data-ttu-id="501e9-115">Класс **\_ группы Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="501e9-115">The **Win32\_Group** class has these methods.</span></span>



| <span data-ttu-id="501e9-116">Метод</span><span class="sxs-lookup"><span data-stu-id="501e9-116">Method</span></span>                                               | <span data-ttu-id="501e9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="501e9-117">Description</span></span>                        |
|:-----------------------------------------------------|:-----------------------------------|
| [<span data-ttu-id="501e9-118">**Имени**</span><span class="sxs-lookup"><span data-stu-id="501e9-118">**Rename**</span></span>](rename-method-in-class-win32-group.md) | <span data-ttu-id="501e9-119">Изменяет имя группы.</span><span class="sxs-lookup"><span data-stu-id="501e9-119">Changes the group name.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="501e9-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="501e9-120">Properties</span></span>

<span data-ttu-id="501e9-121">Класс **\_ группы Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="501e9-121">The **Win32\_Group** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="501e9-122">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="501e9-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="501e9-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-125">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="501e9-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="501e9-126">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="501e9-126">A short textual description of the object.</span></span>

<span data-ttu-id="501e9-127">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="501e9-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="501e9-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="501e9-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="501e9-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-131">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="501e9-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="501e9-132">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="501e9-132">A textual description of the object.</span></span>

<span data-ttu-id="501e9-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="501e9-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="501e9-134">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="501e9-134">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="501e9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-137">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("домен"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management functions \| имя_домена")</span><span class="sxs-lookup"><span data-stu-id="501e9-137">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="501e9-138">Имя домена Windows, к которому принадлежит учетная запись группы.</span><span class="sxs-lookup"><span data-stu-id="501e9-138">Name of the Windows domain to which the group account belongs.</span></span>

<span data-ttu-id="501e9-139">Пример: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="501e9-139">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="501e9-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="501e9-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-141">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="501e9-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-143">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="501e9-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="501e9-144">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="501e9-144">Indicates when the object was installed.</span></span> <span data-ttu-id="501e9-145">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="501e9-145">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="501e9-146">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="501e9-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="501e9-147">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="501e9-147">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="501e9-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-150">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="501e9-150">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="501e9-151">Если **значение — true**, учетная запись определена на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="501e9-151">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="501e9-152">Чтобы получить только учетные записи, определенные на локальном компьютере, создайте запрос, включающий условие «LocalAccount =**true**».</span><span class="sxs-lookup"><span data-stu-id="501e9-152">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="501e9-153">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="501e9-153">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="501e9-154">**Name**</span><span class="sxs-lookup"><span data-stu-id="501e9-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="501e9-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-157">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| ")</span><span class="sxs-lookup"><span data-stu-id="501e9-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="501e9-158">Имя учетной записи группы Windows в домене, указанном свойством **domain** этого класса.</span><span class="sxs-lookup"><span data-stu-id="501e9-158">Name of the Windows group account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="501e9-159">**SID**</span><span class="sxs-lookup"><span data-stu-id="501e9-159">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="501e9-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-162">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| идентификаторы безопасности Win32API (SID)")</span><span class="sxs-lookup"><span data-stu-id="501e9-162">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="501e9-163">Идентификатор безопасности (SID) для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="501e9-163">Security identifier (SID) for this account.</span></span> <span data-ttu-id="501e9-164">Идентификатор безопасности — это строковое значение переменной длины, используемое для распознавания доверенного лица.</span><span class="sxs-lookup"><span data-stu-id="501e9-164">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="501e9-165">Каждая учетная запись имеет уникальный идентификатор безопасности, выданный центром сертификации (например, доменом Windows), который хранится в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="501e9-165">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="501e9-166">Когда пользователь входит в систему, система получает SID пользователя из базы данных и помещает ее в маркер доступа пользователя.</span><span class="sxs-lookup"><span data-stu-id="501e9-166">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="501e9-167">Система использует идентификатор безопасности в маркере доступа пользователя для обнаружения пользователя во всех последующих взаимодействиях с системой безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="501e9-167">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="501e9-168">Если идентификатор безопасности используется в качестве уникального идентификатора пользователя или группы, он не может быть использован для идентификации другого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="501e9-168">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="501e9-169">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="501e9-169">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="501e9-170">**Идентификатор типа безопасности**</span><span class="sxs-lookup"><span data-stu-id="501e9-170">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-171">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="501e9-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-173">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| управления доступом для типов \| перечисления \_ SID \_ use")</span><span class="sxs-lookup"><span data-stu-id="501e9-173">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="501e9-174">Перечислимые значения, указывающие тип идентификатора безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="501e9-174">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="501e9-175">Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="501e9-175">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="501e9-176">**Сидтипеусер** (1)</span><span class="sxs-lookup"><span data-stu-id="501e9-176">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="501e9-177">**Сидтипеграуп** (2)</span><span class="sxs-lookup"><span data-stu-id="501e9-177">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="501e9-178">**Сидтипедомаин** (3)</span><span class="sxs-lookup"><span data-stu-id="501e9-178">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="501e9-179">**Сидтипеалиас** (4)</span><span class="sxs-lookup"><span data-stu-id="501e9-179">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="501e9-180">**Сидтипевеллкновнграуп** (5)</span><span class="sxs-lookup"><span data-stu-id="501e9-180">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="501e9-181">**Сидтипеделетедаккаунт** (6)</span><span class="sxs-lookup"><span data-stu-id="501e9-181">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="501e9-182">**Сидтипеинвалид** (7)</span><span class="sxs-lookup"><span data-stu-id="501e9-182">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="501e9-183">**Сидтипеункновн** (8)</span><span class="sxs-lookup"><span data-stu-id="501e9-183">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="501e9-184">**Сидтипекомпутер** (9)</span><span class="sxs-lookup"><span data-stu-id="501e9-184">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="501e9-185">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="501e9-185">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="501e9-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="501e9-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="501e9-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="501e9-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="501e9-188">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="501e9-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="501e9-189">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="501e9-189">String that indicates the current status of the object.</span></span> <span data-ttu-id="501e9-190">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="501e9-190">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="501e9-191">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="501e9-191">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="501e9-192">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="501e9-192">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="501e9-193">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="501e9-193">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="501e9-194">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="501e9-194">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="501e9-195">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="501e9-195">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="501e9-196">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="501e9-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="501e9-197">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="501e9-197">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="501e9-198">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="501e9-198">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="501e9-199">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="501e9-199">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="501e9-200">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="501e9-200">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="501e9-201">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="501e9-201">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="501e9-202">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="501e9-202">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="501e9-203">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="501e9-203">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="501e9-204">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="501e9-204">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="501e9-205">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="501e9-205">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="501e9-206">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="501e9-206">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="501e9-207">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="501e9-207">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="501e9-208">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="501e9-208">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="501e9-209">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="501e9-209">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="501e9-210"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="501e9-210"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="501e9-211">Комментарии</span><span class="sxs-lookup"><span data-stu-id="501e9-211">Remarks</span></span>

<span data-ttu-id="501e9-212">Класс **\_ группы Win32** является производным от [**\_ учетной записи Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="501e9-212">The **Win32\_Group** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="examples"></a><span data-ttu-id="501e9-213">Примеры</span><span class="sxs-lookup"><span data-stu-id="501e9-213">Examples</span></span>

<span data-ttu-id="501e9-214">Следующий код, взятый из [списка локальных групп с помощью WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) -кода VBScript в коллекции TechNet, использует **\_ группу Win32** для возвращения сведений о локальных группах, найденных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="501e9-214">The following code, taken from the [List Local Groups Using WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) VBScript code example on TechNet Gallery, uses **Win32\_Group** to return information about the local groups found on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_Group  Where LocalAccount = True") 
 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Domain: " & objItem.Domain 
    Wscript.Echo "Local Account: " & objItem.LocalAccount 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "SID: " & objItem.SID 
    Wscript.Echo "SID Type: " & objItem.SIDType 
    Wscript.Echo "Status: " & objItem.Status 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="501e9-215">Требования</span><span class="sxs-lookup"><span data-stu-id="501e9-215">Requirements</span></span>



| <span data-ttu-id="501e9-216">Требование</span><span class="sxs-lookup"><span data-stu-id="501e9-216">Requirement</span></span> | <span data-ttu-id="501e9-217">Значение</span><span class="sxs-lookup"><span data-stu-id="501e9-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="501e9-218">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="501e9-218">Minimum supported client</span></span><br/> | <span data-ttu-id="501e9-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="501e9-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="501e9-220">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="501e9-220">Minimum supported server</span></span><br/> | <span data-ttu-id="501e9-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="501e9-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="501e9-222">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="501e9-222">Namespace</span></span><br/>                | <span data-ttu-id="501e9-223">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="501e9-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="501e9-224">MOF</span><span class="sxs-lookup"><span data-stu-id="501e9-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="501e9-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="501e9-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="501e9-226">DLL</span><span class="sxs-lookup"><span data-stu-id="501e9-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="501e9-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="501e9-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="501e9-228">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="501e9-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501e9-229">**\_Учетная запись Win32**</span><span class="sxs-lookup"><span data-stu-id="501e9-229">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

<span data-ttu-id="501e9-230">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="501e9-230">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

