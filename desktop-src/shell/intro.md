---
description: Пользовательский интерфейс Windows предоставляет пользователям доступ к широкому спектру объектов, необходимых для запуска приложений и управления операционной системой.
title: Руководством разработчика оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997294"
---
# <a name="shell-developers-guide"></a><span data-ttu-id="83265-103">Руководством разработчика оболочки</span><span class="sxs-lookup"><span data-stu-id="83265-103">Shell Developer's Guide</span></span>

<span data-ttu-id="83265-104">Пользовательский интерфейс Windows предоставляет пользователям доступ к широкому спектру объектов, необходимых для запуска приложений и управления операционной системой.</span><span class="sxs-lookup"><span data-stu-id="83265-104">The Windows UI provides users with access to a wide variety of objects necessary to run applications and manage the operating system.</span></span> <span data-ttu-id="83265-105">Самыми многочисленными и знакомыми этими объектами являются папки и файлы, расположенные на дисках компьютера.</span><span class="sxs-lookup"><span data-stu-id="83265-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="83265-106">Существует также ряд виртуальных объектов, позволяющих пользователю выполнять такие задачи, как отправка файлов на удаленные принтеры или доступ к корзине.</span><span class="sxs-lookup"><span data-stu-id="83265-106">There are also a number of virtual objects that allow the user to do tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="83265-107">Оболочка организует эти объекты в иерархическое пространство имен и предоставляет пользователям и приложениям единообразный и эффективный способ доступа к объектам и управления ими.</span><span class="sxs-lookup"><span data-stu-id="83265-107">The Shell organizes these objects into a hierarchical namespace, and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="83265-108">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="83265-108">In this section</span></span>

-   [<span data-ttu-id="83265-109">Вопросы безопасности: оболочка Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="83265-109">Security Considerations: Microsoft Windows Shell</span></span>](sec-shell.md)
-   [<span data-ttu-id="83265-110">Руководство по реализации расширений In-Process</span><span class="sxs-lookup"><span data-stu-id="83265-110">Guidance for Implementing In-Process Extensions</span></span>](shell-and-managed-code.md)
-   [<span data-ttu-id="83265-111">Версии оболочки и стандартных элементов управления</span><span class="sxs-lookup"><span data-stu-id="83265-111">Shell and Common Controls Versions</span></span>](versions.md)
-   [<span data-ttu-id="83265-112">Реализация интерфейсов объекта папки Basic</span><span class="sxs-lookup"><span data-stu-id="83265-112">Implementing the Basic Folder Object Interfaces</span></span>](nse-implement.md)
-   [<span data-ttu-id="83265-113">Реализация пользовательского формата файла</span><span class="sxs-lookup"><span data-stu-id="83265-113">Implementing a Custom File Format</span></span>](customizing-file-types-bumper.md)
-   [<span data-ttu-id="83265-114">Расширяемость оболочки (создание источника данных)</span><span class="sxs-lookup"><span data-stu-id="83265-114">Shell Extensibility (Creating a Data Source)</span></span>](shell-extensibility-bumper.md)
-   [<span data-ttu-id="83265-115">Реализация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="83265-115">Implementing Control Panel Items</span></span>](control-panel-applications.md)
-   [<span data-ttu-id="83265-116">Поддержка приложений оболочки</span><span class="sxs-lookup"><span data-stu-id="83265-116">Supporting Shell Applications</span></span>](application-support-bumper.md)
-   [<span data-ttu-id="83265-117">Статьи о старых оболочках</span><span class="sxs-lookup"><span data-stu-id="83265-117">Legacy Shell Topics</span></span>](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a><span data-ttu-id="83265-118">Соглашения о документе</span><span class="sxs-lookup"><span data-stu-id="83265-118">Document Conventions</span></span>

<span data-ttu-id="83265-119">Руководства для разработчиков оболочки следуют стандартным соглашениям к документам пакета средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="83265-119">The Shell Developers's Guide follows the usual Windows Software Development Kit (SDK) document conventions.</span></span> <span data-ttu-id="83265-120">Следует отметить два соглашения в частности:</span><span class="sxs-lookup"><span data-stu-id="83265-120">Two conventions in particular should be noted:</span></span>

-   <span data-ttu-id="83265-121">В примере кода опущен стандартный код исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="83265-121">Sample code omits normal error-correction code.</span></span> <span data-ttu-id="83265-122">Этот код был удален только для того, чтобы сделать код более удобочитаемым.</span><span class="sxs-lookup"><span data-stu-id="83265-122">This code has been removed only to make the code more readable.</span></span> <span data-ttu-id="83265-123">В свои приложения следует включить весь соответствующий код исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="83265-123">You should include all appropriate error-correction code in your own applications.</span></span>
-   <span data-ttu-id="83265-124">Чтобы образцы записей реестра были очищены, имена разделов, подразделов и записей, а также значения отображаются со стандартным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="83265-124">To make sample registry entries clear, key, subkey, and entry names as well as values are displayed with a standard font.</span></span> <span data-ttu-id="83265-125">Имена элементов, определяемых пользователем или приложениями, выделены курсивом.</span><span class="sxs-lookup"><span data-stu-id="83265-125">User or application-defined item names are italicized.</span></span>

 

 



