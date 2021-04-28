---
description: Msvm_EthernetDeviceSAPImplementation класс — представляет связь между точкой доступа службы и логическим устройством, которое ее реализует.
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
ms.openlocfilehash: fddce9505ca2f8692044239d294904eb17c95ffa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111952"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a><span data-ttu-id="f9c53-103">\_Класс мсвм есернетдевицесапимплементатион</span><span class="sxs-lookup"><span data-stu-id="f9c53-103">Msvm\_EthernetDeviceSAPImplementation class</span></span>

<span data-ttu-id="f9c53-104">Представляет связь между точкой доступа службы и логическим устройством, которое ее реализует.</span><span class="sxs-lookup"><span data-stu-id="f9c53-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="f9c53-105">Кратность этой ассоциации — «многие ко многим».</span><span class="sxs-lookup"><span data-stu-id="f9c53-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="f9c53-106">Точка доступа к службе (SAP) может предоставляться несколькими логическими устройствами, работающими совместно.</span><span class="sxs-lookup"><span data-stu-id="f9c53-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="f9c53-107">Любое устройство может предоставлять более одного SAP.</span><span class="sxs-lookup"><span data-stu-id="f9c53-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="f9c53-108">Если несколько логических устройств связаны с одним SAP, предполагается, что эти элементы работают совместно, чтобы предоставить точку доступа.</span><span class="sxs-lookup"><span data-stu-id="f9c53-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="f9c53-109">При наличии различных реализаций SAP каждая из этих реализаций будет создавать отдельные экземпляры объекта SAP.</span><span class="sxs-lookup"><span data-stu-id="f9c53-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="f9c53-110">Эти отдельные экземпляры будут иметь связи с уникальными реализациями.</span><span class="sxs-lookup"><span data-stu-id="f9c53-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="f9c53-111">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f9c53-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c53-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9c53-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f9c53-113">Члены</span><span class="sxs-lookup"><span data-stu-id="f9c53-113">Members</span></span>

<span data-ttu-id="f9c53-114">Класс **мсвм \_ есернетдевицесапимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f9c53-114">The **Msvm\_EthernetDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="f9c53-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="f9c53-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9c53-116">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="f9c53-116">Properties</span></span>

<span data-ttu-id="f9c53-117">Класс **мсвм \_ есернетдевицесапимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f9c53-117">The **Msvm\_EthernetDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9c53-118">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f9c53-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c53-119">Тип данных: **[ **CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span><span class="sxs-lookup"><span data-stu-id="f9c53-119">Data type: **[**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span></span>
</dt> <dt>

<span data-ttu-id="f9c53-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9c53-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9c53-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f9c53-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f9c53-122">Ссылка на класс, производный от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) , который представляет логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="f9c53-122">A reference to a class derived from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="f9c53-123">**Него**</span><span class="sxs-lookup"><span data-stu-id="f9c53-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c53-124">Тип данных: **[ **мсвм \_ ланендпоинт**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="f9c53-124">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f9c53-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9c53-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9c53-126">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="f9c53-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f9c53-127">Ссылка на экземпляр класса [**мсвм \_ ланендпоинт**](msvm-lanendpoint.md) , представляющий SAP, использующий **предшествующую задачу**.</span><span class="sxs-lookup"><span data-stu-id="f9c53-127">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9c53-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f9c53-128">Requirements</span></span>



| <span data-ttu-id="f9c53-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f9c53-129">Requirement</span></span> | <span data-ttu-id="f9c53-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f9c53-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c53-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9c53-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c53-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f9c53-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f9c53-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9c53-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c53-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f9c53-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9c53-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f9c53-135">Namespace</span></span><br/>                | <span data-ttu-id="f9c53-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f9c53-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f9c53-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f9c53-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9c53-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9c53-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9c53-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c53-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9c53-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9c53-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

