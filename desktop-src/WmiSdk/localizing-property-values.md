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
# <a name="localizing-property-values"></a>Локализация значений свойств

Модель локализации схемы CIM предоставляет механизм локализации квалификаторов. Он не поддерживает прямую локализацию значений свойств.

Однако в некоторых случаях значения строковых свойств в статических экземплярах можно заменить на перечисляемый целочисленный тип, а для свойства в определении класса можно определить карту значений. В этих случаях квалификатор **значений** должен быть локализован. Использование квалификаторов перечисления является основным механизмом локализации значений свойств. Другие формы локализации значений свойств не поддерживаются.

В следующем примере показано, как можно локализовать статические свойства с помощью частичных карт значений с регулярными выражениями. В этом примере предопределенное подмножество значений инициализируется в схеме с помощью статических экземпляров. Остальные значения предоставляются динамически.

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

Дополнительные сведения см. в разделе [Локализация статических свойств](localizing-static-properties.md).

 

 



