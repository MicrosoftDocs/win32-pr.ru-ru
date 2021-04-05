---
description: Классы, используемые для хранения данных реестра, определяются с помощью нескольких стандартных квалификаторов.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Определение класса реестра с квалификаторами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898794"
---
# <a name="defining-a-registry-class-with-qualifiers"></a><span data-ttu-id="b5814-103">Определение класса реестра с квалификаторами</span><span class="sxs-lookup"><span data-stu-id="b5814-103">Defining a Registry Class With Qualifiers</span></span>

<span data-ttu-id="b5814-104">Классы, используемые для хранения данных реестра, определяются с помощью нескольких стандартных квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="b5814-104">The classes used to hold registry data are defined with several standard qualifiers.</span></span>

<span data-ttu-id="b5814-105">Ниже приведен список стандартных квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="b5814-105">The following is a list of the standard qualifiers:</span></span>

-   <span data-ttu-id="b5814-106">[Динамический](standard-wmi-qualifiers.md) и [ **поставщик**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="b5814-106">[Dynamic](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>

    <span data-ttu-id="b5814-107">Можно присоединить **динамический** квалификатор к классу или экземпляру.</span><span class="sxs-lookup"><span data-stu-id="b5814-107">You can attach the **Dynamic** qualifier to either a class or an instance.</span></span> <span data-ttu-id="b5814-108">**Динамический** квалификатор помечает класс или экземпляр как динамически управляемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="b5814-108">The **Dynamic** qualifier marks the class or instance as managed dynamically by a provider.</span></span> <span data-ttu-id="b5814-109">Если **dynamic** отображается в классе или экземпляре, также должен быть указан квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="b5814-109">When **Dynamic** appears on a class or instance, the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier must also appear.</span></span> <span data-ttu-id="b5814-110">Квалификатор **поставщика** определяет конкретного поставщика, который должен управлять динамическим классом или экземпляром.</span><span class="sxs-lookup"><span data-stu-id="b5814-110">The **Provider** qualifier identifies the particular provider that must manage the dynamic class or instance.</span></span>

-   [<span data-ttu-id="b5814-111">классконтекст</span><span class="sxs-lookup"><span data-stu-id="b5814-111">ClassContext</span></span>](standard-wmi-qualifiers.md)

    <span data-ttu-id="b5814-112">Квалификатор **классконтекст** присоединяется к классу.</span><span class="sxs-lookup"><span data-stu-id="b5814-112">The **ClassContext** qualifier is attached to a class.</span></span> <span data-ttu-id="b5814-113">Он указывает путь к разделу реестра, который содержит сведения, представляемые классом.</span><span class="sxs-lookup"><span data-stu-id="b5814-113">It specifies the path to the registry key that contains the information the class represents.</span></span>

    <span data-ttu-id="b5814-114">Квалификатор **классконтекст** имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="b5814-114">The **ClassContext** qualifier has the following format.</span></span>

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    <span data-ttu-id="b5814-115">Значение ключевого пути может быть длинным, если оно включает ключи с подразделами.</span><span class="sxs-lookup"><span data-stu-id="b5814-115">The value for KeyPath can be long if it includes keys with subkeys.</span></span>

    <span data-ttu-id="b5814-116">В следующем примере показан квалификатор **классконтекст** , который содержит путь к конкретному транспортному устройству компьютера.</span><span class="sxs-lookup"><span data-stu-id="b5814-116">The following example shows the **ClassContext** qualifier that contains the path to a particular computer transport device.</span></span>

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

<span data-ttu-id="b5814-117">В следующем шаблоне для определения класса показано использование квалификаторов **dynamic**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)и **классконтекст** .</span><span class="sxs-lookup"><span data-stu-id="b5814-117">The following template for a class definition illustrates the use of the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **ClassContext** qualifiers.</span></span> <span data-ttu-id="b5814-118">Поставщик с именем, указанным квалификатором **поставщика** , является системным поставщиком системного реестра.</span><span class="sxs-lookup"><span data-stu-id="b5814-118">The provider named by the **Provider** qualifier is the instance System Registry provider.</span></span> <span data-ttu-id="b5814-119">Имейте в виду, что пути реестра не учитывают регистр, как и имена квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="b5814-119">Be aware that registry paths are case-insensitive, as are qualifier names.</span></span>

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

<span data-ttu-id="b5814-120">Приложения управления также могут использовать поставщик системного реестра для извлечения и изменения данных реестра для определенного ключа.</span><span class="sxs-lookup"><span data-stu-id="b5814-120">Management applications can also use the System Registry provider to retrieve and modify registry data for a particular key.</span></span>

 

 



