---
description: Программный интерфейс (API) программы установки предоставляет набор функций, которые могут вызываться приложением установки для выполнения операций установки. Эти функции установки работают с INF-файлами Windows для предоставления следующих функций установки.
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: Обзор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32b99c6079fdb61fd6bfd0033ffccb9ebb7b922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663512"
---
# <a name="overview"></a><span data-ttu-id="eaadc-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="eaadc-104">Overview</span></span>

<span data-ttu-id="eaadc-105">Программный интерфейс (API) программы установки предоставляет набор функций, которые могут вызываться приложением установки для выполнения операций установки.</span><span class="sxs-lookup"><span data-stu-id="eaadc-105">The Setup application programming interface (API) provides a set of functions that your setup application can call to perform installation operations.</span></span> <span data-ttu-id="eaadc-106">Эти функции установки работают с INF-файлами Windows для предоставления следующих функций установки.</span><span class="sxs-lookup"><span data-stu-id="eaadc-106">These setup functions work with Windows INF files to provide the following setup functionality.</span></span>



| <span data-ttu-id="eaadc-107">Сведения о</span><span class="sxs-lookup"><span data-stu-id="eaadc-107">For information about</span></span>                       | <span data-ttu-id="eaadc-108">См.</span><span class="sxs-lookup"><span data-stu-id="eaadc-108">See</span></span>                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaadc-109">Файлы очереди</span><span class="sxs-lookup"><span data-stu-id="eaadc-109">Queuing files</span></span>                               | [<span data-ttu-id="eaadc-110">Очереди файлов</span><span class="sxs-lookup"><span data-stu-id="eaadc-110">File Queues</span></span>](file-queues.md)                                                                                                                                              |
| <span data-ttu-id="eaadc-111">Установка файлов</span><span class="sxs-lookup"><span data-stu-id="eaadc-111">Installing files</span></span>                            | [<span data-ttu-id="eaadc-112">Очереди файлов</span><span class="sxs-lookup"><span data-stu-id="eaadc-112">File Queues</span></span>](file-queues.md)<br/> [<span data-ttu-id="eaadc-113">Настройка приложений</span><span class="sxs-lookup"><span data-stu-id="eaadc-113">Setup Applications</span></span>](setup-applications.md)<br/> [<span data-ttu-id="eaadc-114">Создание приложений установки</span><span class="sxs-lookup"><span data-stu-id="eaadc-114">Creating Setup Applications</span></span>](creating-setup-applications.md)<br/> |
| <span data-ttu-id="eaadc-115">Обработка ошибок и запрос мультимедиа</span><span class="sxs-lookup"><span data-stu-id="eaadc-115">Handling errors and prompting for media</span></span>     | [<span data-ttu-id="eaadc-116">Запросы к диску и обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="eaadc-116">Disk Prompting and Error Handling</span></span>](disk-prompting-and-error-handling.md)                                                                                                  |
| <span data-ttu-id="eaadc-117">Обновление записей реестра</span><span class="sxs-lookup"><span data-stu-id="eaadc-117">Updating registry entries</span></span>                   | [<span data-ttu-id="eaadc-118">Настройка приложений</span><span class="sxs-lookup"><span data-stu-id="eaadc-118">Setup Applications</span></span>](setup-applications.md)                                                                                                                                |
| <span data-ttu-id="eaadc-119">Ведение журнала установленных файлов</span><span class="sxs-lookup"><span data-stu-id="eaadc-119">Logging installed files</span></span>                     | [<span data-ttu-id="eaadc-120">Журнал файлов</span><span class="sxs-lookup"><span data-stu-id="eaadc-120">File Log</span></span>](file-log.md)                                                                                                                                                    |
| <span data-ttu-id="eaadc-121">Хранение недавно использовавшихся исходных путей</span><span class="sxs-lookup"><span data-stu-id="eaadc-121">Storing the most recently used source paths</span></span> | [<span data-ttu-id="eaadc-122">Список источников MRU</span><span class="sxs-lookup"><span data-stu-id="eaadc-122">MRU Source List</span></span>](mru-source-list.md)                                                                                                                                      |



 

<span data-ttu-id="eaadc-123">Для большинства функций установки доступны версии Юникода и ANSI.</span><span class="sxs-lookup"><span data-stu-id="eaadc-123">Unicode and ANSI versions are available for most setup functions.</span></span> <span data-ttu-id="eaadc-124">Текстовые файлы в Юникоде должны содержать стандартную метку порядка следования байтов 0xFEFF, чтобы функции программы установки могли обозначать файл как текст в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="eaadc-124">Unicode text files should contain the standard 0xFEFF byte-order mark to enable setup functions to identify the file as Unicode text.</span></span>

<span data-ttu-id="eaadc-125">Хотя API установки поддерживает запросы новых носителей и основных диалоговых окон обработки ошибок, функции установки не предоставляют возможности мастера или универсальный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="eaadc-125">Although the Setup API supports prompting for new media and basic error-handling dialog boxes, the setup functions do not provide wizard functionality or a generic user interface.</span></span>

<span data-ttu-id="eaadc-126">Разработчикам следует определить, могут ли они использовать [установщик Windows](/windows/desktop/Msi/windows-installer-portal) для установки приложений, а не API установки.</span><span class="sxs-lookup"><span data-stu-id="eaadc-126">Developers should consider whether they can use [Windows Installer](/windows/desktop/Msi/windows-installer-portal) to install their applications rather than the Setup API.</span></span> <span data-ttu-id="eaadc-127">Установщик Windows сокращает совокупную стоимость владения для клиентов, позволяя им эффективно устанавливать и настраивать ваши продукты и приложения.</span><span class="sxs-lookup"><span data-stu-id="eaadc-127">Windows Installer reduces the total cost of ownership (TCO) for your customers by enabling them to efficiently install and configure your products and applications.</span></span> <span data-ttu-id="eaadc-128">Установщик также может предоставить вашему продукту новые возможности для объявления функций без их установки, установки продуктов по требованию и добавления пользовательских настроек.</span><span class="sxs-lookup"><span data-stu-id="eaadc-128">The installer can also provide your product with new capabilities to advertise features without installing them, to install products on-demand, and to add user customizations.</span></span>

 

