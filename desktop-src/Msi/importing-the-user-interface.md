---
description: Помимо сведений, обсуждаемых в предыдущих разделах, uisample.msi также содержит данные для примера пользовательского интерфейса.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Импорт пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897806"
---
# <a name="importing-the-user-interface"></a><span data-ttu-id="e64d3-103">Импорт пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e64d3-103">Importing the User Interface</span></span>

<span data-ttu-id="e64d3-104">Помимо сведений, обсуждаемых в предыдущих разделах, uisample.msi также содержит данные для примера пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e64d3-104">In addition to information discussed in previous sections, uisample.msi also contains data for a sample user interface.</span></span> <span data-ttu-id="e64d3-105">При объединении uisample.msi в MNP2000.msi в разделе [Импорт пустой базы данных](importing-a-blank-database.md)эти сведения также находятся в MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="e64d3-105">If you merged uisample.msi into MNP2000.msi in the section [Importing a Blank Database](importing-a-blank-database.md), then this information is present in MNP2000.msi as well.</span></span> <span data-ttu-id="e64d3-106">Сведения для примера пользовательского интерфейса приведены в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="e64d3-106">The information for the sample user interface is in the following tables.</span></span>

-   [<span data-ttu-id="e64d3-107">Таблица Актионтекст</span><span class="sxs-lookup"><span data-stu-id="e64d3-107">ActionText table</span></span>](actiontext-table.md)
-   [<span data-ttu-id="e64d3-108">Двоичная таблица</span><span class="sxs-lookup"><span data-stu-id="e64d3-108">Binary table</span></span>](binary-table.md)
-   [<span data-ttu-id="e64d3-109">Таблица управления</span><span class="sxs-lookup"><span data-stu-id="e64d3-109">Control table</span></span>](control-table.md)
-   [<span data-ttu-id="e64d3-110">Таблица таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="e64d3-110">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="e64d3-111">Таблица диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="e64d3-111">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="e64d3-112">Таблица ошибок</span><span class="sxs-lookup"><span data-stu-id="e64d3-112">Error table</span></span>](error-table.md)
-   [<span data-ttu-id="e64d3-113">Таблица Таблица eventmapping</span><span class="sxs-lookup"><span data-stu-id="e64d3-113">EventMapping table</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="e64d3-114">Таблица RadioButton</span><span class="sxs-lookup"><span data-stu-id="e64d3-114">RadioButton table</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="e64d3-115">Таблица система создала шрифт</span><span class="sxs-lookup"><span data-stu-id="e64d3-115">TextStyle table</span></span>](textstyle-table.md)
-   [<span data-ttu-id="e64d3-116">Таблица Уитекст</span><span class="sxs-lookup"><span data-stu-id="e64d3-116">UIText table</span></span>](uitext-table.md)

<span data-ttu-id="e64d3-117">Редактор базы данных Orca, поставляемый с установщиком, включает параметр Предварительный просмотр диалогового окна, который можно использовать для предварительного просмотра диалоговых окон пользовательского интерфейса, заданных в приведенных выше таблицах.</span><span class="sxs-lookup"><span data-stu-id="e64d3-117">The database editor Orca provided with the installer includes a dialog preview option that you can use to preview the dialogs of the user interface that is specified by the data in the above tables.</span></span>

<span data-ttu-id="e64d3-118">Образец установочного пакета MNP2000.msi теперь готов к проверке пакета.</span><span class="sxs-lookup"><span data-stu-id="e64d3-118">The sample installation package MNP2000.msi is now ready for package validation.</span></span> <span data-ttu-id="e64d3-119">Всегда запускайте проверку для нового пакета, прежде чем пытаться установить пакет в первый раз.</span><span class="sxs-lookup"><span data-stu-id="e64d3-119">Always run validation on a new package before attempting to install the package for the first time.</span></span> <span data-ttu-id="e64d3-120">Это рассматривается в разделе Проверка образца установки.</span><span class="sxs-lookup"><span data-stu-id="e64d3-120">This is discussed in Validating the Installation Sample.</span></span>

