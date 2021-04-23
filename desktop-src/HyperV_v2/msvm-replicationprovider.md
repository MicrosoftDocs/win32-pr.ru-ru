---
description: Представляет доступные поставщики для репликации.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Класс Msvm_ReplicationProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8cc821b6bdd5d6f5d1c1085a804799c662f9d62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910139"
---
# <a name="msvm_replicationprovider-class"></a><span data-ttu-id="e8b7d-103">\_Класс мсвм репликатионпровидер</span><span class="sxs-lookup"><span data-stu-id="e8b7d-103">Msvm\_ReplicationProvider class</span></span>

<span data-ttu-id="e8b7d-104">Представляет доступные поставщики для репликации.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-104">Represents the available providers for replication.</span></span>

<span data-ttu-id="e8b7d-105">Следующий синтаксис упрощен из MOF-кода и включает эти наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-105">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b7d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8b7d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a><span data-ttu-id="e8b7d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e8b7d-107">Members</span></span>

<span data-ttu-id="e8b7d-108">Класс **мсвм \_ репликатионпровидер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e8b7d-108">The **Msvm\_ReplicationProvider** class has these types of members:</span></span>

-   [<span data-ttu-id="e8b7d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8b7d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8b7d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8b7d-110">Properties</span></span>

<span data-ttu-id="e8b7d-111">Класс **мсвм \_ репликатионпровидер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-111">The **Msvm\_ReplicationProvider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8b7d-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8b7d-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8b7d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-115">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e8b7d-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="e8b7d-116">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-116">A short description of the object.</span></span> <span data-ttu-id="e8b7d-117">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e8b7d-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="e8b7d-118">Для этого объекта значение равно:</span><span class="sxs-lookup"><span data-stu-id="e8b7d-118">For this object, the value is:</span></span>

<span data-ttu-id="e8b7d-119">"Поставщик репликации"</span><span class="sxs-lookup"><span data-stu-id="e8b7d-119">"Replication Provider"</span></span>

</dd> <dt>

<span data-ttu-id="e8b7d-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8b7d-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8b7d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8b7d-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-123">A description of the object.</span></span> <span data-ttu-id="e8b7d-124">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e8b7d-124">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="e8b7d-125">Для внешних поставщиков это значение предоставляется.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-125">For external providers, the value is provided by them.</span></span> <span data-ttu-id="e8b7d-126">Для размещения встроенного поставщика на узле используется значение:</span><span class="sxs-lookup"><span data-stu-id="e8b7d-126">For host to host inbuilt provider, the value is:</span></span>

<span data-ttu-id="e8b7d-127">"Поставщик репликации виртуальных машин для узла Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="e8b7d-127">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="e8b7d-128">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-128">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8b7d-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8b7d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8b7d-131">Отображаемое имя для поставщика конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-131">A display name for the endpoint provider.</span></span> <span data-ttu-id="e8b7d-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e8b7d-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="e8b7d-133">Для размещения встроенного поставщика на узле этому свойству всегда присваивается значение:</span><span class="sxs-lookup"><span data-stu-id="e8b7d-133">For host to host inbuilt provider, this property is always set to:</span></span>

<span data-ttu-id="e8b7d-134">"Поставщик репликации виртуальных машин для узла Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="e8b7d-134">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="e8b7d-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8b7d-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8b7d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-138">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e8b7d-138">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e8b7d-139">Идентификатор экземпляра WMI, который идентифицирует поставщик.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-139">The WMI instance ID, which identifies the provider.</span></span> <span data-ttu-id="e8b7d-140">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e8b7d-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="e8b7d-141">Это свойство имеет формат "Microsoft: <Host-Machine-Name>\\ репликатионпровидер \\<поставщик-имя>".</span><span class="sxs-lookup"><span data-stu-id="e8b7d-141">The format of this property is "Microsoft:<host-machine-name>\\ReplicationProvider\\<provider-Name>."</span></span>

</dd> <dt>

<span data-ttu-id="e8b7d-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8b7d-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8b7d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-145">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e8b7d-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e8b7d-146">Глобальный уникальный идентификатор (GUID) поставщика, который идентифицирует поставщик конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-146">The globally unique identifier (GUID) of the provider that identifies the endpoint provider.</span></span> <span data-ttu-id="e8b7d-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e8b7d-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="e8b7d-148">В случае с внешним поставщиком это свойство является идентификатором CLSID объекта класса COM поставщика.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-148">In the case of an external provider, this property is the CLSID of the provider COM class object.</span></span> <span data-ttu-id="e8b7d-149">Для размещения встроенного поставщика на узле это свойство имеет фиксированное значение:</span><span class="sxs-lookup"><span data-stu-id="e8b7d-149">For host to host inbuilt provider, this property is fixed as:</span></span>

<span data-ttu-id="e8b7d-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span><span class="sxs-lookup"><span data-stu-id="e8b7d-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span></span>

</dd> <dt>

<span data-ttu-id="e8b7d-151">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-151">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8b7d-152">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e8b7d-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e8b7d-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8b7d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8b7d-154">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-154">The current statuses of the object.</span></span> <span data-ttu-id="e8b7d-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение:</span><span class="sxs-lookup"><span data-stu-id="e8b7d-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to:</span></span>

<dl> <dt>

<span data-ttu-id="e8b7d-156"><span id="S_OK"></span><span id="s_ok"></span>**С \_ ОК** (2)</span><span class="sxs-lookup"><span data-stu-id="e8b7d-156"><span id="S_OK"></span><span id="s_ok"></span>**S\_OK** (2)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8b7d-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8b7d-157">Remarks</span></span>

<span data-ttu-id="e8b7d-158">Для включения отношения репликации можно использовать любой из доступных поставщиков и класс [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b7d-158">You can use any of available providers and the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to enable a replication relationship.</span></span> <span data-ttu-id="e8b7d-159">По умолчанию Hyper-V выбирает встроенный узел для поставщика узла, который можно изменить во время создания репликации.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-159">Hyper-V by default chooses the inbuilt host to host provider, which can be changed while creating the replication.</span></span> <span data-ttu-id="e8b7d-160">Служба управления Hyper-V взаимодействует с внешним поставщиком с помощью COM.</span><span class="sxs-lookup"><span data-stu-id="e8b7d-160">Hyper-V management service communicates with an external provider by using COM.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b7d-161">Требования</span><span class="sxs-lookup"><span data-stu-id="e8b7d-161">Requirements</span></span>



| <span data-ttu-id="e8b7d-162">Требование</span><span class="sxs-lookup"><span data-stu-id="e8b7d-162">Requirement</span></span> | <span data-ttu-id="e8b7d-163">Значение</span><span class="sxs-lookup"><span data-stu-id="e8b7d-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b7d-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8b7d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b7d-165">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8b7d-165">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e8b7d-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8b7d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b7d-167">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8b7d-167">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e8b7d-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8b7d-168">Namespace</span></span><br/>                | <span data-ttu-id="e8b7d-169">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e8b7d-169">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e8b7d-170">MOF</span><span class="sxs-lookup"><span data-stu-id="e8b7d-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8b7d-171"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8b7d-171"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8b7d-172">DLL</span><span class="sxs-lookup"><span data-stu-id="e8b7d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8b7d-173"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8b7d-173"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8b7d-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8b7d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b7d-175">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-175">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="e8b7d-176">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e8b7d-176">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

