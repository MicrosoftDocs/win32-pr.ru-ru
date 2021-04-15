---
description: Представляет универсальную ассоциацию между двумя управляемыми элементами, которые представляют различные аспекты одной и той же базовой сущности.
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: Класс CIM_LogicalIdentity (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662143"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a><span data-ttu-id="516d2-103">Класс CIM_LogicalIdentity (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="516d2-103">CIM_LogicalIdentity class (Hyper-V management)</span></span>

<span data-ttu-id="516d2-104">Представляет универсальную ассоциацию между двумя управляемыми элементами, которые представляют различные аспекты одной и той же базовой сущности.</span><span class="sxs-lookup"><span data-stu-id="516d2-104">Represents a generic association between two managed elements that represent different aspects of the same underlying entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="516d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="516d2-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a><span data-ttu-id="516d2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="516d2-106">Members</span></span>

<span data-ttu-id="516d2-107">Класс **CIM \_ логикалидентити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="516d2-107">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="516d2-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="516d2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="516d2-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="516d2-109">Properties</span></span>

<span data-ttu-id="516d2-110">Класс **CIM \_ логикалидентити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="516d2-110">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="516d2-111">**самилемент**</span><span class="sxs-lookup"><span data-stu-id="516d2-111">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="516d2-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="516d2-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="516d2-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="516d2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="516d2-114">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="516d2-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="516d2-115">Второй аспект ассоциации.</span><span class="sxs-lookup"><span data-stu-id="516d2-115">The second aspect in the association.</span></span>

</dd> <dt>

<span data-ttu-id="516d2-116">**системелемент**</span><span class="sxs-lookup"><span data-stu-id="516d2-116">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="516d2-117">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="516d2-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="516d2-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="516d2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="516d2-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="516d2-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="516d2-120">Первый аспект ассоциации.</span><span class="sxs-lookup"><span data-stu-id="516d2-120">The first aspect in the association.</span></span> <span data-ttu-id="516d2-121">Использование системы в имени свойства не ограничивает область ассоциации.</span><span class="sxs-lookup"><span data-stu-id="516d2-121">The use of System in the property name does not limit the scope of the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="516d2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="516d2-122">Requirements</span></span>



| <span data-ttu-id="516d2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="516d2-123">Requirement</span></span> | <span data-ttu-id="516d2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="516d2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="516d2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="516d2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="516d2-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="516d2-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="516d2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="516d2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="516d2-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="516d2-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="516d2-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="516d2-129">Namespace</span></span><br/>                | <span data-ttu-id="516d2-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="516d2-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="516d2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="516d2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="516d2-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="516d2-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="516d2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="516d2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="516d2-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="516d2-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

