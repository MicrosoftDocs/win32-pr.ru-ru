---
description: Представляет связь между заданием и управляемым элементом, ответственным за создание задания.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Класс Msvm_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684466"
---
# <a name="msvm_owningjobelement-class"></a><span data-ttu-id="c4356-103">\_Класс мсвм овнингжобелемент</span><span class="sxs-lookup"><span data-stu-id="c4356-103">Msvm\_OwningJobElement class</span></span>

<span data-ttu-id="c4356-104">Представляет связь между заданием и управляемым элементом, ответственным за создание задания.</span><span class="sxs-lookup"><span data-stu-id="c4356-104">Represents an association between a job and the managed element responsible for the creation of the job.</span></span>

<span data-ttu-id="c4356-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c4356-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4356-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4356-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="c4356-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c4356-107">Members</span></span>

<span data-ttu-id="c4356-108">Класс **мсвм \_ овнингжобелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c4356-108">The **Msvm\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="c4356-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4356-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4356-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4356-110">Properties</span></span>

<span data-ttu-id="c4356-111">Класс **мсвм \_ овнингжобелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c4356-111">The **Msvm\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4356-112">**овнеделемент**</span><span class="sxs-lookup"><span data-stu-id="c4356-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4356-113">Тип данных: **[ **мсвм \_ конкретежоб**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="c4356-113">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c4356-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4356-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4356-115">Задание, созданное управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="c4356-115">The job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="c4356-116">**овнинжелемент**</span><span class="sxs-lookup"><span data-stu-id="c4356-116">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4356-117">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="c4356-117">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="c4356-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4356-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4356-119">Управляемый элемент, ответственный за создание задания.</span><span class="sxs-lookup"><span data-stu-id="c4356-119">The managed element responsible for the creation of the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4356-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c4356-120">Requirements</span></span>



| <span data-ttu-id="c4356-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c4356-121">Requirement</span></span> | <span data-ttu-id="c4356-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c4356-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4356-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4356-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c4356-124">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c4356-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c4356-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4356-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c4356-126">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c4356-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4356-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4356-127">Namespace</span></span><br/>                | <span data-ttu-id="c4356-128">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c4356-128">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c4356-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c4356-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4356-130"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4356-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4356-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c4356-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4356-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4356-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

