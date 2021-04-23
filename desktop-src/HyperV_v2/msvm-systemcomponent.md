---
description: Устанавливает &\# 0034; часть&\# 0034; отношение между системой и любым управляемым системным элементом, из которого она состоит.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Класс Msvm_SystemComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423694"
---
# <a name="msvm_systemcomponent-class"></a><span data-ttu-id="8d947-103">\_Класс мсвм системкомпонент</span><span class="sxs-lookup"><span data-stu-id="8d947-103">Msvm\_SystemComponent class</span></span>

<span data-ttu-id="8d947-104">Устанавливает отношение "часть" между системой и любым управляемым системным элементом, из которого она состоит.</span><span class="sxs-lookup"><span data-stu-id="8d947-104">Establishes a "part of" relationship between a system and any managed system element of which it is composed.</span></span>

<span data-ttu-id="8d947-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8d947-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d947-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d947-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8d947-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8d947-107">Members</span></span>

<span data-ttu-id="8d947-108">Класс **мсвм \_ системкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8d947-108">The **Msvm\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="8d947-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="8d947-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d947-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8d947-110">Properties</span></span>

<span data-ttu-id="8d947-111">Класс **мсвм \_ системкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8d947-111">The **Msvm\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d947-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="8d947-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d947-113">Тип данных: **[ **\_ система CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="8d947-113">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="8d947-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d947-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d947-115">Родительский элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="8d947-115">The parent element in the association.</span></span> <span data-ttu-id="8d947-116">Это свойство наследуется от [**CIM \_ системкомпонент**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="8d947-116">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> <dt>

<span data-ttu-id="8d947-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8d947-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d947-118">Тип данных: **[ **CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span><span class="sxs-lookup"><span data-stu-id="8d947-118">Data type: **[**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span></span>
</dt> <dt>

<span data-ttu-id="8d947-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d947-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d947-120">Дочерний элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="8d947-120">The child element in the association.</span></span> <span data-ttu-id="8d947-121">Это свойство наследуется от [**CIM \_ системкомпонент**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="8d947-121">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d947-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8d947-122">Requirements</span></span>



| <span data-ttu-id="8d947-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8d947-123">Requirement</span></span> | <span data-ttu-id="8d947-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8d947-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d947-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d947-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8d947-126">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d947-126">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8d947-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d947-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8d947-128">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d947-128">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8d947-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8d947-129">Namespace</span></span><br/>                | <span data-ttu-id="8d947-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8d947-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8d947-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8d947-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d947-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d947-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d947-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8d947-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d947-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d947-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

