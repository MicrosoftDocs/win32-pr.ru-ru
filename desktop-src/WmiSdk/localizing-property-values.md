---
description: Модель локализации схемы CIM предоставляет механизм локализации квалификаторов. Он не поддерживает прямую локализацию значений свойств.
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: Локализация значений свойств
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344895"
---
# <a name="localizing-property-values"></a><span data-ttu-id="8f4a4-104">Локализация значений свойств</span><span class="sxs-lookup"><span data-stu-id="8f4a4-104">Localizing Property Values</span></span>

<span data-ttu-id="8f4a4-105">Модель локализации схемы CIM предоставляет механизм локализации квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-105">The CIM schema localization model provides a mechanism for localizing qualifiers.</span></span> <span data-ttu-id="8f4a4-106">Он не поддерживает прямую локализацию значений свойств.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-106">It does not support direct localization of property values.</span></span>

<span data-ttu-id="8f4a4-107">Однако в некоторых случаях значения строковых свойств в статических экземплярах можно заменить на перечисляемый целочисленный тип, а для свойства в определении класса можно определить карту значений.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-107">In some cases, however, the string properties values in the static instances can be replaced by an enumerated integer type and a value map can be defined for the property in the class definition.</span></span> <span data-ttu-id="8f4a4-108">В этих случаях квалификатор **значений** должен быть локализован.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-108">In these cases, the **Values** qualifier should be localized.</span></span> <span data-ttu-id="8f4a4-109">Использование квалификаторов перечисления является основным механизмом локализации значений свойств.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-109">Using enumeration qualifiers is the primary mechanism for localizing property values.</span></span> <span data-ttu-id="8f4a4-110">Другие формы локализации значений свойств не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-110">Any other forms of property value localization are not supported.</span></span>

<span data-ttu-id="8f4a4-111">В следующем примере показано, как можно локализовать статические свойства с помощью частичных карт значений с регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-111">The following example shows how static properties can be localized using partial value maps with regular expressions.</span></span> <span data-ttu-id="8f4a4-112">В этом примере предопределенное подмножество значений инициализируется в схеме с помощью статических экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-112">In this example, the predefined subset of values is initialized in the schema using static instances.</span></span> <span data-ttu-id="8f4a4-113">Остальные значения предоставляются динамически.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-113">The rest of the values are provided dynamically.</span></span>

``` syntax
[abstract]
class DataGroup
{
   [key] string GUID;
   [Description("data group display name"): Amended,
                     ValueMap{"Logical Disk",
                     "CPU Utilization", ".+"}]
                     string GroupDisplayName;
   [ValueMap{"Monitors percentage of disk free space",
                  "Monitors percentage CPU utilization", ".+"}] 
                   string GroupDescription;
};

[static, Description ("pre-configured parameters") :amended]
class InitialGroup : DataGroup {
};

[dynamic, provider("HMProvider"),
    Description ("user-defined parameters") :amended]
class UserDefionedGroup : DataGroup {
};

instance of InitialGroup {
   GUID = "abc";
   GroupDisplayName = "Logical Disk";
   GroupDescription = "Monitors percentage of disk free space";
};

instance of InitialGroup {
   GUID = "def";
   GroupDisplayName = "CPU Utilization";
   GroupDescription = "Monitors percentage CPU utilization";
};
```

<span data-ttu-id="8f4a4-114">Дополнительные сведения см. в разделе [Локализация статических свойств](localizing-static-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8f4a4-114">For more information, see [Localizing Static Properties](localizing-static-properties.md).</span></span>

 

 



