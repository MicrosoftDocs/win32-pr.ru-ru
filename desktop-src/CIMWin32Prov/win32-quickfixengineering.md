---
description: '&Win32 \_ куиккфиксенгиниринг \# 8194; Класс WMI представляет небольшое обновление на уровне системы, которое обычно называется обновлением QFE, которое применяется к текущей операционной системе.'
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Класс Win32_QuickFixEngineering
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9db31dd452161a31575b6f7184a34c35dea71e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650446"
---
# <a name="win32_quickfixengineering-class"></a><span data-ttu-id="e9529-103">\_Класс Win32 куиккфиксенгиниринг</span><span class="sxs-lookup"><span data-stu-id="e9529-103">Win32\_QuickFixEngineering class</span></span>

<span data-ttu-id="e9529-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ куиккфиксенгиниринг для Win32** представляет небольшое обновление на уровне системы, которое обычно называется обновлением QFE, которое применяется к текущей операционной системе.</span><span class="sxs-lookup"><span data-stu-id="e9529-104">The **Win32\_QuickFixEngineering** [WMI class](../wmisdk/retrieving-a-class.md) represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system.</span></span> <span data-ttu-id="e9529-105">Этот класс возвращает только обновления, предоставляемые компонентом обслуживания на основе компонентов (CBS).</span><span class="sxs-lookup"><span data-stu-id="e9529-105">This class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="e9529-106">Эти обновления не перечислены в реестре.</span><span class="sxs-lookup"><span data-stu-id="e9529-106">These updates are not listed in the registry.</span></span> <span data-ttu-id="e9529-107">Обновления, предоставляемые Microsoft установщик Windows (MSI) или веб-сайтом центра обновления Windows ( [https://update.microsoft.com](https://update.microsoft.com/) ), не возвращаются **Win32 \_ куиккфиксенгиниринг**.</span><span class="sxs-lookup"><span data-stu-id="e9529-107">Updates supplied by Microsoft Windows Installer (MSI) or the Windows update site ([https://update.microsoft.com](https://update.microsoft.com/)) are not returned by **Win32\_QuickFixEngineering**.</span></span>

<span data-ttu-id="e9529-108">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e9529-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e9529-109">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="e9529-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9529-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9529-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a><span data-ttu-id="e9529-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e9529-111">Members</span></span>

<span data-ttu-id="e9529-112">Класс **Win32 \_ куиккфиксенгиниринг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e9529-112">The **Win32\_QuickFixEngineering** class has these types of members:</span></span>

