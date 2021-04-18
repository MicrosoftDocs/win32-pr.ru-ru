---
description: Класс CIM \_ манажеделемент является абстрактным классом, предоставляющим общий суперкласс (или вершину дерева наследования) для классов без ассоциаций в схеме CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: Класс CIM_ManagedElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682416"
---
# <a name="cim_managedelement-class"></a><span data-ttu-id="efbb3-103">\_Класс CIM манажеделемент</span><span class="sxs-lookup"><span data-stu-id="efbb3-103">CIM\_ManagedElement class</span></span>

<span data-ttu-id="efbb3-104">Класс **CIM \_ манажеделемент** является абстрактным классом, предоставляющим общий суперкласс (или вершину дерева наследования) для классов без ассоциаций в схеме CIM.</span><span class="sxs-lookup"><span data-stu-id="efbb3-104">The **CIM\_ManagedElement** class is an abstract class that provides a common superclass (or top of the inheritance tree) for the non-association classes in the CIM Schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efbb3-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="efbb3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="efbb3-106">Members</span></span>

<span data-ttu-id="efbb3-107">Класс **CIM \_ манажеделемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="efbb3-107">The **CIM\_ManagedElement** class has these types of members:</span></span>

-   [<span data-ttu-id="efbb3-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="efbb3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efbb3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="efbb3-109">Properties</span></span>

<span data-ttu-id="efbb3-110">Класс **CIM \_ манажеделемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="efbb3-110">The **CIM\_ManagedElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efbb3-111">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="efbb3-111">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbb3-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="efbb3-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbb3-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="efbb3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efbb3-114">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="efbb3-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="efbb3-115">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="efbb3-115">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="efbb3-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="efbb3-116">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbb3-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="efbb3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbb3-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="efbb3-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbb3-119">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="efbb3-119">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="efbb3-120">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="efbb3-120">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbb3-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="efbb3-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbb3-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="efbb3-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbb3-123">Понятное для пользователя имя объекта.</span><span class="sxs-lookup"><span data-stu-id="efbb3-123">A user-friendly name for the object.</span></span> <span data-ttu-id="efbb3-124">Это свойство позволяет каждому экземпляру определять понятное имя в дополнение к ключевым свойствам, данным удостоверениям и сведениям о описании.</span><span class="sxs-lookup"><span data-stu-id="efbb3-124">This property allows each instance to define a user-friendly name in addition to its key properties, identity data, and description information.</span></span>

</dd> <dt>

<span data-ttu-id="efbb3-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="efbb3-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbb3-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="efbb3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efbb3-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="efbb3-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbb3-128">Уникально и непрозрачно определяет экземпляр этого класса в области содержащего его пространства имен.</span><span class="sxs-lookup"><span data-stu-id="efbb3-128">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="efbb3-129">Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="efbb3-129">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="efbb3-130">*OrgID* должен включать в себя запись с правом или иным именем, которая принадлежит бизнес-сущности, определяющей **InstanceId**, или быть зарегистрированным идентификатором, который назначается распознанным глобальным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="efbb3-130">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="efbb3-131">Этот шаблон похож на структуру имен классов схемы.</span><span class="sxs-lookup"><span data-stu-id="efbb3-131">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="efbb3-132">Кроме того, чтобы обеспечить уникальность, первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="efbb3-132">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="efbb3-133">Поэтому *OrgID* не должен содержать двоеточие (":").</span><span class="sxs-lookup"><span data-stu-id="efbb3-133">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="efbb3-134">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.</span><span class="sxs-lookup"><span data-stu-id="efbb3-134">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="efbb3-135">Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="efbb3-135">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="efbb3-136">Для экземпляров распределенного управления Task Force (DMTF) необходимо использовать шаблон с *OrgID* , для которого задано значение CIM.</span><span class="sxs-lookup"><span data-stu-id="efbb3-136">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efbb3-137">Требования</span><span class="sxs-lookup"><span data-stu-id="efbb3-137">Requirements</span></span>



| <span data-ttu-id="efbb3-138">Требование</span><span class="sxs-lookup"><span data-stu-id="efbb3-138">Requirement</span></span> | <span data-ttu-id="efbb3-139">Значение</span><span class="sxs-lookup"><span data-stu-id="efbb3-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efbb3-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efbb3-140">Minimum supported client</span></span><br/> | <span data-ttu-id="efbb3-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="efbb3-141">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="efbb3-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efbb3-142">Minimum supported server</span></span><br/> | <span data-ttu-id="efbb3-143">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="efbb3-143">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="efbb3-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="efbb3-144">Namespace</span></span><br/>                | <span data-ttu-id="efbb3-145">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="efbb3-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="efbb3-146">MOF</span><span class="sxs-lookup"><span data-stu-id="efbb3-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efbb3-147"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efbb3-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efbb3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="efbb3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efbb3-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efbb3-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

