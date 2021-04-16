---
description: Этот класс устарел. Вместо этого рекомендуется создавать производные от \_ класса службы CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: Класс CIM_NetworkService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684282"
---
# <a name="cim_networkservice-class"></a><span data-ttu-id="bd913-104">\_Класс сетевой NetworkService CIM</span><span class="sxs-lookup"><span data-stu-id="bd913-104">CIM\_NetworkService class</span></span>

<span data-ttu-id="bd913-105">Этот класс устарел.</span><span class="sxs-lookup"><span data-stu-id="bd913-105">This class is deprecated.</span></span> <span data-ttu-id="bd913-106">Вместо этого рекомендуется создавать производные от класса [**\_ службы CIM**](cim-service.md) .</span><span class="sxs-lookup"><span data-stu-id="bd913-106">Instead, we recommend deriving from the [**CIM\_Service**](cim-service.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd913-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd913-107">Syntax</span></span>

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a><span data-ttu-id="bd913-108">Члены</span><span class="sxs-lookup"><span data-stu-id="bd913-108">Members</span></span>

<span data-ttu-id="bd913-109">Класс **\_ NetworkService CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bd913-109">The **CIM\_NetworkService** class has these types of members:</span></span>

-   [<span data-ttu-id="bd913-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="bd913-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd913-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="bd913-111">Properties</span></span>

<span data-ttu-id="bd913-112">Класс **\_ NetworkService CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="bd913-112">The **CIM\_NetworkService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd913-113">**Ключевые слова**</span><span class="sxs-lookup"><span data-stu-id="bd913-113">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd913-114">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="bd913-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bd913-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd913-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd913-116">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")</span><span class="sxs-lookup"><span data-stu-id="bd913-116">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="bd913-117">Это свойство является устаревшим и не должно использоваться.</span><span class="sxs-lookup"><span data-stu-id="bd913-117">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="bd913-118">Нерекомендуемое описание: массив ключевых слов, которые могут использоваться в запросах.</span><span class="sxs-lookup"><span data-stu-id="bd913-118">Deprecated description: An array of keywords that can be used in queries.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd913-119">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="bd913-119">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd913-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd913-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd913-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd913-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd913-122">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ сервицеакцессури")</span><span class="sxs-lookup"><span data-stu-id="bd913-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_ServiceAccessURI")</span></span>
</dt> </dl>

<span data-ttu-id="bd913-123">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="bd913-123">This property is deprecated.</span></span> <span data-ttu-id="bd913-124">Вместо этого рекомендуется использовать класс **CIM \_ сервицеакцессури** .</span><span class="sxs-lookup"><span data-stu-id="bd913-124">Instead, we recommend the **CIM\_ServiceAccessURI** class.</span></span>

> [!Note]  
> <span data-ttu-id="bd913-125">Нерекомендуемое описание: URL-адрес, предоставляющий протокол, сетевое расположение и другие сведения, относящиеся к службе, необходимые для доступа к службе.</span><span class="sxs-lookup"><span data-stu-id="bd913-125">Deprecated description: A URL that provides the protocol, network location, and other service-specific information required in order to access the service.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd913-126">**стартупкондитионс**</span><span class="sxs-lookup"><span data-stu-id="bd913-126">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd913-127">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="bd913-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bd913-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd913-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd913-129">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")</span><span class="sxs-lookup"><span data-stu-id="bd913-129">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="bd913-130">Это свойство является устаревшим и не должно использоваться.</span><span class="sxs-lookup"><span data-stu-id="bd913-130">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="bd913-131">Нерекомендуемое описание: предварительные условия, которые должны быть выполнены, чтобы эта служба запускалась правильно.</span><span class="sxs-lookup"><span data-stu-id="bd913-131">Deprecated description: The pre-conditions that must be met in order for this service to start correctly.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd913-132">**стартуппараметерс**</span><span class="sxs-lookup"><span data-stu-id="bd913-132">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd913-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="bd913-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bd913-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd913-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd913-135">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")</span><span class="sxs-lookup"><span data-stu-id="bd913-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="bd913-136">Это свойство является устаревшим и не должно использоваться.</span><span class="sxs-lookup"><span data-stu-id="bd913-136">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="bd913-137">Нерекомендуемое описание: параметры, которые должны быть передаются методу **StartService** для правильной работы этой службы.</span><span class="sxs-lookup"><span data-stu-id="bd913-137">Deprecated description: The parameters that must be supplied to the **StartService** method in order for this service to start correctly.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd913-138">Требования</span><span class="sxs-lookup"><span data-stu-id="bd913-138">Requirements</span></span>



| <span data-ttu-id="bd913-139">Требование</span><span class="sxs-lookup"><span data-stu-id="bd913-139">Requirement</span></span> | <span data-ttu-id="bd913-140">Значение</span><span class="sxs-lookup"><span data-stu-id="bd913-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd913-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd913-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bd913-142">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bd913-142">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bd913-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd913-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bd913-144">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bd913-144">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bd913-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bd913-145">Namespace</span></span><br/>                | <span data-ttu-id="bd913-146">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bd913-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bd913-147">MOF</span><span class="sxs-lookup"><span data-stu-id="bd913-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd913-148"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd913-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd913-149">DLL</span><span class="sxs-lookup"><span data-stu-id="bd913-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd913-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bd913-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bd913-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd913-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd913-152">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="bd913-152">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

