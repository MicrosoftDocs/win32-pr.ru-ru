---
description: Связь между объектом и другим примененным к нему объектом.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: Класс CIM_LastAppliedSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717785"
---
# <a name="cim_lastappliedsettingdata-class"></a><span data-ttu-id="18491-103">\_Класс CIM ластапплиедсеттингдата</span><span class="sxs-lookup"><span data-stu-id="18491-103">CIM\_LastAppliedSettingData class</span></span>

<span data-ttu-id="18491-104">Связь между объектом и другим примененным к нему объектом.</span><span class="sxs-lookup"><span data-stu-id="18491-104">An association between an object and another object which has been applied to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18491-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="18491-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="18491-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="18491-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="18491-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="18491-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18491-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18491-108">Syntax</span></span>

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a><span data-ttu-id="18491-109">Члены</span><span class="sxs-lookup"><span data-stu-id="18491-109">Members</span></span>

<span data-ttu-id="18491-110">Класс **CIM \_ ластапплиедсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18491-110">The **CIM\_LastAppliedSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="18491-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="18491-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18491-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="18491-112">Properties</span></span>

<span data-ttu-id="18491-113">Класс **CIM \_ ластапплиедсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18491-113">The **CIM\_LastAppliedSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18491-114">**апплиедобжект**</span><span class="sxs-lookup"><span data-stu-id="18491-114">**AppliedObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18491-115">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="18491-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="18491-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18491-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18491-117">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="18491-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="18491-118">Объект, примененный к целевому объекту.</span><span class="sxs-lookup"><span data-stu-id="18491-118">The object that was applied to the target object.</span></span>

</dd> <dt>

<span data-ttu-id="18491-119">**Целевой объект**</span><span class="sxs-lookup"><span data-stu-id="18491-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18491-120">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="18491-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="18491-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18491-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18491-122">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="18491-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="18491-123">Объект, который был целевым объектом приложения объекта.</span><span class="sxs-lookup"><span data-stu-id="18491-123">The object that was the target of the object's application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18491-124">Требования</span><span class="sxs-lookup"><span data-stu-id="18491-124">Requirements</span></span>



| <span data-ttu-id="18491-125">Требование</span><span class="sxs-lookup"><span data-stu-id="18491-125">Requirement</span></span> | <span data-ttu-id="18491-126">Значение</span><span class="sxs-lookup"><span data-stu-id="18491-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="18491-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18491-127">Namespace</span></span><br/> | <span data-ttu-id="18491-128">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="18491-128">Root\\CIMV2</span></span><br/> |



 

 




