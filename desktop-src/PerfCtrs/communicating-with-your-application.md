---
description: Как правило, поставщик предоставляет данные от имени приложения.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Взаимодействие с приложением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909748"
---
# <a name="communicating-with-your-application"></a><span data-ttu-id="e10f0-103">Взаимодействие с приложением</span><span class="sxs-lookup"><span data-stu-id="e10f0-103">Communicating With Your Application</span></span>

<span data-ttu-id="e10f0-104">Как правило, поставщик предоставляет данные от имени приложения.</span><span class="sxs-lookup"><span data-stu-id="e10f0-104">Typically, a provider provides data on behalf of an application.</span></span> <span data-ttu-id="e10f0-105">Например, сервер может создать библиотеку DLL производительности для предоставления данных счетчиков.</span><span class="sxs-lookup"><span data-stu-id="e10f0-105">For example, a server might create a performance DLL to provide its counter data.</span></span> <span data-ttu-id="e10f0-106">Взаимодействие между приложением и его поставщиком отличается для приложений пользовательского режима и режима ядра.</span><span class="sxs-lookup"><span data-stu-id="e10f0-106">Communication between an application and its provider differs for user-mode and kernel-mode applications.</span></span> <span data-ttu-id="e10f0-107">Поставщики выполняются в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="e10f0-107">Providers execute in user mode.</span></span> <span data-ttu-id="e10f0-108">В связи с этим приложения пользовательского режима, такие как приложения для печати и отображения, могут использовать любой способ межпроцессного взаимодействия, например именованные каналы, сопоставление файлов или RPC.</span><span class="sxs-lookup"><span data-stu-id="e10f0-108">Because of this, user-mode applications, such as print and display applications, can use any technique for interprocess communication, such as named pipes, file mapping, or RPC.</span></span> <span data-ttu-id="e10f0-109">Однако приложения в режиме ядра должны предоставлять интерфейс IOCTL, который возвращает поставщику данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="e10f0-109">However, kernel-mode applications must provide an IOCTL interface that returns the performance data to the provider.</span></span>

> [!WARNING]
> <span data-ttu-id="e10f0-110">Не используйте COM в качестве механизма IPC.</span><span class="sxs-lookup"><span data-stu-id="e10f0-110">Do not use COM as the IPC mechanism.</span></span> <span data-ttu-id="e10f0-111">Система не может гарантировать состояние инициализации COM потока, вызывающего интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e10f0-111">The system cannot guarantee the COM initialization state of the thread calling the interface.</span></span> <span data-ttu-id="e10f0-112">Поэтому библиотека DLL не сможет успешно инициализировать COM и получить данные.</span><span class="sxs-lookup"><span data-stu-id="e10f0-112">Therefore, the DLL may not be able to successfully initialize COM and collect the data.</span></span>

 

 

 



