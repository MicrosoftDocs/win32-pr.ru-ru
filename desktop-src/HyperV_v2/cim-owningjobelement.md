---
description: Представляет связь между заданием и управляемым элементом, создавшим задание.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: Класс CIM_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664337"
---
# <a name="cim_owningjobelement-class"></a><span data-ttu-id="adbd7-103">\_Класс CIM овнингжобелемент</span><span class="sxs-lookup"><span data-stu-id="adbd7-103">CIM\_OwningJobElement class</span></span>

<span data-ttu-id="adbd7-104">Представляет связь между заданием и управляемым элементом, создавшим задание.</span><span class="sxs-lookup"><span data-stu-id="adbd7-104">Represents an association between a job and the managed element that created the job.</span></span> <span data-ttu-id="adbd7-105">Так как задание может перемещаться между системами, а управляемый элемент может не существовать в течение всего задания, в некоторых случаях такая ассоциация может быть невозможной или может существовать только для части существования задания.</span><span class="sxs-lookup"><span data-stu-id="adbd7-105">Since a job might move between systems, and the managed element might not exist for the entire duration of the job, in some cases, this association might not be possible or might only exist for a portion of the existence of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="adbd7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adbd7-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="adbd7-107">Члены</span><span class="sxs-lookup"><span data-stu-id="adbd7-107">Members</span></span>

<span data-ttu-id="adbd7-108">Класс **CIM \_ овнингжобелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="adbd7-108">The **CIM\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="adbd7-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="adbd7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="adbd7-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="adbd7-110">Properties</span></span>

<span data-ttu-id="adbd7-111">Класс **CIM \_ овнингжобелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="adbd7-111">The **CIM\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="adbd7-112">**овнеделемент**</span><span class="sxs-lookup"><span data-stu-id="adbd7-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbd7-113">Тип данных: **\_ Задание CIM** .</span><span class="sxs-lookup"><span data-stu-id="adbd7-113">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="adbd7-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="adbd7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adbd7-115">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="adbd7-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="adbd7-116">Ссылка на задание, созданное управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="adbd7-116">A reference to the job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="adbd7-117">**овнинжелемент**</span><span class="sxs-lookup"><span data-stu-id="adbd7-117">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbd7-118">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="adbd7-118">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="adbd7-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="adbd7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adbd7-120">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="adbd7-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="adbd7-121">Ссылка на управляемый элемент, создавший задание.</span><span class="sxs-lookup"><span data-stu-id="adbd7-121">A reference to the managed element that created the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adbd7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="adbd7-122">Requirements</span></span>



| <span data-ttu-id="adbd7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="adbd7-123">Requirement</span></span> | <span data-ttu-id="adbd7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="adbd7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adbd7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adbd7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="adbd7-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="adbd7-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="adbd7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adbd7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="adbd7-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="adbd7-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="adbd7-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="adbd7-129">Namespace</span></span><br/>                | <span data-ttu-id="adbd7-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="adbd7-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="adbd7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="adbd7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adbd7-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="adbd7-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="adbd7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="adbd7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adbd7-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="adbd7-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

