---
description: WMI реализует метод, позволяющий хранить в репозитории несколько локализованных версий одного и того же класса.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Локализация сведений о классе WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348395"
---
# <a name="localizing-wmi-class-information"></a><span data-ttu-id="e770a-103">Локализация сведений о классе WMI</span><span class="sxs-lookup"><span data-stu-id="e770a-103">Localizing WMI Class Information</span></span>

<span data-ttu-id="e770a-104">WMI реализует метод, позволяющий хранить в репозитории несколько локализованных версий одного и того же класса.</span><span class="sxs-lookup"><span data-stu-id="e770a-104">WMI implements a technique that allows multiple localized versions of the same class to be stored in the repository.</span></span>

<span data-ttu-id="e770a-105">Определение класса разделено на следующие версии:</span><span class="sxs-lookup"><span data-stu-id="e770a-105">The class definition is separated into the following versions:</span></span>

-   <span data-ttu-id="e770a-106">Версия, не зависящая от языка, которая содержит только определение базового класса.</span><span class="sxs-lookup"><span data-stu-id="e770a-106">A language-neutral version that contains only a basic class definition.</span></span>
-   <span data-ttu-id="e770a-107">Зависящая от языка версия, содержащая локализованные сведения, такие как описания свойств, характерные для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="e770a-107">A language-specific version that contains localized information, such as property descriptions that are specific to a locale.</span></span>

<span data-ttu-id="e770a-108">Определения классов, зависящих от языка, хранятся в дочернем пространстве имен под пространством имен, которое содержит определение базового класса, не зависящее от языка.</span><span class="sxs-lookup"><span data-stu-id="e770a-108">The language-specific class definitions are stored in a child namespace beneath the namespace that contains a language-neutral basic class definition.</span></span>

<span data-ttu-id="e770a-109">При запросе определения локализованного класса для определенного языкового стандарта Инструментарий WMI объединяет базовое определение класса и локализованную информацию о классе для формирования полного локализованного класса.</span><span class="sxs-lookup"><span data-stu-id="e770a-109">When you request a localized class definition for a specific locale, WMI combines the basic class definition and the localized class information to form a complete localized class.</span></span> <span data-ttu-id="e770a-110">Локализованную версию класса WMI можно получить, указав языковой стандарт при подключении к WMI и установив флаг, указывающий, что требуется локализованная информация.</span><span class="sxs-lookup"><span data-stu-id="e770a-110">You can get a localized version of a WMI class by specifying a locale when you connect to WMI and setting a flag that indicates that you want localized information.</span></span> <span data-ttu-id="e770a-111">Затем Инструментарий WMI объединяет информацию из языка определения класса и языковых версий определений классов для формирования локализованного класса.</span><span class="sxs-lookup"><span data-stu-id="e770a-111">WMI then merges the information from the language-neutral and the language-specific versions of the class definition to form a localized class.</span></span>

<span data-ttu-id="e770a-112">Классы WMI, содержащие локализованные сведения, помечаются **квалификатором** изменения и называются исправленными классами. класс поддерживает локализованные сведения, если он имеет этот квалификатор.</span><span class="sxs-lookup"><span data-stu-id="e770a-112">WMI classes that contain localized information are marked with the **Amendment** qualifier and are called amended classes; a class supports localized information if it has this qualifier.</span></span> <span data-ttu-id="e770a-113">Вы можете определить, какой языковой стандарт был локализован для класса, выполнив проверку другого квалификатора с именем [**locale**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="e770a-113">You can determine which locale the class has been localized for by checking for another qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span> <span data-ttu-id="e770a-114">Квалификатор языкового стандарта содержит идентификатор локализации (Windows LCID), определяющий языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="e770a-114">The locale qualifier contains a localization identifier (Windows LCID) that identifies a locale.</span></span> <span data-ttu-id="e770a-115">Например, языковой стандарт американский английский — 0x409.</span><span class="sxs-lookup"><span data-stu-id="e770a-115">For example, the locale for American English is 0x409.</span></span> <span data-ttu-id="e770a-116">Если квалификатор в исправленном классе содержит локализованные сведения, он содержит **измененную** разновидность квалификатора.</span><span class="sxs-lookup"><span data-stu-id="e770a-116">If a qualifier in an amended class contains localized information, it contains the **amended** qualifier flavor.</span></span>

<span data-ttu-id="e770a-117">Локализация WMI включает следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="e770a-117">WMI localization includes the following tasks:</span></span>

-   [<span data-ttu-id="e770a-118">Создание локализованных определений классов</span><span class="sxs-lookup"><span data-stu-id="e770a-118">Creating localized class definitions</span></span>](creating-localized-class-definitions.md)
-   [<span data-ttu-id="e770a-119">Компиляция локализованных MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="e770a-119">Compiling localized MOF files</span></span>](compiling-localized-mof-files.md)
-   [<span data-ttu-id="e770a-120">Локализация значений свойств</span><span class="sxs-lookup"><span data-stu-id="e770a-120">Localizing property values</span></span>](localizing-property-values.md)
-   [<span data-ttu-id="e770a-121">Извлечение измененных классов</span><span class="sxs-lookup"><span data-stu-id="e770a-121">Retrieving amended classes</span></span>](retrieving-amended-classes.md)

<span data-ttu-id="e770a-122">Дополнительные сведения см. в разделе [уточненные рекомендации по классам](amended-class-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="e770a-122">For more information, see [Amended Class Considerations](amended-class-considerations.md).</span></span>

 

 



