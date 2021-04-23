---
description: Представляет ассоциацию, в которой управляемый элемент соответствует стандарту зарегистрированного профиля.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: Класс CIM_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662598"
---
# <a name="cim_elementconformstoprofile-class"></a><span data-ttu-id="991a5-103">\_Класс CIM елементконформстопрофиле</span><span class="sxs-lookup"><span data-stu-id="991a5-103">CIM\_ElementConformsToProfile class</span></span>

<span data-ttu-id="991a5-104">Представляет ассоциацию, в которой управляемый элемент соответствует стандарту зарегистрированного профиля.</span><span class="sxs-lookup"><span data-stu-id="991a5-104">Represents an association in which a managed element conforms to the standard of a registered profile.</span></span> <span data-ttu-id="991a5-105">Эта ассоциация обычно применяется к экземпляру более высокого уровня, например к системе, пространству имен или службе.</span><span class="sxs-lookup"><span data-stu-id="991a5-105">This association usually applies to a higher level instance, such as a system, namespace, or service.</span></span> <span data-ttu-id="991a5-106">При применении к экземпляру более высокого уровня все составные части должны вести себя соответствующим образом для обеспечения соответствия Манажеделемент с именованным Регистередпрофиле.</span><span class="sxs-lookup"><span data-stu-id="991a5-106">When applied to a higher level instance, all constituent parts MUST behave appropriately in support of the ManagedElement's conformance to the named RegisteredProfile.</span></span>

## <a name="syntax"></a><span data-ttu-id="991a5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="991a5-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="991a5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="991a5-108">Members</span></span>

<span data-ttu-id="991a5-109">Класс **CIM \_ елементконформстопрофиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="991a5-109">The **CIM\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="991a5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="991a5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="991a5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="991a5-111">Properties</span></span>

<span data-ttu-id="991a5-112">Класс **CIM \_ елементконформстопрофиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="991a5-112">The **CIM\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="991a5-113">**конформантстандард**</span><span class="sxs-lookup"><span data-stu-id="991a5-113">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="991a5-114">Тип данных: **CIM \_ регистередпрофиле**</span><span class="sxs-lookup"><span data-stu-id="991a5-114">Data type: **CIM\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="991a5-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="991a5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="991a5-116">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="991a5-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="991a5-117">Зарегистрированный профиль, которому соответствует управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="991a5-117">The registered profile to which the managed element conforms.</span></span>

</dd> <dt>

<span data-ttu-id="991a5-118">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="991a5-118">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="991a5-119">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="991a5-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="991a5-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="991a5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="991a5-121">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="991a5-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="991a5-122">Управляемый элемент, который соответствует зарегистрированному профилю.</span><span class="sxs-lookup"><span data-stu-id="991a5-122">The managed element that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="991a5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="991a5-123">Requirements</span></span>



| <span data-ttu-id="991a5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="991a5-124">Requirement</span></span> | <span data-ttu-id="991a5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="991a5-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="991a5-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="991a5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="991a5-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="991a5-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="991a5-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="991a5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="991a5-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="991a5-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="991a5-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="991a5-130">Namespace</span></span><br/>                | <span data-ttu-id="991a5-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="991a5-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="991a5-132">MOF</span><span class="sxs-lookup"><span data-stu-id="991a5-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="991a5-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="991a5-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="991a5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="991a5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="991a5-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="991a5-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

