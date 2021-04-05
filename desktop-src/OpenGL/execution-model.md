---
title: Модель выполнения
description: Модель выполнения
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, модель выполнения
- модель выполнения OpenGL
- Модель OpenGL, клиент/сервер
- модель клиента/сервера OpenGL
- OpenGL, прозрачный для сети
- фрамебуфферс, модель выполнения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986737"
---
# <a name="execution-model"></a><span data-ttu-id="2f939-109">Модель выполнения</span><span class="sxs-lookup"><span data-stu-id="2f939-109">Execution Model</span></span>

<span data-ttu-id="2f939-110">Для интерпретации команд OpenGL используется модель "клиент-сервер".</span><span class="sxs-lookup"><span data-stu-id="2f939-110">The model for interpretation of OpenGL commands is client/server.</span></span> <span data-ttu-id="2f939-111">Код приложения (клиент) выдает команды, интерпретируемые и обрабатываемые OpenGL (сервером).</span><span class="sxs-lookup"><span data-stu-id="2f939-111">Application code (the client) issues commands, which are interpreted and processed by OpenGL (the server).</span></span> <span data-ttu-id="2f939-112">Сервер может и не быть работающим на том же компьютере, что и клиент.</span><span class="sxs-lookup"><span data-stu-id="2f939-112">The server may or may not operate on the same computer as the client.</span></span> <span data-ttu-id="2f939-113">В этом смысле OpenGL является прозрачным для сети.</span><span class="sxs-lookup"><span data-stu-id="2f939-113">In this sense, OpenGL is network-transparent.</span></span> <span data-ttu-id="2f939-114">Сервер может поддерживать несколько контекстов OpenGL, каждый из которых является инкапсулированным состоянием OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2f939-114">A server can maintain several OpenGL contexts, each of which is an encapsulated OpenGL state.</span></span> <span data-ttu-id="2f939-115">Клиент может подключаться к одному из этих контекстов.</span><span class="sxs-lookup"><span data-stu-id="2f939-115">A client can connect to any one of these contexts.</span></span> <span data-ttu-id="2f939-116">Необходимый сетевой протокол можно реализовать, добавив уже существующий протокол (например, для системы X Window) или используя независимый протокол.</span><span class="sxs-lookup"><span data-stu-id="2f939-116">The required network protocol can be implemented by augmenting an already existing protocol (such as that of the X Window System) or by using an independent protocol.</span></span> <span data-ttu-id="2f939-117">Для получения вводимых пользователем данных команды OpenGL не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="2f939-117">No OpenGL commands are provided for obtaining user input.</span></span>

<span data-ttu-id="2f939-118">Система Window, которая выделяет ресурсы буфера кадров, в конечном итоге управляет влиянием команд OpenGL на буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2f939-118">The window system that allocates framebuffer resources ultimately controls the effects of OpenGL commands on the framebuffer.</span></span> <span data-ttu-id="2f939-119">Система Window:</span><span class="sxs-lookup"><span data-stu-id="2f939-119">The window system:</span></span>

-   <span data-ttu-id="2f939-120">Определяет, какие части буфера кадров OpenGL могут быть доступны в любой конкретный момент времени.</span><span class="sxs-lookup"><span data-stu-id="2f939-120">Determines which portions of the framebuffer OpenGL may access at any given time.</span></span>
-   <span data-ttu-id="2f939-121">Взаимодействует с OpenGL, как структурированы эти части.</span><span class="sxs-lookup"><span data-stu-id="2f939-121">Communicates to OpenGL how those portions are structured.</span></span>

<span data-ttu-id="2f939-122">Поэтому нет команд OpenGL для настройки буфера кадров или инициализации OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2f939-122">Therefore, there are no OpenGL commands to configure the framebuffer or initialize OpenGL.</span></span> <span data-ttu-id="2f939-123">Настройка буфера кадров выполняется вне OpenGL в сочетании с системным окном; Инициализация OpenGL выполняется, когда система Window выделяет окно для отрисовки OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2f939-123">Frame buffer configuration is done outside of OpenGL in conjunction with the window system; OpenGL initialization takes place when the window system allocates a window for OpenGL rendering.</span></span>

 

 