<span data-ttu-id="e64d3-121">Если вы не хотите включать пользовательский интерфейс в образец пакета, пропустите или удалите все сведения из приведенных выше таблиц, за исключением [таблицы система создала шрифт](textstyle-table.md) (которая необходима для определения свойства [**дефаултуифонт**](defaultuifont.md) ).</span><span class="sxs-lookup"><span data-stu-id="e64d3-121">If you do not want to include the user interface in the sample package, omit or remove the all information in the tables shown above except for the [TextStyle table](textstyle-table.md) (which is needed to define the [**DefaultUIFont**](defaultuifont.md) property).</span></span> <span data-ttu-id="e64d3-122">Также следует удалить свойства пользовательского интерфейса из [таблицы свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="e64d3-122">You should also remove user interface properties from the [Property Table](property-table.md).</span></span> <span data-ttu-id="e64d3-123">Ниже показан пример таблицы свойств для примера "Блокнот" без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e64d3-123">An example Property table for the Notepad sample, without a UI, is shown below.</span></span> <span data-ttu-id="e64d3-124">Не используйте идентификаторы GUID, показанные в таблице, если скопировать этот пример.</span><span class="sxs-lookup"><span data-stu-id="e64d3-124">Do not reuse the GUIDs shown in the table if you copy this example.</span></span>

[<span data-ttu-id="e64d3-125">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="e64d3-125">Property Table</span></span>](property-table.md)



| <span data-ttu-id="e64d3-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="e64d3-126">Property</span></span>                                   | <span data-ttu-id="e64d3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e64d3-127">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="e64d3-128">**дефаултуифонт**</span><span class="sxs-lookup"><span data-stu-id="e64d3-128">**DefaultUIFont**</span></span>](defaultuifont.md)     | <span data-ttu-id="e64d3-129">DlgFont8</span><span class="sxs-lookup"><span data-stu-id="e64d3-129">DlgFont8</span></span>                               |
| [<span data-ttu-id="e64d3-130">**инсталллевел**</span><span class="sxs-lookup"><span data-stu-id="e64d3-130">**INSTALLLEVEL**</span></span>](installlevel.md)       | <span data-ttu-id="e64d3-131">3</span><span class="sxs-lookup"><span data-stu-id="e64d3-131">3</span></span>                                      |
| [<span data-ttu-id="e64d3-132">**лимитуи**</span><span class="sxs-lookup"><span data-stu-id="e64d3-132">**LIMITUI**</span></span>](limitui.md)                 | <span data-ttu-id="e64d3-133">1</span><span class="sxs-lookup"><span data-stu-id="e64d3-133">1</span></span>                                      |
| [<span data-ttu-id="e64d3-134">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="e64d3-134">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="e64d3-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="e64d3-135">Microsoft</span></span>                              |
| [<span data-ttu-id="e64d3-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="e64d3-136">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="e64d3-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="e64d3-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> |
| [<span data-ttu-id="e64d3-138">**продуктлангуаже**</span><span class="sxs-lookup"><span data-stu-id="e64d3-138">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="e64d3-139">1033</span><span class="sxs-lookup"><span data-stu-id="e64d3-139">1033</span></span>                                   |
| [<span data-ttu-id="e64d3-140">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="e64d3-140">**ProductName**</span></span>](productname.md)         | <span data-ttu-id="e64d3-141">MNP2000</span><span class="sxs-lookup"><span data-stu-id="e64d3-141">MNP2000</span></span>                                |
| [<span data-ttu-id="e64d3-142">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="e64d3-142">**ProductVersion**</span></span>](productversion.md)   | <span data-ttu-id="e64d3-143">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="e64d3-143">01.40.0000</span></span>                             |
| [<span data-ttu-id="e64d3-144">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="e64d3-144">**UpgradeCode**</span></span>](upgradecode.md)         | <span data-ttu-id="e64d3-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="e64d3-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> |



 

<span data-ttu-id="e64d3-146">Пакет без пользовательского интерфейса можно установить из командной строки или из программы.</span><span class="sxs-lookup"><span data-stu-id="e64d3-146">A package without a user interface can be installed from the command line or from a program.</span></span> <span data-ttu-id="e64d3-147">Чтобы установить пакет из командной строки, используйте методы, описанные в разделе [Параметры командной строки](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="e64d3-147">To install a package from the command line use the methods described in [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="e64d3-148">Чтобы установить пакет из программы, используйте методы, описанные в разделе [Использование функций установщика](using-installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e64d3-148">To install a package from a program use the methods described in [Using Installer Functions](using-installer-functions.md).</span></span> <span data-ttu-id="e64d3-149">Всегда запускайте проверку в новом пакете, прежде чем пытаться установить новый пакет в первый раз.</span><span class="sxs-lookup"><span data-stu-id="e64d3-149">Always run validation on a new package before attempting to install a new package for the first time.</span></span>

[<span data-ttu-id="e64d3-150">Продолжить</span><span class="sxs-lookup"><span data-stu-id="e64d3-150">Continue</span></span>](validating-an-installation-database.md)

 

 



