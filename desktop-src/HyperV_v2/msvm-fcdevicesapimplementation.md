---
description: Представляет связь между точкой доступа службы и логическим устройством, которое ее реализует.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Класс Msvm_FcDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc40f25e3b288155e713415aa512d629b538d1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662526"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="acce8-103">\_Класс мсвм фкдевицесапимплементатион</span><span class="sxs-lookup"><span data-stu-id="acce8-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="acce8-104">Представляет связь между точкой доступа службы и логическим устройством, которое ее реализует.</span><span class="sxs-lookup"><span data-stu-id="acce8-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="acce8-105">Кратность этой ассоциации — «многие ко многим».</span><span class="sxs-lookup"><span data-stu-id="acce8-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="acce8-106">Точка доступа к службе (SAP) может предоставляться несколькими логическими устройствами, работающими совместно.</span><span class="sxs-lookup"><span data-stu-id="acce8-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="acce8-107">Любое устройство может предоставлять более одного SAP.</span><span class="sxs-lookup"><span data-stu-id="acce8-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="acce8-108">Если несколько логических устройств связаны с одним SAP, предполагается, что эти элементы работают совместно, чтобы предоставить точку доступа.</span><span class="sxs-lookup"><span data-stu-id="acce8-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="acce8-109">При наличии различных реализаций SAP каждая из этих реализаций будет создавать отдельные экземпляры объекта SAP.</span><span class="sxs-lookup"><span data-stu-id="acce8-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="acce8-110">Эти отдельные экземпляры будут иметь связи с уникальными реализациями.</span><span class="sxs-lookup"><span data-stu-id="acce8-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="acce8-111">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="acce8-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="acce8-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acce8-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="acce8-113">Члены</span><span class="sxs-lookup"><span data-stu-id="acce8-113">Members</span></span>

<span data-ttu-id="acce8-114">Класс **мсвм \_ фкдевицесапимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="acce8-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="acce8-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="acce8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acce8-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="acce8-116">Properties</span></span>

<span data-ttu-id="acce8-117">Класс **мсвм \_ фкдевицесапимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="acce8-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="acce8-118">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="acce8-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acce8-119">Тип данных: **CIM \_ фкпорт**</span><span class="sxs-lookup"><span data-stu-id="acce8-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="acce8-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="acce8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acce8-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="acce8-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="acce8-122">Ссылка на класс, производный от **CIM \_ фкпорт** , который представляет логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="acce8-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="acce8-123">**Него**</span><span class="sxs-lookup"><span data-stu-id="acce8-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acce8-124">Тип данных: **мсвм \_ фцендпоинт**</span><span class="sxs-lookup"><span data-stu-id="acce8-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="acce8-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="acce8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acce8-126">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="acce8-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="acce8-127">Ссылка на экземпляр класса [**мсвм \_ фцендпоинт**](msvm-fcendpoint.md) , представляющий SAP, использующий **предшествующую задачу**.</span><span class="sxs-lookup"><span data-stu-id="acce8-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="acce8-128">Требования</span><span class="sxs-lookup"><span data-stu-id="acce8-128">Requirements</span></span>



| <span data-ttu-id="acce8-129">Требование</span><span class="sxs-lookup"><span data-stu-id="acce8-129">Requirement</span></span> | <span data-ttu-id="acce8-130">Значение</span><span class="sxs-lookup"><span data-stu-id="acce8-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acce8-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acce8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="acce8-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="acce8-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="acce8-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acce8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="acce8-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="acce8-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="acce8-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="acce8-135">Namespace</span></span><br/>                | <span data-ttu-id="acce8-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="acce8-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="acce8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="acce8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acce8-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acce8-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="acce8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="acce8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acce8-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="acce8-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

