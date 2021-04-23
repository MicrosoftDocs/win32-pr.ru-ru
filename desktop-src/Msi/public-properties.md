---
description: Общедоступные свойства могут быть созданы в базе данных установки так же, как и частные свойства.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Открытые свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822dfc55e0ab659e5580580edd04eb156540cb61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909472"
---
# <a name="public-properties"></a><span data-ttu-id="28041-103">Открытые свойства</span><span class="sxs-lookup"><span data-stu-id="28041-103">Public Properties</span></span>

<span data-ttu-id="28041-104">Общедоступные свойства могут быть созданы в базе данных установки так же, как и [частные свойства](private-properties.md).</span><span class="sxs-lookup"><span data-stu-id="28041-104">Public properties can be authored into the installation database in the same way as [private properties](private-properties.md).</span></span> <span data-ttu-id="28041-105">Кроме того, значения открытых свойств могут быть изменены пользователем или системным администратором путем задания свойства в командной строке, применения преобразования или взаимодействия с созданным пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="28041-105">In addition, the values of public properties can be changed by a user or system administrator by setting the property on the command line, by applying a transform, or by interacting with an authored user interface.</span></span> <span data-ttu-id="28041-106">Имена общедоступных свойств не могут содержать строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="28041-106">Public property names cannot contain lowercase letters.</span></span> <span data-ttu-id="28041-107">См. раздел [ограничения имен свойств](restrictions-on-property-names.md).</span><span class="sxs-lookup"><span data-stu-id="28041-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="28041-108">Общие свойства обычно устанавливаются пользователями во время установки.</span><span class="sxs-lookup"><span data-stu-id="28041-108">Public properties are commonly set by users during the installation.</span></span> <span data-ttu-id="28041-109">Например, свойство public Property [**инсталллевел**](installlevel.md) можно указать в командной строке, используемой для запуска установки или выбора с помощью созданного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="28041-109">For example, the public property [**INSTALLLEVEL**](installlevel.md) property can be specified at the command line used to launch the installation or chosen by using an authored user interface.</span></span>

<span data-ttu-id="28041-110">Значения общих свойств могут быть переопределены либо в командной строке, с помощью [стандартного](standard-actions.md) или [настраиваемого](custom-actions.md) действия, путем применения преобразования, либо путем взаимодействия пользователя с созданным пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="28041-110">Public property values can be overridden either at a command line, by using a [standard](standard-actions.md) or [custom](custom-actions.md) action, by applying a transform, or by having the user interact with an authored user interface.</span></span> <span data-ttu-id="28041-111">Чтобы очистить открытое свойство в таблице свойств, оставьте его за пределами таблицы.</span><span class="sxs-lookup"><span data-stu-id="28041-111">To clear a public property in the property table, leave it out of the table.</span></span> <span data-ttu-id="28041-112">Свойства, которые устанавливаются пользовательским интерфейсом во время установки, а затем передаются на этап выполнения установки, должны быть общедоступными.</span><span class="sxs-lookup"><span data-stu-id="28041-112">Properties that are to be set by the user interface during the installation and then passed to the execution phase of the installation must be public.</span></span>

<span data-ttu-id="28041-113">Список стандартных общих свойств, используемых установщиком, см. в [справочнике по свойствам](property-reference.md).</span><span class="sxs-lookup"><span data-stu-id="28041-113">For a list of the standard public properties used by the installer see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="28041-114">Автор может также определить пользовательское общедоступное свойство, введя имя свойства и начальное значение в [таблицу свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="28041-114">An author can also define a custom public property by entering the property's name and an initial value into the [Property table](property-table.md).</span></span> <span data-ttu-id="28041-115">Все открытые свойства могут быть переопределены всеми пользователями, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="28041-115">All public properties can be overridden by all users if any of the following conditions are true.</span></span>

-   <span data-ttu-id="28041-116">Пользователь является системным администратором.</span><span class="sxs-lookup"><span data-stu-id="28041-116">The user is a system administrator.</span></span>
-   <span data-ttu-id="28041-117">Для политики Енаблеусерконтрол на уровне компьютера задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="28041-117">The per-machine EnableUserControl policy is set to 1.</span></span> <span data-ttu-id="28041-118">См. раздел [Системная политика](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="28041-118">See [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="28041-119">Свойство [**енаблеусерконтрол**](-enableusercontrol.md) имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="28041-119">The [**EnableUserControl**](-enableusercontrol.md) property is set to 1.</span></span>
-   <span data-ttu-id="28041-120">Это Неуправляемая установка, которая не выполняется с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="28041-120">This is an unmanaged installation that is not being done with elevated privileges.</span></span>

<span data-ttu-id="28041-121">Если ни одно из перечисленных выше условий не выполняется, установщик по умолчанию будет ограничивать, какие общедоступные свойства могут быть переопределены пользователем, который не является системным администратором.</span><span class="sxs-lookup"><span data-stu-id="28041-121">If none of the above conditions are true, the installer defaults to limiting which public properties can be overridden by a user that is not a system administrator.</span></span> <span data-ttu-id="28041-122">См. раздел [**ограниченные общие свойства**](restricted-public-properties.md).</span><span class="sxs-lookup"><span data-stu-id="28041-122">See [**Restricted Public Properties**](restricted-public-properties.md).</span></span>

 

 



