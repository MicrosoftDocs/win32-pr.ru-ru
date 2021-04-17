---
description: Определяет средства, с помощью которых клиент может обнаружить допустимый диапазон параметров по умолчанию для функции коммутатора Ethernet.
ms.assetid: 84ae7656-2cc4-4ca7-b4ae-95d9905c9aad
title: Класс Msvm_EthernetSwitchFeatureCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureCapabilities
- Msvm_EthernetSwitchFeatureCapabilities.InstanceID
- Msvm_EthernetSwitchFeatureCapabilities.Caption
- Msvm_EthernetSwitchFeatureCapabilities.Description
- Msvm_EthernetSwitchFeatureCapabilities.ElementName
- Msvm_EthernetSwitchFeatureCapabilities.FeatureId
- Msvm_EthernetSwitchFeatureCapabilities.Applicability
- Msvm_EthernetSwitchFeatureCapabilities.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba145ca6a43a2031a676e565f38210dc6771f40e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664772"
---
# <a name="msvm_ethernetswitchfeaturecapabilities-class"></a><span data-ttu-id="e435e-103">\_Класс мсвм есернетсвитчфеатурекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="e435e-103">Msvm\_EthernetSwitchFeatureCapabilities class</span></span>

<span data-ttu-id="e435e-104">Определяет средства, с помощью которых клиент может обнаружить допустимый диапазон параметров по умолчанию для функции коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e435e-104">Defines the means by which a client can discover the valid range of default settings for an Ethernet switch feature.</span></span> <span data-ttu-id="e435e-105">Объект **\_ есернетсвитчфеатурекапабилитиес мсвм** связан с каждым виртуальным коммутатором Ethernet для каждого компонента, поддерживаемого коммутатором.</span><span class="sxs-lookup"><span data-stu-id="e435e-105">An **Msvm\_EthernetSwitchFeatureCapabilities** object is associated with each virtual Ethernet switch, for each feature that the switch supports.</span></span> <span data-ttu-id="e435e-106">С объектом **мсвм \_ есернетсвитчфеатурекапабилитиес** связано четыре объекта [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md) , которые описывают минимальное, максимальное, по умолчанию и добавочные значения для функций данного коммутатора.</span><span class="sxs-lookup"><span data-stu-id="e435e-106">Four [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) objects are associated with the **Msvm\_EthernetSwitchFeatureCapabilities** object to describe the minimum, maximum, default, and incremental values for the given switch's feature capabilities.</span></span>

<span data-ttu-id="e435e-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e435e-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e435e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e435e-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = " Ethernet Switch Feature Capabilities";
  string Description = "Microsoft Virtual Ethernet Switch Feature Capabilities";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  string FeatureId;
  uint16 Applicability;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="e435e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e435e-109">Members</span></span>

<span data-ttu-id="e435e-110">Класс **мсвм \_ есернетсвитчфеатурекапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e435e-110">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="e435e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e435e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e435e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e435e-112">Properties</span></span>

<span data-ttu-id="e435e-113">Класс **мсвм \_ есернетсвитчфеатурекапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e435e-113">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e435e-114">**Квартал**</span><span class="sxs-lookup"><span data-stu-id="e435e-114">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e435e-115">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e435e-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e435e-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e435e-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e435e-117">Описывает, применяется ли эта функция к коммутатору Ethernet или к конкретному порту коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e435e-117">Describes whether this feature is applied to an Ethernet switch or a particular Ethernet switch port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e435e-118">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e435e-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Port"></span><span id="port"></span><span id="PORT"></span>

<span data-ttu-id="e435e-119">**Порт** (1)</span><span class="sxs-lookup"><span data-stu-id="e435e-119">**Port** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="e435e-120">**Switch** (2)</span><span class="sxs-lookup"><span data-stu-id="e435e-120">**Switch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e435e-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e435e-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e435e-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e435e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e435e-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e435e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e435e-124">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e435e-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="e435e-125">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e435e-125">A short description of the object.</span></span> <span data-ttu-id="e435e-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e435e-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e435e-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e435e-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e435e-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e435e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e435e-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e435e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e435e-130">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e435e-130">A description of the object.</span></span> <span data-ttu-id="e435e-131">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e435e-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e435e-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e435e-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e435e-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e435e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e435e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e435e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e435e-135">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e435e-135">A display name for the object.</span></span> <span data-ttu-id="e435e-136">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e435e-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e435e-137">**феатуреид**</span><span class="sxs-lookup"><span data-stu-id="e435e-137">**FeatureId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e435e-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e435e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e435e-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e435e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e435e-140">Идентификатор компонента, для которого этот объект предоставляет сведения о возможностях.</span><span class="sxs-lookup"><span data-stu-id="e435e-140">The identifier of the feature this object provides capabilities information for.</span></span>

</dd> <dt>

<span data-ttu-id="e435e-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e435e-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e435e-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e435e-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e435e-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e435e-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e435e-144">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e435e-144">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e435e-145">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e435e-145">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e435e-146">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e435e-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e435e-147">**Version**</span><span class="sxs-lookup"><span data-stu-id="e435e-147">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e435e-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e435e-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e435e-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e435e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e435e-150">Версия компонента в формате "основной. дополнительный", например "2,0".</span><span class="sxs-lookup"><span data-stu-id="e435e-150">The version of the feature in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e435e-151">Требования</span><span class="sxs-lookup"><span data-stu-id="e435e-151">Requirements</span></span>



| <span data-ttu-id="e435e-152">Требование</span><span class="sxs-lookup"><span data-stu-id="e435e-152">Requirement</span></span> | <span data-ttu-id="e435e-153">Значение</span><span class="sxs-lookup"><span data-stu-id="e435e-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e435e-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e435e-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e435e-155">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e435e-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e435e-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e435e-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e435e-157">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e435e-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e435e-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e435e-158">Namespace</span></span><br/>                | <span data-ttu-id="e435e-159">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e435e-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e435e-160">MOF</span><span class="sxs-lookup"><span data-stu-id="e435e-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e435e-161"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e435e-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e435e-162">DLL</span><span class="sxs-lookup"><span data-stu-id="e435e-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e435e-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e435e-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

