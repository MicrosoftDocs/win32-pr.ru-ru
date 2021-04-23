---
description: Представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для запуска и настройки компьютерной системы (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: Класс CIM_BIOSElement (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664688"
---
# <a name="cim_bioselement-class-hyper-v-management"></a><span data-ttu-id="62dc5-103">Класс CIM_BIOSElement (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="62dc5-103">CIM_BIOSElement class (Hyper-V management)</span></span>

<span data-ttu-id="62dc5-104">Представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для запуска и настройки компьютерной системы ([**CIM \_ ComputerSystem**](cim-computersystem.md)).</span><span class="sxs-lookup"><span data-stu-id="62dc5-104">Represents the low-level software that is loaded into non-volatile storage and used to start up and configure a computer system ([**CIM\_ComputerSystem**](cim-computersystem.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="62dc5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62dc5-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a><span data-ttu-id="62dc5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="62dc5-106">Members</span></span>

<span data-ttu-id="62dc5-107">Класс **CIM \_ биоселемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="62dc5-107">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="62dc5-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="62dc5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62dc5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="62dc5-109">Properties</span></span>

<span data-ttu-id="62dc5-110">Класс **CIM \_ биоселемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="62dc5-110">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62dc5-111">**куррентлангуаже**</span><span class="sxs-lookup"><span data-stu-id="62dc5-111">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62dc5-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-114">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ биоселемент**.**Листофлангуажес**")</span><span class="sxs-lookup"><span data-stu-id="62dc5-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSElement**.**ListOfLanguages**")</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-115">Выбранный в данный момент язык для BIOS.</span><span class="sxs-lookup"><span data-stu-id="62dc5-115">The currently selected language for the BIOS.</span></span> <span data-ttu-id="62dc5-116">Эти сведения можно получить из системы System Management BIOS (SMBIOS), используя атрибут текущего языка структуры типа 13 для индексации в список строк, следующий за структурой.</span><span class="sxs-lookup"><span data-stu-id="62dc5-116">This information can be obtained from the System Management BIOS (SMBIOS) using the Current Language attribute of the Type 13 structure to index into the string list that follows the structure.</span></span> <span data-ttu-id="62dc5-117">Это свойство форматируется с использованием имени языка ISO 639, за которым может следовать имя территории ISO 3166 и метод Encoding.</span><span class="sxs-lookup"><span data-stu-id="62dc5-117">This property is formatted using the ISO 639 Language Name, and may be followed by the ISO 3166 Territory Name and the encoding method.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-118">**листофлангуажес**</span><span class="sxs-lookup"><span data-stu-id="62dc5-118">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-119">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="62dc5-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-121">Список устанавливаемых языков для BIOS.</span><span class="sxs-lookup"><span data-stu-id="62dc5-121">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="62dc5-122">Эти сведения можно получить из SMBIOS в списке строк, который следует за структурой типа 13.</span><span class="sxs-lookup"><span data-stu-id="62dc5-122">This information can be obtained from SMBIOS, from the string list that follows the Type 13 structure.</span></span> <span data-ttu-id="62dc5-123">Для указания устанавливаемых языков BIOS можно использовать имя языка ISO 639.</span><span class="sxs-lookup"><span data-stu-id="62dc5-123">An ISO 639 Language Name should be used to specify the BIOS' installable languages.</span></span> <span data-ttu-id="62dc5-124">Кроме того, можно указать имя территории ISO 3166 и метод Encoding, следуя названиям языка.</span><span class="sxs-lookup"><span data-stu-id="62dc5-124">The ISO 3166 Territory Name and the encoding method may also be specified, following the Language Name.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-125">**лоадедендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="62dc5-125">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62dc5-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="62dc5-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-129">Конечный адрес памяти, занимаемой BIOS.</span><span class="sxs-lookup"><span data-stu-id="62dc5-129">The ending address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-130">**лоадедстартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="62dc5-130">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-131">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62dc5-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="62dc5-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-134">Начальный адрес памяти, занимаемой BIOS.</span><span class="sxs-lookup"><span data-stu-id="62dc5-134">The starting address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-135">**лоадутилитинформатион**</span><span class="sxs-lookup"><span data-stu-id="62dc5-135">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62dc5-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-138">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -система BIOS \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="62dc5-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-139">Строка произвольной формы, описывающая программу BIOS Flash/Load, необходимую для обновления объекта **CIM \_ биоселемент** .</span><span class="sxs-lookup"><span data-stu-id="62dc5-139">A free form string that describes the BIOS flash/load utility that is required to update the **CIM\_BIOSElement** object.</span></span> <span data-ttu-id="62dc5-140">В этом свойстве могут быть указаны версия и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="62dc5-140">Version and other information may be indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-141">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="62dc5-141">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62dc5-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-144">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -система BIOS \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="62dc5-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-145">Производитель программного элемента.</span><span class="sxs-lookup"><span data-stu-id="62dc5-145">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-146">**примарибиос**</span><span class="sxs-lookup"><span data-stu-id="62dc5-146">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-147">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62dc5-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-149">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="62dc5-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-150">Значение true, если это основная BIOS компьютерной системы; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="62dc5-150">True if this is the primary BIOS of the computer system; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-151">**регистрюрис**</span><span class="sxs-lookup"><span data-stu-id="62dc5-151">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-152">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="62dc5-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-154">Расположение публикации реестров атрибутов BIOS, к которым соответствует реализация BIOS.</span><span class="sxs-lookup"><span data-stu-id="62dc5-154">The publication location of the BIOS attribute registries to which the BIOS implementation complies.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-155">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="62dc5-155">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-156">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="62dc5-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-158">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="62dc5-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-159">Дата выпуска BIOS.</span><span class="sxs-lookup"><span data-stu-id="62dc5-159">The Date on which this BIOS was released.</span></span>

</dd> <dt>

<span data-ttu-id="62dc5-160">**Version**</span><span class="sxs-lookup"><span data-stu-id="62dc5-160">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62dc5-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62dc5-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62dc5-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62dc5-163">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("версия"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -система BIOS \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="62dc5-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="62dc5-164">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="62dc5-164">The version of the operation.</span></span> <span data-ttu-id="62dc5-165">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="62dc5-165">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="62dc5-166">*<major>*.*<minor>*.*<revision>*</span><span class="sxs-lookup"><span data-stu-id="62dc5-166">*<major>*.*<minor>*.*<revision>*</span></span>
-   <span data-ttu-id="62dc5-167">*<major>*.*<minor><letter><revision>*</span><span class="sxs-lookup"><span data-stu-id="62dc5-167">*<major>*.*<minor><letter><revision>*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62dc5-168">Требования</span><span class="sxs-lookup"><span data-stu-id="62dc5-168">Requirements</span></span>



| <span data-ttu-id="62dc5-169">Требование</span><span class="sxs-lookup"><span data-stu-id="62dc5-169">Requirement</span></span> | <span data-ttu-id="62dc5-170">Значение</span><span class="sxs-lookup"><span data-stu-id="62dc5-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62dc5-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62dc5-171">Minimum supported client</span></span><br/> | <span data-ttu-id="62dc5-172">Windows 8</span><span class="sxs-lookup"><span data-stu-id="62dc5-172">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="62dc5-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62dc5-173">Minimum supported server</span></span><br/> | <span data-ttu-id="62dc5-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62dc5-174">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="62dc5-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62dc5-175">Namespace</span></span><br/>                | <span data-ttu-id="62dc5-176">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="62dc5-176">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="62dc5-177">MOF</span><span class="sxs-lookup"><span data-stu-id="62dc5-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62dc5-178"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62dc5-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62dc5-179">DLL</span><span class="sxs-lookup"><span data-stu-id="62dc5-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62dc5-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62dc5-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62dc5-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62dc5-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62dc5-182">**\_СОФТВАРИЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="62dc5-182">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

