---
description: Представляет связь между точкой доступа службы и логическим устройством, которое ее реализует.
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Класс Msvm_EthernetDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 96290eb0d572f4848fbf3805a44ce0ae173892c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345785"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a><span data-ttu-id="d405f-103">\_Класс мсвм есернетдевицесапимплементатион</span><span class="sxs-lookup"><span data-stu-id="d405f-103">Msvm\_EthernetDeviceSAPImplementation class</span></span>

<span data-ttu-id="d405f-104">Представляет связь между точкой доступа службы и логическим устройством, которое ее реализует.</span><span class="sxs-lookup"><span data-stu-id="d405f-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="d405f-105">Кратность этой ассоциации — «многие ко многим».</span><span class="sxs-lookup"><span data-stu-id="d405f-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="d405f-106">Точка доступа к службе (SAP) может предоставляться несколькими логическими устройствами, работающими совместно.</span><span class="sxs-lookup"><span data-stu-id="d405f-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="d405f-107">Любое устройство может предоставлять более одного SAP.</span><span class="sxs-lookup"><span data-stu-id="d405f-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="d405f-108">Если несколько логических устройств связаны с одним SAP, предполагается, что эти элементы работают совместно, чтобы предоставить точку доступа.</span><span class="sxs-lookup"><span data-stu-id="d405f-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="d405f-109">При наличии различных реализаций SAP каждая из этих реализаций будет создавать отдельные экземпляры объекта SAP.</span><span class="sxs-lookup"><span data-stu-id="d405f-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="d405f-110">Эти отдельные экземпляры будут иметь связи с уникальными реализациями.</span><span class="sxs-lookup"><span data-stu-id="d405f-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="d405f-111">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d405f-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d405f-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d405f-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d405f-113">Члены</span><span class="sxs-lookup"><span data-stu-id="d405f-113">Members</span></span>

<span data-ttu-id="d405f-114">Класс **мсвм \_ есернетдевицесапимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d405f-114">The **Msvm\_EthernetDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="d405f-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="d405f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d405f-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="d405f-116">Properties</span></span>

<span data-ttu-id="d405f-117">Класс **мсвм \_ есернетдевицесапимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d405f-117">The **Msvm\_EthernetDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d405f-118">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="d405f-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d405f-119">Тип данных: **[ **CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span><span class="sxs-lookup"><span data-stu-id="d405f-119">Data type: **[**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span></span>
</dt> <dt>

<span data-ttu-id="d405f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d405f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d405f-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d405f-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d405f-122">Ссылка на класс, производный от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) , который представляет логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="d405f-122">A reference to a class derived from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="d405f-123">**Него**</span><span class="sxs-lookup"><span data-stu-id="d405f-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d405f-124">Тип данных: **[ **мсвм \_ ланендпоинт**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="d405f-124">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="d405f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d405f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d405f-126">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="d405f-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d405f-127">Ссылка на экземпляр класса [**мсвм \_ ланендпоинт**](msvm-lanendpoint.md) , представляющий SAP, использующий **предшествующую задачу**.</span><span class="sxs-lookup"><span data-stu-id="d405f-127">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d405f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d405f-128">Requirements</span></span>



| <span data-ttu-id="d405f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d405f-129">Requirement</span></span> | <span data-ttu-id="d405f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d405f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d405f-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d405f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d405f-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d405f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d405f-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d405f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d405f-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d405f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d405f-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d405f-135">Namespace</span></span><br/>                | <span data-ttu-id="d405f-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d405f-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d405f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d405f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d405f-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d405f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d405f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d405f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d405f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d405f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

