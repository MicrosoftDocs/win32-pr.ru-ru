---
description: Ассоциация между экземпляром \_ класса мсвм есернетсвитчпорт и экземпляром \_ класса мсвм есернетпортдата, который представляет данные, собранные по порту с помощью расширения коммутатора.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Класс Msvm_EthernetPortInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683551"
---
# <a name="msvm_ethernetportinfo-class"></a><span data-ttu-id="20699-103">\_Класс мсвм есернетпортинфо</span><span class="sxs-lookup"><span data-stu-id="20699-103">Msvm\_EthernetPortInfo class</span></span>

<span data-ttu-id="20699-104">Ассоциация между экземпляром класса [**мсвм \_ есернетсвитчпорт**](msvm-ethernetswitchport.md) и экземпляром класса [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md) , который представляет данные, собранные по порту с помощью расширения коммутатора.</span><span class="sxs-lookup"><span data-stu-id="20699-104">An association between an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class and an instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents data gathered about the port by a switch extension.</span></span>

<span data-ttu-id="20699-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="20699-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20699-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20699-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="20699-107">Члены</span><span class="sxs-lookup"><span data-stu-id="20699-107">Members</span></span>

<span data-ttu-id="20699-108">Класс **мсвм \_ есернетпортинфо** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="20699-108">The **Msvm\_EthernetPortInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="20699-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="20699-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20699-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="20699-110">Properties</span></span>

<span data-ttu-id="20699-111">Класс **мсвм \_ есернетпортинфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="20699-111">The **Msvm\_EthernetPortInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20699-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="20699-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20699-113">Тип данных: **мсвм \_ есернетсвитчпорт**</span><span class="sxs-lookup"><span data-stu-id="20699-113">Data type: **Msvm\_EthernetSwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="20699-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20699-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20699-115">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="20699-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="20699-116">Экземпляр класса [**мсвм \_ есернетсвитчпорт**](msvm-ethernetswitchport.md) , представляющий порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="20699-116">An instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="20699-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="20699-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20699-118">Тип данных: **мсвм \_ есернетпортдата**</span><span class="sxs-lookup"><span data-stu-id="20699-118">Data type: **Msvm\_EthernetPortData**</span></span>
</dt> <dt>

<span data-ttu-id="20699-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20699-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20699-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")</span><span class="sxs-lookup"><span data-stu-id="20699-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="20699-121">Экземпляр класса [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md) , представляющий данные порта.</span><span class="sxs-lookup"><span data-stu-id="20699-121">An instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents the port data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20699-122">Требования</span><span class="sxs-lookup"><span data-stu-id="20699-122">Requirements</span></span>



| <span data-ttu-id="20699-123">Требование</span><span class="sxs-lookup"><span data-stu-id="20699-123">Requirement</span></span> | <span data-ttu-id="20699-124">Значение</span><span class="sxs-lookup"><span data-stu-id="20699-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20699-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20699-125">Minimum supported client</span></span><br/> | <span data-ttu-id="20699-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="20699-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="20699-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20699-127">Minimum supported server</span></span><br/> | <span data-ttu-id="20699-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="20699-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20699-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="20699-129">Namespace</span></span><br/>                | <span data-ttu-id="20699-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="20699-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="20699-131">MOF</span><span class="sxs-lookup"><span data-stu-id="20699-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20699-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20699-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20699-133">DLL</span><span class="sxs-lookup"><span data-stu-id="20699-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20699-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20699-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

