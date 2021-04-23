---
description: Представляет ассоциацию между двумя точками доступа к службе (SAP), в которых один SAP зависит от другого для использования службы или подключения к ней.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: Класс CIM_SAPSAPDependency (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6888cbb74ea03b85bc9abfcea24e65660fd65953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542399"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a><span data-ttu-id="61101-103">Класс CIM_SAPSAPDependency (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="61101-103">CIM_SAPSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="61101-104">Представляет ассоциацию между двумя точками доступа к службе (SAP), в которых один SAP зависит от другого для использования службы или подключения к ней.</span><span class="sxs-lookup"><span data-stu-id="61101-104">Represents an association between two service access points (SAP), in which one SAP is dependant on the other to utilize or connect with a service.</span></span> <span data-ttu-id="61101-105">Например, для печати на сетевом принтере локальные точки доступа печати должны использовать базовые SAPs, связанные с сетью, для отправки запроса на печать.</span><span class="sxs-lookup"><span data-stu-id="61101-105">For example, to print on a network printer, local print access points must utilize underlying network-related SAPs to send the print request.</span></span>

## <a name="syntax"></a><span data-ttu-id="61101-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61101-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="61101-107">Члены</span><span class="sxs-lookup"><span data-stu-id="61101-107">Members</span></span>

<span data-ttu-id="61101-108">Класс **CIM \_ сапсапдепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="61101-108">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="61101-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="61101-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61101-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="61101-110">Properties</span></span>

<span data-ttu-id="61101-111">Класс **CIM \_ сапсапдепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="61101-111">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61101-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="61101-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61101-113">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="61101-113">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="61101-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61101-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61101-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="61101-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="61101-116">Ссылка на требуемый SAP.</span><span class="sxs-lookup"><span data-stu-id="61101-116">A reference to the required SAP.</span></span>

</dd> <dt>

<span data-ttu-id="61101-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="61101-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61101-118">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="61101-118">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="61101-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61101-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61101-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="61101-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="61101-121">Ссылка на зависимый SAP.</span><span class="sxs-lookup"><span data-stu-id="61101-121">A reference to the dependant SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61101-122">Требования</span><span class="sxs-lookup"><span data-stu-id="61101-122">Requirements</span></span>



| <span data-ttu-id="61101-123">Требование</span><span class="sxs-lookup"><span data-stu-id="61101-123">Requirement</span></span> | <span data-ttu-id="61101-124">Значение</span><span class="sxs-lookup"><span data-stu-id="61101-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61101-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61101-125">Minimum supported client</span></span><br/> | <span data-ttu-id="61101-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61101-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="61101-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61101-127">Minimum supported server</span></span><br/> | <span data-ttu-id="61101-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61101-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="61101-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="61101-129">Namespace</span></span><br/>                | <span data-ttu-id="61101-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="61101-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="61101-131">MOF</span><span class="sxs-lookup"><span data-stu-id="61101-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61101-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61101-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61101-133">DLL</span><span class="sxs-lookup"><span data-stu-id="61101-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61101-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61101-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61101-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61101-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61101-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="61101-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

