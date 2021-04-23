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
# <a name="use-the-system-registry-provider-as-a-property-provider"></a><span data-ttu-id="36aa5-103">Использование поставщика системных систем в качестве поставщика свойств</span><span class="sxs-lookup"><span data-stu-id="36aa5-103">Use the System Registry Provider as a Property Provider</span></span>

<span data-ttu-id="36aa5-104">[Поставщик системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) можно использовать в качестве экземпляра или поставщика свойств.</span><span class="sxs-lookup"><span data-stu-id="36aa5-104">You can use the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) as either an instance or a property provider.</span></span>

<span data-ttu-id="36aa5-105">Если вы решили получить доступ к интерфейсам поставщика свойств, необходимо пометить классы WMI, чтобы указать вашу намерение.</span><span class="sxs-lookup"><span data-stu-id="36aa5-105">If you choose to access the property provider interfaces, you must mark your WMI classes to indicate your intention.</span></span>

<span data-ttu-id="36aa5-106">**Использование поставщика системных систем в качестве поставщика свойств**</span><span class="sxs-lookup"><span data-stu-id="36aa5-106">**To use the system registry provider as a property provider**</span></span>

-   <span data-ttu-id="36aa5-107">Определите класс WMI с помощью квалификаторов **динпропс**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)и **пропертиконтекст** Standard.</span><span class="sxs-lookup"><span data-stu-id="36aa5-107">Define your WMI class with the **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** standard qualifiers.</span></span>

    <span data-ttu-id="36aa5-108">Квалификатор **динпропс** определяет класс как имеющий свойства, поддерживаемые поставщиком свойств, идентифицируемым квалификатором [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="36aa5-108">The **DynProps** qualifier identifies a class as having properties that are maintained by the property provider identified by the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span> <span data-ttu-id="36aa5-109">Квалификатор **пропертиконтекст** задает имя значения реестра, которое будет храниться в свойстве.</span><span class="sxs-lookup"><span data-stu-id="36aa5-109">The **PropertyContext** qualifier specifies the name of the registry value to be stored by the property.</span></span> <span data-ttu-id="36aa5-110">Формат квалификатора **пропертиконтекст** совпадает с форматом квалификатора **классконтекст** с дополнительными значениями *valueName* и *Expression* .</span><span class="sxs-lookup"><span data-stu-id="36aa5-110">The format of the **PropertyContext** qualifier is the same as the format of the **ClassContext** qualifier with additional *valuename* and *expression* values.</span></span>

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    <span data-ttu-id="36aa5-111">Значения *valueName* и *Expression* являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="36aa5-111">Both *valuename* and *expression* are optional.</span></span> <span data-ttu-id="36aa5-112">Параметр *valueName* используется только в том случае, если значение реестра имеет имя.</span><span class="sxs-lookup"><span data-stu-id="36aa5-112">The *valuename* setting is only used if the registry value has a name.</span></span> <span data-ttu-id="36aa5-113">*Выражение* также является необязательным и используется для данных дескриптора ресурса.</span><span class="sxs-lookup"><span data-stu-id="36aa5-113">The *expression* is also optional and is used for resource descriptor data.</span></span> <span data-ttu-id="36aa5-114">Дополнительные сведения см. в разделе [Описание ресурса для реестра](describing-a-resource-for-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="36aa5-114">For more information, see [Describing a Resource for the Registry](describing-a-resource-for-the-registry.md).</span></span>

    <span data-ttu-id="36aa5-115">В следующем примере кода показано, как класс использует поставщик системного реестра в качестве поставщика свойств для обслуживания его неключевых свойств.</span><span class="sxs-lookup"><span data-stu-id="36aa5-115">The following code example shows how the class uses the System Registry provider as a property provider to maintain its nonkey properties.</span></span>

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

 

 
