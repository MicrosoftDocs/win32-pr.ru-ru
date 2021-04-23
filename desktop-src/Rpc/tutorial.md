---
title: Учебник
description: В этом руководстве описано, как создать простое распределенное приложение с одним клиентом на одном сервере из существующего автономного приложения.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- Удаленный вызов процедур RPC, учебник
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068339"
---
# <a name="tutorial"></a><span data-ttu-id="400bd-104">Учебник</span><span class="sxs-lookup"><span data-stu-id="400bd-104">Tutorial</span></span>

<span data-ttu-id="400bd-105">В этом руководстве описано, как создать простое распределенное приложение с одним клиентом на одном сервере из существующего автономного приложения.</span><span class="sxs-lookup"><span data-stu-id="400bd-105">This tutorial takes you through the steps required to create a simple, single-client, single-server distributed application from an existing standalone application.</span></span> <span data-ttu-id="400bd-106">Ниже приведены эти действия.</span><span class="sxs-lookup"><span data-stu-id="400bd-106">These steps are:</span></span>

-   <span data-ttu-id="400bd-107">Создайте определение интерфейса и файлы конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="400bd-107">Create interface definition and application configuration files.</span></span>
-   <span data-ttu-id="400bd-108">Используйте компилятор MIDL для создания заглушек клиента и заголовков сервера на языке C из этих файлов.</span><span class="sxs-lookup"><span data-stu-id="400bd-108">Use the MIDL compiler to generate C-language client and server stubs and headers from those files.</span></span>
-   <span data-ttu-id="400bd-109">Напишите клиентское приложение, которое управляет подключением к серверу.</span><span class="sxs-lookup"><span data-stu-id="400bd-109">Write a client application that manages its connection to the server.</span></span>
-   <span data-ttu-id="400bd-110">Написание серверного приложения, содержащего фактические удаленные процедуры.</span><span class="sxs-lookup"><span data-stu-id="400bd-110">Write a server application that contains the actual remote procedures.</span></span>
-   <span data-ttu-id="400bd-111">Скомпилируйте и свяжите эти файлы с библиотекой времени выполнения RPC для создания распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="400bd-111">Compile and link these files to the RPC run-time library to produce the distributed application.</span></span>

<span data-ttu-id="400bd-112">Клиентское приложение передает строку символов на сервер при удаленном вызове процедуры, а сервер выводит строку "Hello, World" в стандартный выход.</span><span class="sxs-lookup"><span data-stu-id="400bd-112">The client application passes a character string to the server in a remote procedure call, and the server prints the string "Hello, World" to its standard output.</span></span>

<span data-ttu-id="400bd-113">Полные исходные файлы для этого примера приложения, а также дополнительный код для управления входом из командной строки и вывода различных сообщений о состоянии пользователю, находятся в \\ каталоге RPC Hello пакета средств разработки программного обеспечения платформы (SDK).</span><span class="sxs-lookup"><span data-stu-id="400bd-113">The complete source files for this example application, with additional code to handle command-line input and to output various status messages to the user, are in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="400bd-114">В этом разделе представлено обсуждение в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="400bd-114">This section presents its discussion in the following topics:</span></span>

-   [<span data-ttu-id="400bd-115">Автономное приложение</span><span class="sxs-lookup"><span data-stu-id="400bd-115">The Standalone Application</span></span>](the-standalone-application.md)
-   [<span data-ttu-id="400bd-116">Определение интерфейса</span><span class="sxs-lookup"><span data-stu-id="400bd-116">Defining the Interface</span></span>](defining-the-interface.md)
-   [<span data-ttu-id="400bd-117">Создание UUID</span><span class="sxs-lookup"><span data-stu-id="400bd-117">Generating the UUID</span></span>](generating-the-uuid.md)
-   [<span data-ttu-id="400bd-118">IDL-файл</span><span class="sxs-lookup"><span data-stu-id="400bd-118">The IDL File</span></span>](the-idl-file.md)
-   [<span data-ttu-id="400bd-119">Файл ACF</span><span class="sxs-lookup"><span data-stu-id="400bd-119">The ACF File</span></span>](the-acf-file.md)
-   [<span data-ttu-id="400bd-120">Создание файлов заглушек</span><span class="sxs-lookup"><span data-stu-id="400bd-120">Generating the Stub Files</span></span>](generating-the-stub-files.md)
-   [<span data-ttu-id="400bd-121">Клиентское приложение</span><span class="sxs-lookup"><span data-stu-id="400bd-121">The Client Application</span></span>](the-client-application.md)
-   [<span data-ttu-id="400bd-122">Серверное приложение</span><span class="sxs-lookup"><span data-stu-id="400bd-122">The Server Application</span></span>](the-server-application.md)
-   [<span data-ttu-id="400bd-123">Остановка серверного приложения</span><span class="sxs-lookup"><span data-stu-id="400bd-123">Stopping the Server Application</span></span>](stopping-the-server-application.md)
-   [<span data-ttu-id="400bd-124">Компиляция и компоновка</span><span class="sxs-lookup"><span data-stu-id="400bd-124">Compiling and Linking</span></span>](compiling-and-linking.md)
-   [<span data-ttu-id="400bd-125">Запуск приложения</span><span class="sxs-lookup"><span data-stu-id="400bd-125">Running the Application</span></span>](running-the-application.md)

 

 