-   [<span data-ttu-id="e9529-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9529-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9529-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9529-114">Properties</span></span>

<span data-ttu-id="e9529-115">Класс **Win32 \_ куиккфиксенгиниринг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e9529-115">The **Win32\_QuickFixEngineering** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9529-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e9529-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-119">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e9529-119">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-120">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e9529-120">A short textual description of the object.</span></span>

<span data-ttu-id="e9529-121">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9529-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-122">**CSName**</span><span class="sxs-lookup"><span data-stu-id="e9529-122">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-125">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**распространяемый**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" WMI ")</span><span class="sxs-lookup"><span data-stu-id="e9529-125">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-126">Локальное имя компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="e9529-126">Local name of the computer system.</span></span> <span data-ttu-id="e9529-127">Значение этого свойства берется из класса [**CIM \_ ComputerSystem**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e9529-127">The value for this property comes from the [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e9529-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9529-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-131">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="e9529-131">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-132">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e9529-132">A textual description of the object.</span></span>

<span data-ttu-id="e9529-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9529-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-134">**фикскомментс**</span><span class="sxs-lookup"><span data-stu-id="e9529-134">**FixComments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-137">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="e9529-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-138">Дополнительные комментарии, связанные с обновлением.</span><span class="sxs-lookup"><span data-stu-id="e9529-138">Additional comments that relate to the update.</span></span>

</dd> <dt>

<span data-ttu-id="e9529-139">**Идентификаторы HotFixID**</span><span class="sxs-lookup"><span data-stu-id="e9529-139">**HotFixID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-142">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="e9529-142">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-143">Уникальный идентификатор, связанный с определенным обновлением.</span><span class="sxs-lookup"><span data-stu-id="e9529-143">Unique identifier associated with a particular update.</span></span>

</dd> <dt>

<span data-ttu-id="e9529-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e9529-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-145">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9529-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-147">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="e9529-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-148">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="e9529-148">Indicates when the object was installed.</span></span> <span data-ttu-id="e9529-149">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="e9529-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e9529-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9529-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-151">**инсталледби**</span><span class="sxs-lookup"><span data-stu-id="e9529-151">**InstalledBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-154">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="e9529-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-155">Пользователь, установивший обновление.</span><span class="sxs-lookup"><span data-stu-id="e9529-155">Person who installed the update.</span></span> <span data-ttu-id="e9529-156">Если это значение неизвестно, свойство является пустым.</span><span class="sxs-lookup"><span data-stu-id="e9529-156">If this value is unknown, the property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="e9529-157">**Установить**</span><span class="sxs-lookup"><span data-stu-id="e9529-157">**InstalledOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-160">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="e9529-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-161">Дата установки обновления.</span><span class="sxs-lookup"><span data-stu-id="e9529-161">Date that the update was installed.</span></span> <span data-ttu-id="e9529-162">Если это значение неизвестно, свойство является пустым.</span><span class="sxs-lookup"><span data-stu-id="e9529-162">If this value is unknown, the property is empty.</span></span>

> [!Note]  
> <span data-ttu-id="e9529-163">Это свойство может использовать различные форматы в зависимости от того, когда был установлен Куиккфикс.</span><span class="sxs-lookup"><span data-stu-id="e9529-163">This property may use different formats, depending on when the QuickFix was installed.</span></span> <span data-ttu-id="e9529-164">В большинстве систем используется стандартный формат даты, например "23-10-2013".</span><span class="sxs-lookup"><span data-stu-id="e9529-164">Most systems use a standard date format, such as "23-10-2013".</span></span> <span data-ttu-id="e9529-165">Однако некоторые системы могут возвращать 64-разрядное шестнадцатеричное значение в формате Win32 [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="e9529-165">However, some systems may return a 64-bit hexidecimal value in the Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

 

</dd> <dt>

<span data-ttu-id="e9529-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="e9529-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-169">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="e9529-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-170">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="e9529-170">Label by which the object is known.</span></span> <span data-ttu-id="e9529-171">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="e9529-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e9529-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9529-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-173">**сервицепаккинеффект**</span><span class="sxs-lookup"><span data-stu-id="e9529-173">**ServicePackInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-176">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="e9529-176">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-177">Пакет обновления, действующий после применения обновления.</span><span class="sxs-lookup"><span data-stu-id="e9529-177">Service pack in effect when the update was applied.</span></span> <span data-ttu-id="e9529-178">Если пакет обновления не применен, свойство принимает значение SP0.</span><span class="sxs-lookup"><span data-stu-id="e9529-178">If no service pack has been applied, the property takes on the value SP0.</span></span> <span data-ttu-id="e9529-179">Если не удается определить, какой пакет обновления действовал, это свойство имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e9529-179">If it cannot be determined what service pack was in effect, this property is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e9529-180">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e9529-180">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9529-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9529-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9529-183">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="e9529-183">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e9529-184">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e9529-184">String that indicates the current status of the object.</span></span> <span data-ttu-id="e9529-185">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="e9529-185">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e9529-186">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="e9529-186">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e9529-187">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="e9529-187">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e9529-188">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="e9529-188">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e9529-189">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="e9529-189">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e9529-190">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="e9529-190">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e9529-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9529-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e9529-192">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="e9529-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e9529-193">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="e9529-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e9529-194">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="e9529-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e9529-195">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="e9529-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9529-196">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="e9529-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e9529-197">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="e9529-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e9529-198">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="e9529-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e9529-199">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="e9529-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e9529-200">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="e9529-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e9529-201">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="e9529-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e9529-202">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="e9529-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e9529-203">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="e9529-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e9529-204">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="e9529-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="e9529-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e9529-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e9529-206">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9529-206">Remarks</span></span>

<span data-ttu-id="e9529-207">Класс **Win32 \_ куиккфиксенгиниринг** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9529-207">The **Win32\_QuickFixEngineering** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="e9529-208">Поскольку обновления хранятся в двух местах, перечисление этого класса может привести к дублированию.</span><span class="sxs-lookup"><span data-stu-id="e9529-208">Because updates are stored in two places, an enumeration of this class can result in duplicates.</span></span>

<span data-ttu-id="e9529-209">Горячее исправление — это временное исправление операционной системы, созданное группой быстрого устранения исправлений в корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e9529-209">A hot fix is a temporary operating system patch produced by the Quick Fix Engineering group at Microsoft.</span></span> <span data-ttu-id="e9529-210">Как и в случае с пакетами обновления, исправления представляют собой изменения, внесенные в версию Windows после выпуска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e9529-210">Like service packs, hot fixes represent changes that have been made to a version of Windows after the operating system has been released.</span></span>

<span data-ttu-id="e9529-211">В отличие от пакетов обновления, исправления не предназначены для установки на всех компьютерах.</span><span class="sxs-lookup"><span data-stu-id="e9529-211">Unlike service packs, hot fixes are not intended for blanket installation on all computers.</span></span> <span data-ttu-id="e9529-212">Вместо этого они разрабатываются для решения самых конкретных проблем, часто для конкретных конфигураций компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e9529-212">Instead, they are developed to address very specific problems, often for specific computer configurations.</span></span>

<span data-ttu-id="e9529-213">Кроме того, горячие исправления представляют независимые установки, которые не зависят от других выпущенных исправлений.</span><span class="sxs-lookup"><span data-stu-id="e9529-213">In addition, hot fixes represent independent installations that do not depend on other released hot fixes.</span></span> <span data-ttu-id="e9529-214">Например, гипотетическое исправление 4 не включает исправления ошибок и функции, включенные в исправления 1, 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="e9529-214">For example, a hypothetical hot fix 4 would not include the bug fixes and functionality included in hot fixes 1, 2, and 3.</span></span> <span data-ttu-id="e9529-215">В большинстве случаев не обязательно устанавливать исправления 1, 2 и 3, прежде чем устанавливать горячее исправление 4.</span><span class="sxs-lookup"><span data-stu-id="e9529-215">In most cases, there would also be no requirement that you install hot fixes 1, 2, and 3 before installing hot fix 4.</span></span> <span data-ttu-id="e9529-216">Это делает перечисление отдельных исправлений для важной административной задачи: чтобы знать точную конфигурацию компьютера, необходимо знать не только, какие пакеты обновления установлены, но и какие отдельные исправления установлены.</span><span class="sxs-lookup"><span data-stu-id="e9529-216">This makes enumeration of individual hot fixes an important administrative task: to know the exact configuration of a computer, you need to know not only which service packs have been installed but also which individual hot fixes have been installed.</span></span>

<span data-ttu-id="e9529-217">Класс **Win32 \_ куиккфиксенгиниринг** позволяет перечислить все исправления, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e9529-217">The **Win32\_QuickFixEngineering** class enables you to enumerate all the hot fixes that have been installed on a computer</span></span>

## <a name="examples"></a><span data-ttu-id="e9529-218">Примеры</span><span class="sxs-lookup"><span data-stu-id="e9529-218">Examples</span></span>

<span data-ttu-id="e9529-219">Пример [программы PowerShell installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) возвращает полный список установленных программ.</span><span class="sxs-lookup"><span data-stu-id="e9529-219">The [Get Installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) PowerShell example returns a full list of installed programs.</span></span>

<span data-ttu-id="e9529-220">Следующий пример сценария VBScript перечисляет установленные исправления на компьютере</span><span class="sxs-lookup"><span data-stu-id="e9529-220">The following VBScript sample enumerates the installed hot fixes on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a><span data-ttu-id="e9529-221">Требования</span><span class="sxs-lookup"><span data-stu-id="e9529-221">Requirements</span></span>



| <span data-ttu-id="e9529-222">Требование</span><span class="sxs-lookup"><span data-stu-id="e9529-222">Requirement</span></span> | <span data-ttu-id="e9529-223">Значение</span><span class="sxs-lookup"><span data-stu-id="e9529-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9529-224">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9529-224">Minimum supported client</span></span><br/> | <span data-ttu-id="e9529-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9529-225">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9529-226">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9529-226">Minimum supported server</span></span><br/> | <span data-ttu-id="e9529-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9529-227">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9529-228">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e9529-228">Namespace</span></span><br/>                | <span data-ttu-id="e9529-229">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e9529-229">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9529-230">MOF</span><span class="sxs-lookup"><span data-stu-id="e9529-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9529-231"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9529-231"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9529-232">DLL</span><span class="sxs-lookup"><span data-stu-id="e9529-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9529-233"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9529-233"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9529-234">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9529-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9529-235">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e9529-235">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="e9529-236">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="e9529-236">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e9529-237">Задачи WMI: операционные системы</span><span class="sxs-lookup"><span data-stu-id="e9529-237">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
