---
description: Коллекция SNMP сопоставляется с классом CIM, а элементы коллекции сопоставляются со свойствами класса CIM. Все созданные определения класса CIM должны быть производными от класса Снмпобжекттипе.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Коллекции SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711658"
---
# <a name="snmp-collections"></a><span data-ttu-id="8f656-104">Коллекции SNMP</span><span class="sxs-lookup"><span data-stu-id="8f656-104">SNMP Collections</span></span>

<span data-ttu-id="8f656-105">Коллекция SNMP сопоставляется с классом CIM, а элементы коллекции сопоставляются со свойствами класса CIM.</span><span class="sxs-lookup"><span data-stu-id="8f656-105">An SNMP collection maps to a CIM class and the elements of a collection map to the properties of a CIM class.</span></span> <span data-ttu-id="8f656-106">Все созданные определения класса CIM должны быть производными от класса **снмпобжекттипе** .</span><span class="sxs-lookup"><span data-stu-id="8f656-106">All generated CIM class definitions must be derived from the **SnmpObjectType** class.</span></span>

> [!Note]  
> <span data-ttu-id="8f656-107">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8f656-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="8f656-108">Следующие определения классов являются родительскими для всех созданных определений классов:</span><span class="sxs-lookup"><span data-stu-id="8f656-108">The following class definitions parent all generated class definitions:</span></span>

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a><span data-ttu-id="8f656-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f656-109">Remarks</span></span>

<span data-ttu-id="8f656-110">При сопоставлении коллекций SNMP с классами CIM применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="8f656-110">The following rules apply when mapping SNMP collections to CIM classes.</span></span> <span data-ttu-id="8f656-111">Если не указано иное, эти правила применяются как к скалярным, так и к коллекциям таблиц:</span><span class="sxs-lookup"><span data-stu-id="8f656-111">Unless otherwise specified, these rules apply to both scalar and table collections:</span></span>

-   <span data-ttu-id="8f656-112">Процесс сопоставления создает имена классов CIM, объединяя "SNMP \_ ", имя удостоверения модуля MIB, " \_ " и дескриптор объекта коллекции.</span><span class="sxs-lookup"><span data-stu-id="8f656-112">The mapping process generates CIM class names by concatenating "SNMP\_", the MIB module identity name, "\_", and the collection's object descriptor.</span></span>

    <span data-ttu-id="8f656-113">Например: **система** преобразуется в **\_ \_ \_ систему SNMP RFC1213 MIB**, тогда как **ифтабле** преобразуется в **SNMP \_ RFC1213 \_ MIB \_ ифтабле**.</span><span class="sxs-lookup"><span data-stu-id="8f656-113">For example: **system** translates to **SNMP\_RFC1213\_MIB\_system**, while **ifTable** translates to **SNMP\_RFC1213\_MIB\_ifTable**.</span></span>

-   <span data-ttu-id="8f656-114">Во всех случаях дефисы (-) в идентификаторах SNMP MIB сопоставляются с символами подчеркивания ( \_ ) в именах классов CIM.</span><span class="sxs-lookup"><span data-stu-id="8f656-114">In all cases, hyphens (-) in SNMP MIB identifiers map to underscores (\_) in CIM class names.</span></span>
-   <span data-ttu-id="8f656-115">Конфликты имен могут возникать из-за учета регистра в имени CIM.</span><span class="sxs-lookup"><span data-stu-id="8f656-115">Naming conflicts can occur due to CIM name case-insensitivity.</span></span> <span data-ttu-id="8f656-116">При возникновении конфликта имен поставщик выбирает одно из конфликтующих определений групп и игнорирует остальные определения.</span><span class="sxs-lookup"><span data-stu-id="8f656-116">If a naming conflict occurs, the provider chooses one of the conflicting group definitions and ignores the remaining definitions.</span></span>
-   <span data-ttu-id="8f656-117">Имя удостоверения модуля MIB, содержащего коллекцию, сопоставляется с **\_ именем модуля** квалификатора класса CIM.</span><span class="sxs-lookup"><span data-stu-id="8f656-117">The identity name of the MIB module that contains the collection maps to the CIM class qualifier **Module\_Name**.</span></span>
-   <span data-ttu-id="8f656-118">Идентификатор объекта собранной коллекции сопоставляется с **\_ ObjectID группы** квалификаторов класса CIM.</span><span class="sxs-lookup"><span data-stu-id="8f656-118">The object identifier of the fabricated collection maps to the CIM class qualifier **Group\_Objectid**.</span></span>
-   <span data-ttu-id="8f656-119">Список импорта модуля MIB (полученный из определения макроса **удостоверения модуля** ) сопоставляется с **\_ импортируемыми модулями** квалификатора класса CIM.</span><span class="sxs-lookup"><span data-stu-id="8f656-119">The MIB module imports list (obtained from the **MODULE-IDENTITY** macro definition) maps to the CIM class qualifier **module\_imports**.</span></span> <span data-ttu-id="8f656-120">Этот квалификатор содержит разделенный запятыми список имен модулей.</span><span class="sxs-lookup"><span data-stu-id="8f656-120">This qualifier contains a comma-separated list of module names.</span></span>

 

 



