---
description: Представляет связь между управляемым элементом и его возможностями.
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: Класс CIM_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682939"
---
# <a name="cim_elementcapabilities-class"></a><span data-ttu-id="0d1ce-103">\_Класс CIM елементкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="0d1ce-103">CIM\_ElementCapabilities class</span></span>

<span data-ttu-id="0d1ce-104">Представляет связь между управляемым элементом и его возможностями.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-104">Represents an association between a managed element and its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d1ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d1ce-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="0d1ce-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0d1ce-106">Members</span></span>

<span data-ttu-id="0d1ce-107">Класс **CIM \_ елементкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0d1ce-107">The **CIM\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="0d1ce-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="0d1ce-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d1ce-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0d1ce-109">Properties</span></span>

<span data-ttu-id="0d1ce-110">Класс **CIM \_ елементкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-110">The **CIM\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d1ce-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="0d1ce-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d1ce-112">Тип данных: **\_ возможности CIM**</span><span class="sxs-lookup"><span data-stu-id="0d1ce-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="0d1ce-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d1ce-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d1ce-114">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d1ce-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d1ce-115">Возможности, связанные с управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-115">The capabilities associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="0d1ce-116">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="0d1ce-116">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d1ce-117">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0d1ce-117">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d1ce-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d1ce-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d1ce-119">Набор описательных сведений о возможностях.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-119">A set of descriptive information about the capabilities.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="0d1ce-120">**По умолчанию** (2)</span><span class="sxs-lookup"><span data-stu-id="0d1ce-120">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

<span data-ttu-id="0d1ce-121">**Текущий** (3)</span><span class="sxs-lookup"><span data-stu-id="0d1ce-121">**Current** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0d1ce-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0d1ce-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="0d1ce-123">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="0d1ce-123">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d1ce-124">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="0d1ce-124">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d1ce-125">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="0d1ce-125">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="0d1ce-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d1ce-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d1ce-127">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0d1ce-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0d1ce-128">Управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-128">The managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d1ce-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0d1ce-129">Requirements</span></span>



| <span data-ttu-id="0d1ce-130">Требование</span><span class="sxs-lookup"><span data-stu-id="0d1ce-130">Requirement</span></span> | <span data-ttu-id="0d1ce-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0d1ce-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1ce-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d1ce-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1ce-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0d1ce-133">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0d1ce-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d1ce-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1ce-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d1ce-135">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0d1ce-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0d1ce-136">Namespace</span></span><br/>                | <span data-ttu-id="0d1ce-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0d1ce-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d1ce-138">MOF</span><span class="sxs-lookup"><span data-stu-id="0d1ce-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d1ce-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d1ce-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d1ce-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0d1ce-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d1ce-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d1ce-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

