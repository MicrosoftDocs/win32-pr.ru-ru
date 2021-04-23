---
description: Эксперт — это библиотека динамической компоновки (DLL) Microsoft Win32, которая анализирует сетевой трафик, собранный поставщиком сетевых пакетов (НПП), и помещается в файл записи.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Специалист
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662201"
---
# <a name="expert"></a><span data-ttu-id="1270c-103">Специалист</span><span class="sxs-lookup"><span data-stu-id="1270c-103">Expert</span></span>

<span data-ttu-id="1270c-104">Эксперт — это библиотека динамической компоновки (DLL) Microsoft Win32, которая анализирует сетевой трафик, собранный [*поставщиком сетевых пакетов*](n.md) (НПП), и помещается в файл записи.</span><span class="sxs-lookup"><span data-stu-id="1270c-104">An expert is a Microsoft Win32 dynamic-link library (DLL) that analyzes network traffic collected by a [*network packet provider*](n.md) (NPP), and placed in a capture file.</span></span> <span data-ttu-id="1270c-105">После записи и сохранения данных в файле записи эксперт работает с анализатором, который также называется анализатором протокола, для анализа данных в файле.</span><span class="sxs-lookup"><span data-stu-id="1270c-105">After the data is captured and stored in a capture file, the expert works with a parser, also referred to as a protocol parser, to analyze the data in the file.</span></span> <span data-ttu-id="1270c-106">Например, можно проверить кадры файла записи и использовать [*средство синтаксического анализа*](p.md) для распознавания протоколов, таких как SMB, или протокол TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1270c-106">For example, you can examine the frames of the capture file and use a [*parser*](p.md) to recognize protocols such as server message block (SMB), or Transmission Control Protocol/Internet Protocol (TCP/IP).</span></span>

<span data-ttu-id="1270c-107">Вы можете разработать эксперт для работы со всеми анализаторами сетевой монитор, а также с любыми парсерами, созданными самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="1270c-107">You can design an expert to work with all of the Network Monitor parsers, and any parsers that you create yourself.</span></span>

<span data-ttu-id="1270c-108">После того как запрошенное соответствие протоколов определяет конкретный кадр, эксперт извлекает данные из этого фрейма.</span><span class="sxs-lookup"><span data-stu-id="1270c-108">After a requested match of protocols identifies a specific frame, the expert extracts data from the frame.</span></span> <span data-ttu-id="1270c-109">Вы можете программировать эксперта, чтобы обрабатывать данные в пригодных для использования данных, отображаемых сетевой монитор Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="1270c-109">You can program the expert to manipulate information into usable data that the Network Monitor Event Viewer displays.</span></span>

<span data-ttu-id="1270c-110">Вы можете настроить эксперта во время выполнения, а затем использовать сетевой монитор для сохранения данных конфигурации пользователя для повторного использования с различными файлами записи.</span><span class="sxs-lookup"><span data-stu-id="1270c-110">You can configure an expert at run time, and then use Network Monitor to save user configuration data for reuse with different capture files.</span></span> <span data-ttu-id="1270c-111">Вы можете использовать эксперта для предоставления данных корреляции и пользовательских решений для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="1270c-111">You can use an expert to provide correlation data and custom resolutions for end users.</span></span> <span data-ttu-id="1270c-112">Дополнительные сведения о создании сведений о конфигурации на основе HTML см. [на странице справочника по событиям](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="1270c-112">For more information about the creation of HTML-based configuration information, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="1270c-113">Во время установки сетевой монитор следующие файлы DLL экспертов устанавливаются в подкаталог экспертов:</span><span class="sxs-lookup"><span data-stu-id="1270c-113">During Network Monitor setup, the following expert DLLs are installed in the Experts sub-directory:</span></span>

-   <span data-ttu-id="1270c-114">Coalesce.dll</span><span class="sxs-lookup"><span data-stu-id="1270c-114">Coalesce.dll</span></span>
-   <span data-ttu-id="1270c-115">Propdist.dll</span><span class="sxs-lookup"><span data-stu-id="1270c-115">Propdist.dll</span></span>
-   <span data-ttu-id="1270c-116">Protdist.dll</span><span class="sxs-lookup"><span data-stu-id="1270c-116">Protdist.dll</span></span>
-   <span data-ttu-id="1270c-117">Resptime.dll</span><span class="sxs-lookup"><span data-stu-id="1270c-117">Resptime.dll</span></span>
-   <span data-ttu-id="1270c-118">Tcpipe.dll</span><span class="sxs-lookup"><span data-stu-id="1270c-118">Tcpipe.dll</span></span>
-   <span data-ttu-id="1270c-119">Topuser.dll</span><span class="sxs-lookup"><span data-stu-id="1270c-119">Topuser.dll</span></span>

<span data-ttu-id="1270c-120">При запуске сетевой монитор функция [**DllMain**](dllmain-expert.md) создает всех экспертов в подкаталоге экспертов.</span><span class="sxs-lookup"><span data-stu-id="1270c-120">When you start Network Monitor, the [**DllMain**](dllmain-expert.md) function builds all experts in the experts subdirectory.</span></span> <span data-ttu-id="1270c-121">Когда пользователь выбирает **экспертов** в меню **сервис** пользовательского интерфейса сетевой монитор, сетевой монитор загружает экспертные библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="1270c-121">When the user selects **Experts** on the **Tools** menu of the Network Monitor UI, Network Monitor loads the expert DLLs.</span></span> <span data-ttu-id="1270c-122">Эксперт вызывается через точку входа [специалиста по регистрации](register-expert.md) , чтобы предоставить основные сведения о эксперте.</span><span class="sxs-lookup"><span data-stu-id="1270c-122">The expert is called through the [Register Expert](register-expert.md) entry point to provide basic details about the expert.</span></span>

![диалоговое окно "эксперты" сетевого монитора](images/expick.png)

<span data-ttu-id="1270c-124">Сетевой монитор вызывает следующие функции для управления экспертом:</span><span class="sxs-lookup"><span data-stu-id="1270c-124">Network Monitor calls the following functions to manage the expert:</span></span>

-   [<span data-ttu-id="1270c-125">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="1270c-125">**DllMain**</span></span>](dllmain-expert.md)
-   [<span data-ttu-id="1270c-126">**Регистрация экспертов**</span><span class="sxs-lookup"><span data-stu-id="1270c-126">**Register Expert**</span></span>](register-expert.md)
-   [<span data-ttu-id="1270c-127">**Выполнить**</span><span class="sxs-lookup"><span data-stu-id="1270c-127">**Run**</span></span>](run.md)
-   [<span data-ttu-id="1270c-128">**Configure**</span><span class="sxs-lookup"><span data-stu-id="1270c-128">**Configure**</span></span>](configure.md)

<span data-ttu-id="1270c-129">Эксперт должен реализовать каждую из вышеперечисленных функций.</span><span class="sxs-lookup"><span data-stu-id="1270c-129">The expert must implement each of the preceding functions.</span></span>

 

 



