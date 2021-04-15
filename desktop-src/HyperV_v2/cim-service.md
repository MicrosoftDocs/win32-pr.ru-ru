---
description: Представляет логический элемент, содержащий сведения для представления функциональных возможностей, предоставляемых устройством или программным обеспечением, и управления ими.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: Класс CIM_Service (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662472"
---
# <a name="cim_service-class-hyper-v-management"></a><span data-ttu-id="7dcd0-103">Класс CIM_Service (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7dcd0-103">CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="7dcd0-104">Представляет логический элемент, содержащий сведения для представления функциональных возможностей, предоставляемых устройством или программным обеспечением, и управления ими.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-104">Represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="7dcd0-105">Служба — это объект общего назначения для настройки и управления реализацией функциональности; Это не сама функциональность.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcd0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dcd0-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a><span data-ttu-id="7dcd0-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7dcd0-107">Members</span></span>

<span data-ttu-id="7dcd0-108">Класс **\_ службы CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7dcd0-108">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="7dcd0-109">Методы</span><span class="sxs-lookup"><span data-stu-id="7dcd0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7dcd0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7dcd0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7dcd0-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7dcd0-111">Methods</span></span>

<span data-ttu-id="7dcd0-112">Класс **\_ службы CIM** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-112">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="7dcd0-113">Метод</span><span class="sxs-lookup"><span data-stu-id="7dcd0-113">Method</span></span>                                           | <span data-ttu-id="7dcd0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7dcd0-114">Description</span></span>                    |
|:-------------------------------------------------|:-------------------------------|
| [<span data-ttu-id="7dcd0-115">**StartService**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-115">**StartService**</span></span>](cim-service-startservice.md) | <span data-ttu-id="7dcd0-116">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-116">Starts the service.</span></span><br/> |
| [<span data-ttu-id="7dcd0-117">**StopService**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-117">**StopService**</span></span>](cim-service-stopservice.md)   | <span data-ttu-id="7dcd0-118">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-118">Stops the service.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="7dcd0-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="7dcd0-119">Properties</span></span>

<span data-ttu-id="7dcd0-120">Класс **\_ службы CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-120">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7dcd0-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dcd0-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7dcd0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-124">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7dcd0-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7dcd0-125">Имя класса, используемое для создания экземпляра этого класса.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-125">The class name used to create an instance of this class.</span></span> <span data-ttu-id="7dcd0-126">**Свойство CreationClassName** объединяется с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-126">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd0-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-127">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dcd0-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7dcd0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-130">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7dcd0-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7dcd0-131">Уникальный идентификатор службы, указывающий функциональность службы.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-131">A unique identifier of the service that indicates the functionality of the service.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd0-132">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-132">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dcd0-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7dcd0-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-135">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="7dcd0-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="7dcd0-136">Контактные данные основного владельца службы.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-136">Contact information for the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd0-137">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-137">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dcd0-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7dcd0-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-140">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="7dcd0-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="7dcd0-141">Имя основного владельца службы.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-141">The name of the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd0-142">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-142">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dcd0-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7dcd0-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dcd0-145">**значение true** , если служба запущена; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-145">**true** if the service has been started; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd0-146">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-146">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dcd0-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7dcd0-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-149">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ Служба CIM**".**Енабледдефаулт**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="7dcd0-149">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Service**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="7dcd0-150">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-150">This property is deprecated.</span></span> <span data-ttu-id="7dcd0-151">Вместо этого используйте свойство **енабледдефаулт** , унаследованное от [**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7dcd0-151">Instead, use the **EnabledDefault** property that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="7dcd0-152">Нерекомендуемое описание: указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-152">Deprecated description: Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

 

<dt>



 <span data-ttu-id="7dcd0-153">("Автоматически")</span><span class="sxs-lookup"><span data-stu-id="7dcd0-153">("Automatic")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7dcd0-154">("Вручную")</span><span class="sxs-lookup"><span data-stu-id="7dcd0-154">("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7dcd0-155">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dcd0-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7dcd0-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-158">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="7dcd0-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="7dcd0-159">Имя класса, используемое для создания экземпляра системы, содержащей службу.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-159">The class name used to create an instance of the system that contains the service.</span></span> <span data-ttu-id="7dcd0-160">**Системкреатионкласснаме** сочетается с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-160">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd0-161">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-161">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dcd0-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7dcd0-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7dcd0-164">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="7dcd0-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="7dcd0-165">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-165">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dcd0-166">Требования</span><span class="sxs-lookup"><span data-stu-id="7dcd0-166">Requirements</span></span>



| <span data-ttu-id="7dcd0-167">Требование</span><span class="sxs-lookup"><span data-stu-id="7dcd0-167">Requirement</span></span> | <span data-ttu-id="7dcd0-168">Значение</span><span class="sxs-lookup"><span data-stu-id="7dcd0-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dcd0-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dcd0-169">Minimum supported client</span></span><br/> | <span data-ttu-id="7dcd0-170">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7dcd0-170">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7dcd0-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dcd0-171">Minimum supported server</span></span><br/> | <span data-ttu-id="7dcd0-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7dcd0-172">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7dcd0-173">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7dcd0-173">Namespace</span></span><br/>                | <span data-ttu-id="7dcd0-174">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7dcd0-174">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7dcd0-175">MOF</span><span class="sxs-lookup"><span data-stu-id="7dcd0-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7dcd0-176"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7dcd0-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7dcd0-177">DLL</span><span class="sxs-lookup"><span data-stu-id="7dcd0-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dcd0-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7dcd0-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7dcd0-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7dcd0-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dcd0-180">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="7dcd0-180">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

