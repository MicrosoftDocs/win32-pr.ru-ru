---
description: Поставщик системного реестра можно использовать в качестве экземпляра или поставщика свойств.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Использование поставщика системных систем в качестве поставщика свойств
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702653"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>Использование поставщика системных систем в качестве поставщика свойств

[Поставщик системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) можно использовать в качестве экземпляра или поставщика свойств.

Если вы решили получить доступ к интерфейсам поставщика свойств, необходимо пометить классы WMI, чтобы указать вашу намерение.

**Использование поставщика системных систем в качестве поставщика свойств**

-   Определите класс WMI с помощью квалификаторов **динпропс**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)и **пропертиконтекст** Standard.

    Квалификатор **динпропс** определяет класс как имеющий свойства, поддерживаемые поставщиком свойств, идентифицируемым квалификатором [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) . Квалификатор **пропертиконтекст** задает имя значения реестра, которое будет храниться в свойстве. Формат квалификатора **пропертиконтекст** совпадает с форматом квалификатора **классконтекст** с дополнительными значениями *valueName* и *Expression* .

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    Значения *valueName* и *Expression* являются необязательными. Параметр *valueName* используется только в том случае, если значение реестра имеет имя. *Выражение* также является необязательным и используется для данных дескриптора ресурса. Дополнительные сведения см. в разделе [Описание ресурса для реестра](describing-a-resource-for-the-registry.md).

    В следующем примере кода показано, как класс использует поставщик системного реестра в качестве поставщика свойств для обслуживания его неключевых свойств.

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
