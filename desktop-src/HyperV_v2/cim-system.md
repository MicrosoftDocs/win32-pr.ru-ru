---
description: Представляет набор компонентов, которые работают как единая сущность высокого уровня.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: Класс CIM_System (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662817"
---
# <a name="cim_system-class-hyper-v-management"></a><span data-ttu-id="f2eb0-103">Класс CIM_System (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-103">CIM_System class (Hyper-V management)</span></span>

<span data-ttu-id="f2eb0-104">Представляет набор компонентов, которые работают как единая сущность высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-104">Represents a set of components that function as a single high-level entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2eb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2eb0-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="f2eb0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f2eb0-106">Members</span></span>

<span data-ttu-id="f2eb0-107">Класс **\_ системы CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2eb0-107">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="f2eb0-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2eb0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2eb0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2eb0-109">Properties</span></span>

<span data-ttu-id="f2eb0-110">Класс **\_ системы CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-110">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2eb0-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2eb0-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2eb0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-114">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f2eb0-115">Имя класса, используемое для создания экземпляра этого класса.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-115">The class name used to create an instance of this class.</span></span> <span data-ttu-id="f2eb0-116">**Свойство CreationClassName** объединяется с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-116">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="f2eb0-117">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-117">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2eb0-118">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2eb0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-120">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ система CIM**.**Осеридентифингинфо**")</span><span class="sxs-lookup"><span data-stu-id="f2eb0-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="f2eb0-121">Массив, содержащий описания значений в свойстве **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="f2eb0-121">An array that contains descriptions of the values in the **OtherIdentifyingInfo** property.</span></span> <span data-ttu-id="f2eb0-122">Элементы массива в **идентифингдескриптионс** соответствуют элементам в свойстве **идентифингдескриптионс** .</span><span class="sxs-lookup"><span data-stu-id="f2eb0-122">The array items in **IdentifyingDescriptions** correspond to the items in the **IdentifyingDescriptions** property.</span></span>

</dd> <dt>

<span data-ttu-id="f2eb0-123">**Name**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-123">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2eb0-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2eb0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-126">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f2eb0-127">Ключ этого экземпляра в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-127">The key of this instance in an enterprise environment.</span></span>

</dd> <dt>

<span data-ttu-id="f2eb0-128">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-128">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2eb0-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2eb0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-131">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f2eb0-132">Соглашение об именовании, используемое свойством Name для обеспечения уникальности значений **имен** .</span><span class="sxs-lookup"><span data-stu-id="f2eb0-132">The naming convention used by the Name property to ensure that **Name** values are unique.</span></span>

</dd> <dt>

<span data-ttu-id="f2eb0-133">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-133">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2eb0-134">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-134">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2eb0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-136">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ система CIM**.**Идентифингдескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="f2eb0-136">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="f2eb0-137">Массив, содержащий набор дополнительных данных, помимо сведений об имени системы, которые можно использовать для обнаружения компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-137">An array that contains a set of additional data, beyond system name information, that could be used to identify a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="f2eb0-138">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-138">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2eb0-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2eb0-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-141">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="f2eb0-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f2eb0-142">Строка, которая предоставляет сведения о том, как может быть достигнут первичный владелец системы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f2eb0-142">A string that provides information on how the primary system owner can be reached (for example, phone number, e-mail address, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="f2eb0-143">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-143">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2eb0-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2eb0-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-146">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f2eb0-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f2eb0-147">Имя основного пользователя системы.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-147">The name of the primary user of the system.</span></span>

</dd> <dt>

<span data-ttu-id="f2eb0-148">**Роли**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-148">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2eb0-149">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f2eb0-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2eb0-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f2eb0-151">Массив, содержащий роли, которые выполняются системой в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-151">An array that contains the roles carried out by the system in an enterprise environment.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2eb0-152">Требования</span><span class="sxs-lookup"><span data-stu-id="f2eb0-152">Requirements</span></span>



| <span data-ttu-id="f2eb0-153">Требование</span><span class="sxs-lookup"><span data-stu-id="f2eb0-153">Requirement</span></span> | <span data-ttu-id="f2eb0-154">Значение</span><span class="sxs-lookup"><span data-stu-id="f2eb0-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2eb0-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2eb0-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f2eb0-156">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f2eb0-156">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f2eb0-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2eb0-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f2eb0-158">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2eb0-158">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f2eb0-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2eb0-159">Namespace</span></span><br/>                | <span data-ttu-id="f2eb0-160">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f2eb0-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f2eb0-161">MOF</span><span class="sxs-lookup"><span data-stu-id="f2eb0-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2eb0-162"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2eb0-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2eb0-163">DLL</span><span class="sxs-lookup"><span data-stu-id="f2eb0-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2eb0-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2eb0-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2eb0-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2eb0-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2eb0-166">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f2eb0-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

