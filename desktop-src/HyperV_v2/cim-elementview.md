---
description: Представляет и взаимосвязь между представлением, а также экземпляр, представляющий нормализованное представление управляемого ресурса.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: Класс CIM_ElementView
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663481"
---
# <a name="cim_elementview-class"></a><span data-ttu-id="f21d3-103">\_Класс CIM елементвиев</span><span class="sxs-lookup"><span data-stu-id="f21d3-103">CIM\_ElementView class</span></span>

<span data-ttu-id="f21d3-104">Представляет и взаимосвязь между представлением, а также экземпляр, представляющий нормализованное представление управляемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f21d3-104">Represents and association between a view, and an instance that represents the normalized view of a managed resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f21d3-105">Syntax</span></span>

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f21d3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f21d3-106">Members</span></span>

<span data-ttu-id="f21d3-107">Класс **CIM \_ елементвиев** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f21d3-107">The **CIM\_ElementView** class has these types of members:</span></span>

-   [<span data-ttu-id="f21d3-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="f21d3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f21d3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f21d3-109">Properties</span></span>

<span data-ttu-id="f21d3-110">Класс **CIM \_ елементвиев** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f21d3-110">The **CIM\_ElementView** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f21d3-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f21d3-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f21d3-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="f21d3-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f21d3-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f21d3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f21d3-114">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f21d3-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f21d3-115">Экземпляр, представляющий нормализованное представление управляемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f21d3-115">The instance that represents the normalized view of the managed resource.</span></span>

</dd> <dt>

<span data-ttu-id="f21d3-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="f21d3-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f21d3-117">Тип данных: **\_ представление CIM**</span><span class="sxs-lookup"><span data-stu-id="f21d3-117">Data type: **CIM\_View**</span></span>
</dt> <dt>

<span data-ttu-id="f21d3-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f21d3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f21d3-119">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="f21d3-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f21d3-120">Представление, представляющее денормализованное или Статистическое представление управляемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f21d3-120">The view that represents a de-normalized or aggregate view of the managed resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f21d3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f21d3-121">Requirements</span></span>



| <span data-ttu-id="f21d3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f21d3-122">Requirement</span></span> | <span data-ttu-id="f21d3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f21d3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21d3-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f21d3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f21d3-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f21d3-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f21d3-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f21d3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f21d3-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f21d3-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f21d3-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f21d3-128">Namespace</span></span><br/>                | <span data-ttu-id="f21d3-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f21d3-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f21d3-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f21d3-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f21d3-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f21d3-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f21d3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f21d3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f21d3-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f21d3-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f21d3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f21d3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21d3-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="f21d3-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

