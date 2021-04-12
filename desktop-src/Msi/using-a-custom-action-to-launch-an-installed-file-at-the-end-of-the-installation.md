---
description: В следующем примере показано, как запустить HTML-файл в конце установки.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Использование настраиваемого действия для запуска установленного файла в конце установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265410"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a><span data-ttu-id="38ec1-103">Использование настраиваемого действия для запуска установленного файла в конце установки</span><span class="sxs-lookup"><span data-stu-id="38ec1-103">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>

<span data-ttu-id="38ec1-104">В следующем примере показано, как запустить HTML-файл в конце установки.</span><span class="sxs-lookup"><span data-stu-id="38ec1-104">The following example illustrates how to launch an HTML file at the end of an installation.</span></span> <span data-ttu-id="38ec1-105">Установщик устанавливает компонент, содержащий файл, а затем публикует событие элемента управления в конце установки для запуска настраиваемого действия, открывающего файл.</span><span class="sxs-lookup"><span data-stu-id="38ec1-105">The Installer installs the component that contains the file, and then publishes a control event at the end of the installation to run a custom action that opens the file.</span></span> <span data-ttu-id="38ec1-106">Этот подход можно использовать для запуска учебника по завершении первой установки приложения.</span><span class="sxs-lookup"><span data-stu-id="38ec1-106">This approach may be used to launch a help tutorial at the end of the first installation of an application.</span></span>

<span data-ttu-id="38ec1-107">Пример должен соответствовать следующим спецификациям.</span><span class="sxs-lookup"><span data-stu-id="38ec1-107">The sample must meet the following specifications.</span></span>

-   <span data-ttu-id="38ec1-108">Установщик выполняет пользовательское действие только в том случае, если для установки приложения используется [*полный уровень пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="38ec1-108">The Installer executes the custom action only if the [*full UI*](f-gly.md) level is used to install an application.</span></span>
-   <span data-ttu-id="38ec1-109">Установщик выполняет пользовательское действие только в том случае, если компонент, содержащий HTML-файл, установлен для локального запуска на компьютере.</span><span class="sxs-lookup"><span data-stu-id="38ec1-109">The Installer executes the custom action only if the component that contains the HTML file is installed to run locally on the computer.</span></span>
-   <span data-ttu-id="38ec1-110">Настраиваемое действие выполняется только при первой установке приложения.</span><span class="sxs-lookup"><span data-stu-id="38ec1-110">The custom action only runs on the first installation of the application.</span></span>
-   <span data-ttu-id="38ec1-111">При сбое настраиваемого действия установка не завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="38ec1-111">The installation does not fail if the custom action fails.</span></span>

<span data-ttu-id="38ec1-112">Пример включает гипотетический компонент с именем Tutorial, который управляет по крайней мере одним ресурсом, файлом с именем tutorial.htm.</span><span class="sxs-lookup"><span data-stu-id="38ec1-112">The sample includes a hypothetical component named Tutorial that controls at least one resource, a file named tutorial.htm.</span></span> <span data-ttu-id="38ec1-113">Идентификатор этого файла в столбце File таблицы File — это учебник.</span><span class="sxs-lookup"><span data-stu-id="38ec1-113">The identifier for this file in the File column of the File table is Tutorial.</span></span> <span data-ttu-id="38ec1-114">В следующем обсуждении предполагается, что вы уже создали ресурсы, необходимые для работы с руководством, и сделали все необходимые записи в таблицах [компонентов](feature-table.md), [компонентов](component-table.md), [файлов](file-table.md), [каталогов](directory-table.md)и [феатурекомпонентс](featurecomponents-table.md) для установки этого компонента.</span><span class="sxs-lookup"><span data-stu-id="38ec1-114">The following discussion assumes that you have already created the resources required by Tutorial, and have made all the necessary entries in the [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md), and [FeatureComponents](featurecomponents-table.md) tables to install this component.</span></span> <span data-ttu-id="38ec1-115">Дополнительные сведения см. [в примере установки](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="38ec1-115">For more information, see [An Installation Example](an-installation-example.md).</span></span>

<span data-ttu-id="38ec1-116">Следующие разделы содержат сведения о том, как создать необходимые настраиваемые действия и добавить их в пакет установки.</span><span class="sxs-lookup"><span data-stu-id="38ec1-116">The following topics contain information about how to create required custom actions and add them to an installation package.</span></span>

-   [<span data-ttu-id="38ec1-117">Создание настраиваемого действия запуска</span><span class="sxs-lookup"><span data-stu-id="38ec1-117">Authoring the Launch Custom Action</span></span>](authoring-the-launch-custom-action.md)
-   [<span data-ttu-id="38ec1-118">Добавление запуска в таблицы CustomAction и binary</span><span class="sxs-lookup"><span data-stu-id="38ec1-118">Adding Launch to the CustomAction and Binary Tables</span></span>](adding-launch-to-the-customaction-and-binary-tables.md)
-   [<span data-ttu-id="38ec1-119">Добавление события элемента управления в конце установки для запуска запуска</span><span class="sxs-lookup"><span data-stu-id="38ec1-119">Adding a Control Event at the End of the Installation to Run Launch</span></span>](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



