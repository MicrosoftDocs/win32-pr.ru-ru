---
title: О ДДЕМЛ
description: В этом разделе обсуждается динамический обмен данными.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Пользовательский интерфейс Windows, платформа динамических данных Exchange (DDE)
- Платформа динамических данных Exchange (DDE), сведения
- DDE (платформа динамических данных Exchange), сведения
- Обмен данными, платформа динамических данных Exchange (DDE)
- Пользовательский интерфейс Windows, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), сведения
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), сведения
- Обмен данными, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532471"
---
# <a name="about-the-ddeml"></a><span data-ttu-id="32ef6-111">О ДДЕМЛ</span><span class="sxs-lookup"><span data-stu-id="32ef6-111">About the DDEML</span></span>

<span data-ttu-id="32ef6-112">Платформа динамических данных Exchange (DDE) отличается от механизма пересылки данных в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="32ef6-112">Dynamic Data Exchange (DDE) differs from the clipboard data-transfer mechanism.</span></span> <span data-ttu-id="32ef6-113">Одно отличие заключается в том, что буфер обмена почти всегда используется как однократный ответ на определенное действие пользователем (например, при выборе команды **Вставить** из меню).</span><span class="sxs-lookup"><span data-stu-id="32ef6-113">One difference is that the clipboard is almost always used as a one-time response to a specific action by the user — such as clicking **Paste** from a menu.</span></span> <span data-ttu-id="32ef6-114">Хотя DDE также может инициироваться пользователем, обычно он продолжается без участия пользователя.</span><span class="sxs-lookup"><span data-stu-id="32ef6-114">Although DDE can also be initiated by a user, it typically continues without the user's further involvement.</span></span>

<span data-ttu-id="32ef6-115">Библиотека управления платформа динамических данных Exchange (ДДЕМЛ) предоставляет интерфейс, который упрощает задачу добавления возможностей DDE в приложение.</span><span class="sxs-lookup"><span data-stu-id="32ef6-115">The Dynamic Data Exchange Management Library (DDEML) provides an interface that simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="32ef6-116">Вместо отправки, публикации и обработки сообщений DDE напрямую приложение использует функции, предоставляемые ДДЕМЛ для управления сеансами DDE.</span><span class="sxs-lookup"><span data-stu-id="32ef6-116">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="32ef6-117">Сеанс DDE — это взаимодействие между клиентскими и серверными приложениями.</span><span class="sxs-lookup"><span data-stu-id="32ef6-117">A DDE conversation is the interaction between client and server applications.</span></span> <span data-ttu-id="32ef6-118">ДДЕМЛ также предоставляет средства для управления строками и данными, общими для приложений DDE.</span><span class="sxs-lookup"><span data-stu-id="32ef6-118">The DDEML also provides a means for managing the strings and data shared among DDE applications.</span></span> <span data-ttu-id="32ef6-119">Вместо использования атомов и указателей на объекты общей памяти приложения DDE создают и обмениваются дескрипторами строк, которые обозначают строки и дескрипторы данных, определяющие объекты DDE.</span><span class="sxs-lookup"><span data-stu-id="32ef6-119">Instead of using atoms and pointers to shared memory objects, DDE applications create and exchange string handles, which identify strings, and data handles, which identify DDE objects.</span></span> <span data-ttu-id="32ef6-120">ДДЕМЛ предоставляет функцию ([**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)), которая позволяет серверному приложению регистрировать имена служб, которые она поддерживает.</span><span class="sxs-lookup"><span data-stu-id="32ef6-120">The DDEML provides a function ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) that enables a server application to register the service names it supports.</span></span> <span data-ttu-id="32ef6-121">Затем имена служб пересылаются в другие приложения в системе, которые используют имена для подключения к серверу.</span><span class="sxs-lookup"><span data-stu-id="32ef6-121">The service names are then broadcast to other applications in the system, which use the names to connect to the server.</span></span> <span data-ttu-id="32ef6-122">ДДЕМЛ также обеспечивает совместимость между приложениями DDE, так как они требуют единообразного применения протокола DDE.</span><span class="sxs-lookup"><span data-stu-id="32ef6-122">The DDEML also ensures compatibility among DDE applications by requiring them to implement the DDE protocol in a consistent manner.</span></span>

<span data-ttu-id="32ef6-123">Существующие приложения, использующие протокол DDE на основе сообщений, полностью совместимы с теми, которые используют ДДЕМЛ; Это значит, что приложение, использующее DDE на основе сообщений, может устанавливать диалоги и выполнять транзакции с приложениями с помощью ДДЕМЛ.</span><span class="sxs-lookup"><span data-stu-id="32ef6-123">Existing applications using the message-based DDE protocol are fully compatible with those that use the DDEML; that is, an application using message-based DDE can establish conversations and perform transactions with applications using the DDEML.</span></span> <span data-ttu-id="32ef6-124">Вместо того чтобы использовать сообщения DDE в новом приложении, воспользуйтесь преимуществами ДДЕМЛ и множества усовершенствований, предлагаемых ИТ.</span><span class="sxs-lookup"><span data-stu-id="32ef6-124">Instead of using DDE messages in your new application, take advantage of the DDEML and the many improvements it offers.</span></span>

<span data-ttu-id="32ef6-125">Чтобы использовать ДДЕМЛ, необходимо включить ДДЕМЛ. Файл заголовка H в исходных файлах, свяжите с USER32. Файл LIB и убедитесь, что файл DDEML.DLL находится в системном пути.</span><span class="sxs-lookup"><span data-stu-id="32ef6-125">To use the DDEML, you must include the DDEML.H header file in your source files, link with the USER32.LIB file, and ensure that the DDEML.DLL file resides in the system's path.</span></span>

<span data-ttu-id="32ef6-126">При сбое функции ДДЕМЛ приложение может вызвать функцию [**ддежетластеррор**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) , чтобы определить причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="32ef6-126">Whenever a DDEML function fails, an application can call the [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) function to determine the cause of the failure.</span></span> <span data-ttu-id="32ef6-127">**Ддежетластеррор** возвращает значение ошибки, указывающее причину самой последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="32ef6-127">**DdeGetLastError** returns an error value that specifies the cause of the most recent error.</span></span>

 

 




