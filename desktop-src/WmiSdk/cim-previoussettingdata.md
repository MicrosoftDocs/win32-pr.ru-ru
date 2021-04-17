---
description: Связь между виртуальной системой и данными параметров моментального снимка, который является родительским для виртуальной системы.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: Класс CIM_PreviousSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704289"
---
# <a name="cim_previoussettingdata-class"></a><span data-ttu-id="5fac2-103">\_Класс CIM превиауссеттингдата</span><span class="sxs-lookup"><span data-stu-id="5fac2-103">CIM\_PreviousSettingData class</span></span>

<span data-ttu-id="5fac2-104">Связь между виртуальной системой и данными параметров моментального снимка, который является родительским для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="5fac2-104">An association between a virtual system and the setting data of the snapshot which is the parent to the virtual system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fac2-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="5fac2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5fac2-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5fac2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5fac2-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5fac2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fac2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fac2-108">Syntax</span></span>

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a><span data-ttu-id="5fac2-109">Члены</span><span class="sxs-lookup"><span data-stu-id="5fac2-109">Members</span></span>

<span data-ttu-id="5fac2-110">Класс **CIM \_ превиауссеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5fac2-110">The **CIM\_PreviousSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5fac2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5fac2-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fac2-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="5fac2-112">Properties</span></span>

<span data-ttu-id="5fac2-113">Класс **CIM \_ превиауссеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5fac2-113">The **CIM\_PreviousSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fac2-114">**превиаусобжект**</span><span class="sxs-lookup"><span data-stu-id="5fac2-114">**PreviousObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-115">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="5fac2-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fac2-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-117">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="5fac2-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5fac2-118">Данные параметра моментального снимка, являющиеся родительскими для данной компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="5fac2-118">The snapshot setting data that is the parent of this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="5fac2-119">**Целевой объект**</span><span class="sxs-lookup"><span data-stu-id="5fac2-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-120">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="5fac2-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fac2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-122">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="5fac2-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5fac2-123">Компьютерная система, которая была целью приложения.</span><span class="sxs-lookup"><span data-stu-id="5fac2-123">The computer system that was the target of the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fac2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5fac2-124">Requirements</span></span>



| <span data-ttu-id="5fac2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="5fac2-125">Requirement</span></span> | <span data-ttu-id="5fac2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="5fac2-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="5fac2-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5fac2-127">Namespace</span></span><br/> | <span data-ttu-id="5fac2-128">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5fac2-128">Root\\CIMV2</span></span><br/> |



 

 




