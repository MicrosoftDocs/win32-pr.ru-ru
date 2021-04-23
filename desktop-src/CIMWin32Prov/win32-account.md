---
description: Содержит сведения об учетных записях пользователей и группах, известных компьютерной системе под Windows.
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Класс Win32_Account
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2af601799095192d7af4ffedce0c8e0cd28bff21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142517"
---
# <a name="win32_account-class"></a><span data-ttu-id="45cd2-103">\_Класс учетной записи Win32</span><span class="sxs-lookup"><span data-stu-id="45cd2-103">Win32\_Account class</span></span>

<span data-ttu-id="45cd2-104">Абстрактный [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ учетной записи Win32** содержит сведения об учетных записях пользователей и учетных записях групп, известных компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="45cd2-104">The **Win32\_Account** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) contains information about user accounts and group accounts known to the computer system running Windows.</span></span> <span data-ttu-id="45cd2-105">Имена пользователей или групп, распознаваемых доменом Windows, являются потомками (или членами) этого класса.</span><span class="sxs-lookup"><span data-stu-id="45cd2-105">User or group names recognized by a Windows domain are descendants (or members) of this class.</span></span>

<span data-ttu-id="45cd2-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="45cd2-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="45cd2-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="45cd2-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cd2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45cd2-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="45cd2-109">Члены</span><span class="sxs-lookup"><span data-stu-id="45cd2-109">Members</span></span>

<span data-ttu-id="45cd2-110">Класс **\_ учетной записи Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="45cd2-110">The **Win32\_Account** class has these types of members:</span></span>

