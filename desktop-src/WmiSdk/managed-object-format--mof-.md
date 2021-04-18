---
description: MOF-файл (MOF) — это язык, используемый для описания классов модель CIM (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: MOF-файл
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693446"
---
# <a name="managed-object-format-mof"></a><span data-ttu-id="534ab-103">MOF-файл</span><span class="sxs-lookup"><span data-stu-id="534ab-103">Managed Object Format (MOF)</span></span>

<span data-ttu-id="534ab-104">MOF-файл (MOF) — это язык, используемый для описания классов [*модель CIM (CIM)*](gloss-c.md) .</span><span class="sxs-lookup"><span data-stu-id="534ab-104">Managed Object Format (MOF) is the language used to describe [*Common Information Model (CIM)*](gloss-c.md) classes.</span></span>

<span data-ttu-id="534ab-105">Для поставщиков WMI рекомендуется реализовать новые классы WMI в MOF-файлах, компилируемых с помощью [**Mofcomp.exe**](mofcomp.md) в [*репозиторий WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="534ab-105">The recommended way for WMI providers to implement new WMI classes is in MOF files which are compiled using [**Mofcomp.exe**](mofcomp.md) into the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="534ab-106">Кроме того, можно создавать классы и экземпляры CIM и управлять ими с помощью [API COM для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="534ab-106">It is also possible to create and manipulate CIM classes and instances using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="534ab-107">Поставщик WMI обычно состоит из MOF-файла, который определяет классы данных и событий, для которых поставщик возвращает данные, и DLL-файл, содержащий код, предоставляющий данные.</span><span class="sxs-lookup"><span data-stu-id="534ab-107">A WMI provider normally consists of a MOF file, which defines the data and event classes for which the provider returns data, and a DLL file which contains the code that supplies data.</span></span> <span data-ttu-id="534ab-108">Дополнительные сведения см. [в разделе Предоставление данных инструментарию WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="534ab-108">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="534ab-109">Клиентские сценарии и приложения WMI могут запрашивать экземпляры классов MOF поставщика или подписываться на получение уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="534ab-109">WMI client scripts and applications can query for instances of provider MOF classes or subscribe to receive event notifications.</span></span>

<span data-ttu-id="534ab-110">С помощью MOF можно выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="534ab-110">You can perform the following tasks with MOF:</span></span>

-   [<span data-ttu-id="534ab-111">Компиляция MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="534ab-111">Compiling MOF Files</span></span>](compiling-mof-files.md)
-   [<span data-ttu-id="534ab-112">Создание класса</span><span class="sxs-lookup"><span data-stu-id="534ab-112">Creating a Class</span></span>](creating-a-class.md)
-   [<span data-ttu-id="534ab-113">Создание экземпляра</span><span class="sxs-lookup"><span data-stu-id="534ab-113">Creating an Instance</span></span>](creating-an-instance.md)
-   [<span data-ttu-id="534ab-114">Создание метода</span><span class="sxs-lookup"><span data-stu-id="534ab-114">Creating a Method</span></span>](creating-a-method.md)
-   [<span data-ttu-id="534ab-115">Добавление квалификатора</span><span class="sxs-lookup"><span data-stu-id="534ab-115">Adding a Qualifier</span></span>](adding-a-qualifier.md)
-   [<span data-ttu-id="534ab-116">Создание комментария</span><span class="sxs-lookup"><span data-stu-id="534ab-116">Creating a Comment</span></span>](creating-a-comment.md)

## <a name="related-topics"></a><span data-ttu-id="534ab-117">См. также</span><span class="sxs-lookup"><span data-stu-id="534ab-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="534ab-118">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="534ab-118">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



