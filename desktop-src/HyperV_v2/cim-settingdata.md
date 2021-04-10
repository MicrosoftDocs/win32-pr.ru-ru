---
description: Представляет конфигурацию и операционные параметры для \_ экземпляров МАНАЖЕДЕЛЕМЕНТ CIM.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: Класс CIM_SettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265059"
---
# <a name="cim_settingdata-class"></a><span data-ttu-id="1fb68-103">\_Класс SETTINGDATA CIM</span><span class="sxs-lookup"><span data-stu-id="1fb68-103">CIM\_SettingData class</span></span>

<span data-ttu-id="1fb68-104">Представляет конфигурацию и операционные параметры для экземпляров [**\_ манажеделемент CIM**](cim-managedelement.md) .</span><span class="sxs-lookup"><span data-stu-id="1fb68-104">Represents configuration and operational parameters for [**CIM\_ManagedElement**](cim-managedelement.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fb68-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="1fb68-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1fb68-106">Members</span></span>

<span data-ttu-id="1fb68-107">Класс **\_ SettingData CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1fb68-107">The **CIM\_SettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1fb68-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fb68-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1fb68-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fb68-109">Properties</span></span>

<span data-ttu-id="1fb68-110">Класс **\_ SettingData CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="1fb68-110">The **CIM\_SettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fb68-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1fb68-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb68-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fb68-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb68-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fb68-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fb68-114">Квалификаторы: [**обязательный**](/windows/desktop/WmiSdk/standard-qualifiers), [**переопределенный**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="1fb68-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="1fb68-115">Понятное имя для экземпляра этого класса.</span><span class="sxs-lookup"><span data-stu-id="1fb68-115">The user-friendly name for an instance of this class.</span></span> <span data-ttu-id="1fb68-116">Кроме того, понятное имя может использоваться в качестве индекса для поиска или запроса.</span><span class="sxs-lookup"><span data-stu-id="1fb68-116">In addition, the user-friendly name can be used as an index for a search or query.</span></span> <span data-ttu-id="1fb68-117">Имя не обязательно должно быть уникальным в пределах пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1fb68-117">The name does not have to be unique within a namespace.</span></span>

</dd> <dt>

<span data-ttu-id="1fb68-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1fb68-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb68-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fb68-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb68-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fb68-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fb68-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="1fb68-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="1fb68-122">Уникально идентифицирует экземпляр этого класса в области содержащего его пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1fb68-122">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1fb68-123">Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="1fb68-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="1fb68-124">*OrgID* должен включать уникальное имя, присвоенное товару или иным способом, которое принадлежит бизнес-сущности, определяющей свойство **InstanceId** , или быть зарегистрированным идентификатором, назначенным распознанным глобальным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="1fb68-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="1fb68-125">*OrgID* не должно содержать двоеточие.</span><span class="sxs-lookup"><span data-stu-id="1fb68-125">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="1fb68-126">Первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="1fb68-126">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="1fb68-127">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.</span><span class="sxs-lookup"><span data-stu-id="1fb68-127">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="1fb68-128">Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1fb68-128">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="1fb68-129">Для экземпляров, определенных DMTF, шаблон должен использоваться с *OrgID* , для которого задано значение "CIM".</span><span class="sxs-lookup"><span data-stu-id="1fb68-129">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fb68-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1fb68-130">Requirements</span></span>



| <span data-ttu-id="1fb68-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1fb68-131">Requirement</span></span> | <span data-ttu-id="1fb68-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1fb68-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb68-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fb68-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb68-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1fb68-134">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1fb68-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fb68-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb68-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fb68-136">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1fb68-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1fb68-137">Namespace</span></span><br/>                | <span data-ttu-id="1fb68-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1fb68-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1fb68-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1fb68-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fb68-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fb68-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fb68-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1fb68-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fb68-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1fb68-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1fb68-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fb68-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb68-144">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="1fb68-144">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

