---
description: Абстрактный класс для подклассов, который описывает возможности связанного управляемого элемента и возможные возможности.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: Класс CIM_Capabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683692"
---
# <a name="cim_capabilities-class"></a><span data-ttu-id="13796-103">\_Класс возможностей CIM</span><span class="sxs-lookup"><span data-stu-id="13796-103">CIM\_Capabilities class</span></span>

<span data-ttu-id="13796-104">Абстрактный класс для подклассов, который описывает возможности связанного управляемого элемента и возможные возможности.</span><span class="sxs-lookup"><span data-stu-id="13796-104">An abstract class for subclasses that describes the abilities of an associated managed element, and the potential of the abilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="13796-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13796-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="13796-106">Члены</span><span class="sxs-lookup"><span data-stu-id="13796-106">Members</span></span>

<span data-ttu-id="13796-107">Класс **\_ возможностей CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="13796-107">The **CIM\_Capabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="13796-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="13796-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13796-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="13796-109">Properties</span></span>

<span data-ttu-id="13796-110">Класс **\_ возможностей CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="13796-110">The **CIM\_Capabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13796-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="13796-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13796-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13796-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13796-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13796-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13796-114">Квалификаторы: [**обязательный**](/windows/desktop/WmiSdk/standard-qualifiers), [**переопределенный**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="13796-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="13796-115">Понятное имя для этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="13796-115">The user friendly name for this class instance.</span></span> <span data-ttu-id="13796-116">Кроме того, понятное имя пользователя можно использовать в качестве свойства индекса для запроса.</span><span class="sxs-lookup"><span data-stu-id="13796-116">In addition, the user friendly name can be used as a index property for a query.</span></span> <span data-ttu-id="13796-117">Это значение не обязательно должно быть уникальным в пределах своего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="13796-117">This value does not have to be unique within its namespace.</span></span>

</dd> <dt>

<span data-ttu-id="13796-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="13796-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13796-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13796-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13796-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13796-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13796-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="13796-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="13796-122">Уникально и непрозрачно определяет экземпляр этого класса в области содержащего его пространства имен.</span><span class="sxs-lookup"><span data-stu-id="13796-122">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="13796-123">Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="13796-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="13796-124">*OrgID* должен включать в себя запись с правом или иным именем, которая принадлежит бизнес-сущности, определяющей **InstanceId**, или быть зарегистрированным идентификатором, который назначается распознанным глобальным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="13796-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="13796-125">Этот шаблон похож на структуру имен классов схемы.</span><span class="sxs-lookup"><span data-stu-id="13796-125">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="13796-126">Кроме того, чтобы обеспечить уникальность, первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="13796-126">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="13796-127">Поэтому *OrgID* не должен содержать двоеточие (":").</span><span class="sxs-lookup"><span data-stu-id="13796-127">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="13796-128">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.</span><span class="sxs-lookup"><span data-stu-id="13796-128">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="13796-129">Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="13796-129">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="13796-130">Для экземпляров распределенного управления Task Force (DMTF) необходимо использовать шаблон с *OrgID* , для которого задано значение CIM.</span><span class="sxs-lookup"><span data-stu-id="13796-130">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13796-131">Требования</span><span class="sxs-lookup"><span data-stu-id="13796-131">Requirements</span></span>



| <span data-ttu-id="13796-132">Требование</span><span class="sxs-lookup"><span data-stu-id="13796-132">Requirement</span></span> | <span data-ttu-id="13796-133">Значение</span><span class="sxs-lookup"><span data-stu-id="13796-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13796-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13796-134">Minimum supported client</span></span><br/> | <span data-ttu-id="13796-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="13796-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="13796-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13796-136">Minimum supported server</span></span><br/> | <span data-ttu-id="13796-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13796-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="13796-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="13796-138">Namespace</span></span><br/>                | <span data-ttu-id="13796-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="13796-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13796-140">MOF</span><span class="sxs-lookup"><span data-stu-id="13796-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13796-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13796-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13796-142">DLL</span><span class="sxs-lookup"><span data-stu-id="13796-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13796-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13796-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13796-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13796-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13796-145">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="13796-145">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