-   [<span data-ttu-id="45cd2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="45cd2-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45cd2-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="45cd2-112">Properties</span></span>

<span data-ttu-id="45cd2-113">Класс **\_ учетной записи Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="45cd2-113">The **Win32\_Account** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45cd2-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="45cd2-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45cd2-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="45cd2-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-118">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="45cd2-118">Short description of the object.</span></span>

<span data-ttu-id="45cd2-119">Это свойство наследуется от класса [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="45cd2-119">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="45cd2-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45cd2-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45cd2-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-123">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="45cd2-123">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-124">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="45cd2-124">Description of the object.</span></span>

<span data-ttu-id="45cd2-125">Это свойство наследуется от класса [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="45cd2-125">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="45cd2-126">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="45cd2-126">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45cd2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-129">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) («Win32API \| Network Management functions \| domain»)</span><span class="sxs-lookup"><span data-stu-id="45cd2-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-130">Имя домена Windows, к которому принадлежит группа или пользователь.</span><span class="sxs-lookup"><span data-stu-id="45cd2-130">Name of the Windows domain to which a group or user belongs.</span></span>

<span data-ttu-id="45cd2-131">Пример: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="45cd2-131">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="45cd2-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45cd2-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-133">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45cd2-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-135">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="45cd2-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-136">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="45cd2-136">Date and time that the object was installed.</span></span> <span data-ttu-id="45cd2-137">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="45cd2-137">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="45cd2-138">Это свойство наследуется от класса [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="45cd2-138">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="45cd2-139">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="45cd2-139">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="45cd2-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-142">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45cd2-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-143">Если **значение — true**, учетная запись определена на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="45cd2-143">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="45cd2-144">Чтобы получить только учетные записи, определенные на локальном компьютере, создайте запрос, включающий условие «LocalAccount =**true**».</span><span class="sxs-lookup"><span data-stu-id="45cd2-144">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

</dd> <dt>

<span data-ttu-id="45cd2-145">**Name**</span><span class="sxs-lookup"><span data-stu-id="45cd2-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45cd2-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-148">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| имя структуры управления сетью Win32API \| ")</span><span class="sxs-lookup"><span data-stu-id="45cd2-148">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-149">Имя системной учетной записи Windows в домене, указанном свойством **domain** данного класса.</span><span class="sxs-lookup"><span data-stu-id="45cd2-149">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span> <span data-ttu-id="45cd2-150">Это свойство переопределяет свойство **Name** , унаследованное от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45cd2-150">This property overrides the **Name** property inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45cd2-151">**SID**</span><span class="sxs-lookup"><span data-stu-id="45cd2-151">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45cd2-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-154">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| идентификаторы безопасности Win32API (SID)")</span><span class="sxs-lookup"><span data-stu-id="45cd2-154">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-155">Идентификатор безопасности (SID) для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="45cd2-155">Security identifier (SID) for this account.</span></span> <span data-ttu-id="45cd2-156">Идентификатор безопасности — это строковое значение переменной длины, используемое для распознавания доверенного лица.</span><span class="sxs-lookup"><span data-stu-id="45cd2-156">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="45cd2-157">Каждая учетная запись имеет уникальный идентификатор безопасности, выданный центром сертификации (например, доменом Windows), который хранится в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="45cd2-157">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="45cd2-158">Когда пользователь входит в систему, система получает SID пользователя из базы данных и помещает ее в маркер доступа пользователя.</span><span class="sxs-lookup"><span data-stu-id="45cd2-158">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="45cd2-159">Система использует идентификатор безопасности в маркере доступа пользователя для обнаружения пользователя во всех последующих взаимодействиях с системой безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="45cd2-159">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="45cd2-160">Если идентификатор безопасности используется в качестве уникального идентификатора пользователя или группы, он не может быть использован для идентификации другого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="45cd2-160">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

</dd> <dt>

<span data-ttu-id="45cd2-161">**Идентификатор типа безопасности**</span><span class="sxs-lookup"><span data-stu-id="45cd2-161">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-162">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="45cd2-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-164">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| управления доступом для типов \| перечисления \_ SID \_ use")</span><span class="sxs-lookup"><span data-stu-id="45cd2-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-165">Перечислимые значения, указывающие тип идентификатора безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="45cd2-165">Enumerated values that specify the type of security identifier (SID).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="45cd2-166">**Сидтипеусер** (1)</span><span class="sxs-lookup"><span data-stu-id="45cd2-166">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="45cd2-167">**Сидтипеграуп** (2)</span><span class="sxs-lookup"><span data-stu-id="45cd2-167">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="45cd2-168">**Сидтипедомаин** (3)</span><span class="sxs-lookup"><span data-stu-id="45cd2-168">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="45cd2-169">**Сидтипеалиас** (4)</span><span class="sxs-lookup"><span data-stu-id="45cd2-169">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="45cd2-170">**Сидтипевеллкновнграуп** (5)</span><span class="sxs-lookup"><span data-stu-id="45cd2-170">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="45cd2-171">**Сидтипеделетедаккаунт** (6)</span><span class="sxs-lookup"><span data-stu-id="45cd2-171">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="45cd2-172">**Сидтипеинвалид** (7)</span><span class="sxs-lookup"><span data-stu-id="45cd2-172">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="45cd2-173">**Сидтипеункновн** (8)</span><span class="sxs-lookup"><span data-stu-id="45cd2-173">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="45cd2-174">**Сидтипекомпутер** (9)</span><span class="sxs-lookup"><span data-stu-id="45cd2-174">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45cd2-175">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="45cd2-175">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cd2-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45cd2-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45cd2-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cd2-178">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="45cd2-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="45cd2-179">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="45cd2-179">Current status of the object.</span></span> <span data-ttu-id="45cd2-180">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="45cd2-180">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="45cd2-181">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозирует сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="45cd2-181">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicts a failure in the near future).</span></span> <span data-ttu-id="45cd2-182">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="45cd2-182">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="45cd2-183">Последняя, «служба», может применяться при зеркальном переносе диска, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="45cd2-183">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="45cd2-184">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="45cd2-184">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="45cd2-185">Это свойство наследуется от класса [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="45cd2-185">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

<span data-ttu-id="45cd2-186">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="45cd2-186">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="45cd2-187">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="45cd2-187">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="45cd2-188">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="45cd2-188">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="45cd2-189">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="45cd2-189">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45cd2-190">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="45cd2-190">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="45cd2-191">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="45cd2-191">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="45cd2-192">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="45cd2-192">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="45cd2-193">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="45cd2-193">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="45cd2-194">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="45cd2-194">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="45cd2-195">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="45cd2-195">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="45cd2-196">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="45cd2-196">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="45cd2-197">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="45cd2-197">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="45cd2-198">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="45cd2-198">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="45cd2-199"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="45cd2-199"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="45cd2-200">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45cd2-200">Remarks</span></span>

<span data-ttu-id="45cd2-201">Класс **\_ учетной записи Win32** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45cd2-201">The **Win32\_Account** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="45cd2-202">Примеры</span><span class="sxs-lookup"><span data-stu-id="45cd2-202">Examples</span></span>

<span data-ttu-id="45cd2-203">Следующий код PowerShell извлекает локальные учетные записи.</span><span class="sxs-lookup"><span data-stu-id="45cd2-203">The following PowerShell code retrieves the local accounts.</span></span>


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



<span data-ttu-id="45cd2-204">Следующий код PowerShell получает учетные записи домена.</span><span class="sxs-lookup"><span data-stu-id="45cd2-204">The following PowerShell code retrieves the domain accounts.</span></span>


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
```



## <a name="requirements"></a><span data-ttu-id="45cd2-205">Требования</span><span class="sxs-lookup"><span data-stu-id="45cd2-205">Requirements</span></span>



| <span data-ttu-id="45cd2-206">Требование</span><span class="sxs-lookup"><span data-stu-id="45cd2-206">Requirement</span></span> | <span data-ttu-id="45cd2-207">Значение</span><span class="sxs-lookup"><span data-stu-id="45cd2-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45cd2-208">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45cd2-208">Minimum supported client</span></span><br/> | <span data-ttu-id="45cd2-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45cd2-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45cd2-210">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45cd2-210">Minimum supported server</span></span><br/> | <span data-ttu-id="45cd2-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45cd2-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45cd2-212">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="45cd2-212">Namespace</span></span><br/>                | <span data-ttu-id="45cd2-213">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="45cd2-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45cd2-214">MOF</span><span class="sxs-lookup"><span data-stu-id="45cd2-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45cd2-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45cd2-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45cd2-216">DLL</span><span class="sxs-lookup"><span data-stu-id="45cd2-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45cd2-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45cd2-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45cd2-218">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45cd2-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cd2-219">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="45cd2-219">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="45cd2-220">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="45cd2-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

