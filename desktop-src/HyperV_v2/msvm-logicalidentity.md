---
description: Связывает два управляемых элемента, которые представляют различные аспекты одной и той же базовой сущности.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Класс Msvm_LogicalIdentity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545423"
---
# <a name="msvm_logicalidentity-class"></a><span data-ttu-id="dc631-103">\_Класс мсвм логикалидентити</span><span class="sxs-lookup"><span data-stu-id="dc631-103">Msvm\_LogicalIdentity class</span></span>

<span data-ttu-id="dc631-104">Связывает два управляемых элемента, которые представляют различные аспекты одной и той же базовой сущности.</span><span class="sxs-lookup"><span data-stu-id="dc631-104">Associates two managed elements that represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="dc631-105">Этот класс является производным от [**CIM \_ логикалидентити**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span><span class="sxs-lookup"><span data-stu-id="dc631-105">This class derives from [**CIM\_LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span></span>

<span data-ttu-id="dc631-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dc631-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc631-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc631-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="dc631-108">Члены</span><span class="sxs-lookup"><span data-stu-id="dc631-108">Members</span></span>

<span data-ttu-id="dc631-109">Класс **мсвм \_ логикалидентити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc631-109">The **Msvm\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="dc631-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc631-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc631-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc631-111">Properties</span></span>

<span data-ttu-id="dc631-112">Класс **мсвм \_ логикалидентити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dc631-112">The **Msvm\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc631-113">**самилемент**</span><span class="sxs-lookup"><span data-stu-id="dc631-113">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc631-114">Тип данных: **CIM \_ логикалелемент**</span><span class="sxs-lookup"><span data-stu-id="dc631-114">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="dc631-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc631-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc631-116">Ссылка на альтернативный аспект системной сущности.</span><span class="sxs-lookup"><span data-stu-id="dc631-116">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="dc631-117">**системелемент**</span><span class="sxs-lookup"><span data-stu-id="dc631-117">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc631-118">Тип данных: **CIM \_ логикалелемент**</span><span class="sxs-lookup"><span data-stu-id="dc631-118">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="dc631-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc631-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc631-120">Ссылка на один аспект логического элемента.</span><span class="sxs-lookup"><span data-stu-id="dc631-120">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc631-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dc631-121">Requirements</span></span>



| <span data-ttu-id="dc631-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dc631-122">Requirement</span></span> | <span data-ttu-id="dc631-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dc631-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc631-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc631-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc631-125">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc631-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="dc631-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc631-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc631-127">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc631-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dc631-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dc631-128">Namespace</span></span><br/>                | <span data-ttu-id="dc631-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dc631-129">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dc631-130">MOF</span><span class="sxs-lookup"><span data-stu-id="dc631-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc631-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc631-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc631-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dc631-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc631-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc631-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc631-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc631-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc631-135">**\_ЛОГИКАЛИДЕНТИТИ CIM**</span><span class="sxs-lookup"><span data-stu-id="dc631-135">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dt>

[<span data-ttu-id="dc631-136">**\_ЛОГИКАЛИДЕНТИТИ CIM**</span><span class="sxs-lookup"><span data-stu-id="dc631-136">**CIM\_LogicalIdentity**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

