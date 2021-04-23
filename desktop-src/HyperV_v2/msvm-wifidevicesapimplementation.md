---
description: Связь между точкой доступа к службе (SAP) и ее реализацией.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Класс Msvm_WiFiDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debec96efb93e60ec18d75b62ffa0d13b0e0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897230"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="e5b2d-103">\_Класс мсвм вифидевицесапимплементатион</span><span class="sxs-lookup"><span data-stu-id="e5b2d-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="e5b2d-104">Связь между точкой доступа к службе (SAP) и ее реализацией.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="e5b2d-105">Кратность этой ассоциации — «многие ко многим».</span><span class="sxs-lookup"><span data-stu-id="e5b2d-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="e5b2d-106">SAP может предоставляться более чем одним логическим устройством, работающим совместно.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="e5b2d-107">Любое устройство может предоставлять более одного SAP.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="e5b2d-108">Если несколько логических устройств связаны с одним SAP, предполагается, что эти элементы работают совместно, чтобы предоставить точку доступа.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="e5b2d-109">При наличии различных реализаций SAP каждая из этих реализаций будет создавать отдельные экземпляры объекта SAP.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="e5b2d-110">Эти отдельные экземпляры будут иметь связи с уникальными реализациями.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="e5b2d-111">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b2d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5b2d-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e5b2d-113">Члены</span><span class="sxs-lookup"><span data-stu-id="e5b2d-113">Members</span></span>

<span data-ttu-id="e5b2d-114">Класс **мсвм \_ вифидевицесапимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e5b2d-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="e5b2d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5b2d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5b2d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5b2d-116">Properties</span></span>

<span data-ttu-id="e5b2d-117">Класс **мсвм \_ вифидевицесапимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5b2d-118">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="e5b2d-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b2d-119">Тип данных: **[ **мсвм \_ вифипорт**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="e5b2d-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e5b2d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5b2d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5b2d-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e5b2d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e5b2d-122">Экземпляр класса [**мсвм \_ вифипорт**](msvm-wifiport.md) , представляющий логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="e5b2d-123">**Него**</span><span class="sxs-lookup"><span data-stu-id="e5b2d-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b2d-124">Тип данных: **[ **мсвм \_ вифиендпоинт**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="e5b2d-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e5b2d-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5b2d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5b2d-126">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="e5b2d-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e5b2d-127">Экземпляр класса [**мсвм \_ вифиендпоинт**](msvm-wifiendpoint.md) , представляющий точку доступа к службе, реализованную с помощью логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5b2d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e5b2d-128">Requirements</span></span>



| <span data-ttu-id="e5b2d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e5b2d-129">Requirement</span></span> | <span data-ttu-id="e5b2d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e5b2d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b2d-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5b2d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b2d-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e5b2d-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e5b2d-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5b2d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b2d-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e5b2d-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5b2d-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e5b2d-135">Namespace</span></span><br/>                | <span data-ttu-id="e5b2d-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e5b2d-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e5b2d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e5b2d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5b2d-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5b2d-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5b2d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e5b2d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5b2d-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5b2d-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

