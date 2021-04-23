---
description: Содержит сводку сведений об указанной виртуальной системе компьютера.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Класс Msvm_ComputerSystemSummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897421"
---
# <a name="msvm_computersystemsummaryinformation-class"></a><span data-ttu-id="8b51c-103">\_Класс мсвм компутерсистемсуммаринформатион</span><span class="sxs-lookup"><span data-stu-id="8b51c-103">Msvm\_ComputerSystemSummaryInformation class</span></span>

<span data-ttu-id="8b51c-104">Содержит сводку сведений об указанной виртуальной системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="8b51c-104">Contains an information summary about the specified virtual computer system.</span></span>

<span data-ttu-id="8b51c-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8b51c-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b51c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b51c-106">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8b51c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8b51c-107">Members</span></span>

<span data-ttu-id="8b51c-108">Класс **мсвм \_ компутерсистемсуммаринформатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8b51c-108">The **Msvm\_ComputerSystemSummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="8b51c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="8b51c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b51c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8b51c-110">Properties</span></span>

<span data-ttu-id="8b51c-111">Класс **мсвм \_ компутерсистемсуммаринформатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8b51c-111">The **Msvm\_ComputerSystemSummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b51c-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="8b51c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b51c-113">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="8b51c-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8b51c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8b51c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b51c-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="8b51c-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8b51c-116">Объект [**CIM \_ ComputerSystem**](cim-computersystem.md) , являющийся экземпляром в нормализованном представлении управляемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b51c-116">A [**CIM\_ComputerSystem**](cim-computersystem.md) object that is an instance in the normalized representation of the managed resource.</span></span>

> [!Note]
>
> <span data-ttu-id="8b51c-117">Тип данных, обновленный с [**мсвм \_ ComputerSystem**](msvm-computersystem.md) в Windows 10, версия 1703.</span><span class="sxs-lookup"><span data-stu-id="8b51c-117">Datatype upgraded from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b51c-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="8b51c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b51c-119">Тип данных: **мсвм \_ суммаринформатионбасе**</span><span class="sxs-lookup"><span data-stu-id="8b51c-119">Data type: **Msvm\_SummaryInformationBase**</span></span>
</dt> <dt>

<span data-ttu-id="8b51c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8b51c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b51c-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="8b51c-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8b51c-122">Экземпляр [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) , представляющий денормализованное или Статистическое представление управляемого ресурса, представленного [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , на который ссылается свойство Antecedent.</span><span class="sxs-lookup"><span data-stu-id="8b51c-122">An instance of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) that represents a de-normalized or aggregate view of the managed resource that is represented by the [**Msvm\_ComputerSystem**](msvm-computersystem.md) referenced by the Antecedent property.</span></span>

> [!Note]
>
> <span data-ttu-id="8b51c-123">Тип данных, обновленный из [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) в Windows 10, версия 1703.</span><span class="sxs-lookup"><span data-stu-id="8b51c-123">Datatype updated from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) in Windows 10, version 1703.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b51c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8b51c-124">Requirements</span></span>



| <span data-ttu-id="8b51c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8b51c-125">Requirement</span></span> | <span data-ttu-id="8b51c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8b51c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b51c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b51c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8b51c-128">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8b51c-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8b51c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b51c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8b51c-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8b51c-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8b51c-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8b51c-131">Namespace</span></span><br/>                | <span data-ttu-id="8b51c-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8b51c-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b51c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8b51c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b51c-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b51c-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b51c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8b51c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b51c-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b51c-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b51c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b51c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b51c-138">**\_ЕЛЕМЕНТВИЕВ CIM**</span><span class="sxs-lookup"><span data-stu-id="8b51c-138">**CIM\_ElementView**</span></span>](cim-elementview.md)
</dt> </dl>

 

