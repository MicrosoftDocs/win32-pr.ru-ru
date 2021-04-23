---
description: 'Windows предоставляет функции, выполняющие следующие задачи:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Объектный интерфейс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497688"
---
# <a name="object-interface"></a><span data-ttu-id="1a66a-103">Объектный интерфейс</span><span class="sxs-lookup"><span data-stu-id="1a66a-103">Object Interface</span></span>

<span data-ttu-id="1a66a-104">Windows предоставляет функции, выполняющие следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="1a66a-104">Windows provides functions that perform the following tasks:</span></span>

-   <span data-ttu-id="1a66a-105">Создание объекта</span><span class="sxs-lookup"><span data-stu-id="1a66a-105">Create an object</span></span>
-   <span data-ttu-id="1a66a-106">Получение маркера объекта</span><span class="sxs-lookup"><span data-stu-id="1a66a-106">Get an object handle</span></span>
-   <span data-ttu-id="1a66a-107">Получение сведений об объекте</span><span class="sxs-lookup"><span data-stu-id="1a66a-107">Get information about the object</span></span>
-   <span data-ttu-id="1a66a-108">Задание сведений об объекте</span><span class="sxs-lookup"><span data-stu-id="1a66a-108">Set information about the object</span></span>
-   <span data-ttu-id="1a66a-109">Закрытие маркера объекта</span><span class="sxs-lookup"><span data-stu-id="1a66a-109">Close the object handle</span></span>
-   <span data-ttu-id="1a66a-110">Уничтожить объект</span><span class="sxs-lookup"><span data-stu-id="1a66a-110">Destroy the object</span></span>

<span data-ttu-id="1a66a-111">Некоторые из этих задач не являются обязательными для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="1a66a-111">Some of these tasks are not necessary for each object.</span></span> <span data-ttu-id="1a66a-112">Некоторые из этих задач объединяются для определенных объектов.</span><span class="sxs-lookup"><span data-stu-id="1a66a-112">Some of these tasks are combined for certain objects.</span></span> <span data-ttu-id="1a66a-113">Например, приложение может создать объект события.</span><span class="sxs-lookup"><span data-stu-id="1a66a-113">For example, an application can create an event object.</span></span> <span data-ttu-id="1a66a-114">Другие приложения могут открыть событие, чтобы получить уникальный маркер для этого объекта события.</span><span class="sxs-lookup"><span data-stu-id="1a66a-114">Other applications can open the event to obtain a unique handle to this event object.</span></span> <span data-ttu-id="1a66a-115">По мере того, как каждое приложение завершает работу с событием, его обработчик закрывается с объектом.</span><span class="sxs-lookup"><span data-stu-id="1a66a-115">As each application finishes using the event, it closes its handle to the object.</span></span> <span data-ttu-id="1a66a-116">Если нет оставшихся открытых дескрипторов для объекта события, система уничтожает объект события.</span><span class="sxs-lookup"><span data-stu-id="1a66a-116">When there are no remaining open handles to the event object, the system destroys the event object.</span></span> <span data-ttu-id="1a66a-117">В отличие от этого приложение может получить маркер для существующего объекта Window.</span><span class="sxs-lookup"><span data-stu-id="1a66a-117">In contrast, an application can obtain a handle to an existing window object.</span></span> <span data-ttu-id="1a66a-118">Если объект Window больше не нужен, приложение должно уничтожить объект, что сделает недействительным его маркер.</span><span class="sxs-lookup"><span data-stu-id="1a66a-118">When the window object is no longer needed, the application must destroy the object, which invalidates the window handle.</span></span>

<span data-ttu-id="1a66a-119">Иногда объект остается в памяти после закрытия всех дескрипторов объектов.</span><span class="sxs-lookup"><span data-stu-id="1a66a-119">Occasionally, an object remains in memory after all object handles have been closed.</span></span> <span data-ttu-id="1a66a-120">Например, поток может создать объект события и подождать обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="1a66a-120">For example, a thread could create an event object and wait on the event handle.</span></span> <span data-ttu-id="1a66a-121">Пока поток находится в состоянии ожидания, другой поток может закрыть тот же самый обработчик объекта события.</span><span class="sxs-lookup"><span data-stu-id="1a66a-121">While the thread is waiting, another thread could close the same event object handle.</span></span> <span data-ttu-id="1a66a-122">Объект события остается в памяти без каких-либо дескрипторов объектов событий, пока для объекта события не будет установлено сигнальное состояние и операция ожидания не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="1a66a-122">The event object remains in memory, without any event object handles, until the event object is set to the signaled state and the wait operation is completed.</span></span> <span data-ttu-id="1a66a-123">В настоящее время система удаляет объект из памяти.</span><span class="sxs-lookup"><span data-stu-id="1a66a-123">At this time, the system removes the object from memory.</span></span>

<span data-ttu-id="1a66a-124">Дескрипторы и объекты потребляют память.</span><span class="sxs-lookup"><span data-stu-id="1a66a-124">Handles and objects consume memory.</span></span> <span data-ttu-id="1a66a-125">Таким образом, чтобы сохранить производительность системы, следует закрыть дескрипторы и удалить объекты, как только они станут ненужными.</span><span class="sxs-lookup"><span data-stu-id="1a66a-125">Therefore, to preserve system performance, you should close handles and delete objects as soon as they are no longer needed.</span></span> <span data-ttu-id="1a66a-126">Если этого не сделать, приложение может повредить производительность системы из-за чрезмерного использования файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="1a66a-126">If you do not do this, your application can hurt system performance, due to excessive use of the paging file.</span></span>

<span data-ttu-id="1a66a-127">Когда процесс завершается, система автоматически закрывает дескрипторы и удаляет объекты, созданные процессом.</span><span class="sxs-lookup"><span data-stu-id="1a66a-127">When a process terminates, the system automatically closes handles and deletes objects created by the process.</span></span> <span data-ttu-id="1a66a-128">Однако при завершении потока система обычно не закрывает дескрипторы и не удаляет объекты.</span><span class="sxs-lookup"><span data-stu-id="1a66a-128">However, when a thread terminates, the system usually does not close handles or delete objects.</span></span> <span data-ttu-id="1a66a-129">Единственными исключениями являются объекты диалога окна, обработчика, расположения окна и динамического обмена данными (DDE). Эти объекты уничтожаются при завершении создания потока.</span><span class="sxs-lookup"><span data-stu-id="1a66a-129">The only exceptions are window, hook, window position, and dynamic data exchange (DDE) conversation objects; these objects are destroyed when the creating thread terminates.</span></span>

 

 



