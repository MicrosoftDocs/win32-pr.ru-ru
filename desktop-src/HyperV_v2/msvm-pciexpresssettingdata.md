---
description: Представляет настроенное состояние порта PCI Express.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Класс Msvm_PciExpressSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684461"
---
# <a name="msvm_pciexpresssettingdata-class"></a><span data-ttu-id="fbf03-103">\_Класс мсвм пЦиекспресссеттингдата</span><span class="sxs-lookup"><span data-stu-id="fbf03-103">Msvm\_PciExpressSettingData class</span></span>

<span data-ttu-id="fbf03-104">Представляет настроенное состояние порта PCI Express.</span><span class="sxs-lookup"><span data-stu-id="fbf03-104">Represents the configured state of a PCI Express port.</span></span>

<span data-ttu-id="fbf03-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fbf03-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf03-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbf03-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="fbf03-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fbf03-107">Members</span></span>

<span data-ttu-id="fbf03-108">Класс **мсвм \_ пЦиекспресссеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fbf03-108">The **Msvm\_PciExpressSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fbf03-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="fbf03-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbf03-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fbf03-110">Properties</span></span>

<span data-ttu-id="fbf03-111">Класс **мсвм \_ пЦиекспресссеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fbf03-111">The **Msvm\_PciExpressSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fbf03-112">**виртуалфунктионс**</span><span class="sxs-lookup"><span data-stu-id="fbf03-112">**VirtualFunctions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf03-113">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="fbf03-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf03-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fbf03-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fbf03-115">Номер виртуальной функции, которую необходимо назначить виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fbf03-115">The virtual function number to assign to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="fbf03-116">**виртуалсистемидентифиерс**</span><span class="sxs-lookup"><span data-stu-id="fbf03-116">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf03-117">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="fbf03-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf03-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fbf03-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf03-119">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="fbf03-119">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fbf03-120">Строковый массив идентификаторов этого ресурса в свободной форме, представленный операционной системе виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="fbf03-120">A free-form string array of identifiers of this resource presented to the virtual computer system's operating system.</span></span> <span data-ttu-id="fbf03-121">Индексы и значения для каждого индекса определяются для каждого ресурса (то есть для каждого перечислимого **значения типа ресурса)** .</span><span class="sxs-lookup"><span data-stu-id="fbf03-121">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="fbf03-122">Для этого свойства задано значение "GUID".</span><span class="sxs-lookup"><span data-stu-id="fbf03-122">This property is set to "GUID".</span></span>

<span data-ttu-id="fbf03-123">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифивиртуалсистемресаурцес**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) класса SD.</span><span class="sxs-lookup"><span data-stu-id="fbf03-123">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the sd class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbf03-124">Требования</span><span class="sxs-lookup"><span data-stu-id="fbf03-124">Requirements</span></span>



| <span data-ttu-id="fbf03-125">Требование</span><span class="sxs-lookup"><span data-stu-id="fbf03-125">Requirement</span></span> | <span data-ttu-id="fbf03-126">Значение</span><span class="sxs-lookup"><span data-stu-id="fbf03-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf03-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbf03-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf03-128">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="fbf03-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fbf03-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbf03-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf03-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fbf03-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fbf03-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fbf03-131">Namespace</span></span><br/>                | <span data-ttu-id="fbf03-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fbf03-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fbf03-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf03-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf03-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf03-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf03-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf03-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf03-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbf03-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbf03-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbf03-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf03-138">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="fbf03-138">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

