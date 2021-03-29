---
description: Если поток ожидает завершения обратного вызова режима ядра, то сторона пользовательского режима в потоке будет задерживаться при вызове функции Звкаллбаккретурн.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Обнаружение обратных вызовов Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990681"
---
# <a name="detecting-kernel-mode-callbacks"></a><span data-ttu-id="08464-103">Обнаружение обратных вызовов Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="08464-103">Detecting Kernel-Mode Callbacks</span></span>

<span data-ttu-id="08464-104">Большая часть кода для операционной системы Windows выполняется в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="08464-104">Most of the code for the Windows operating system runs in kernel mode.</span></span> <span data-ttu-id="08464-105">Режим процессора переключается из пользовательского режима в режим ядра каждый раз, когда поток приложения вызывает функцию из API Windows, которая, в свою очередь, вызывает внутреннюю системную функцию, которая должна выполняться в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="08464-105">The processor mode switches from user mode to kernel mode whenever an application thread calls a function from the Windows API that in turn calls an internal system function that must execute in kernel mode.</span></span> <span data-ttu-id="08464-106">Режим процессора возвращается в пользовательский режим перед возвратом управления функции, чтобы обеспечить защиту системных данных.</span><span class="sxs-lookup"><span data-stu-id="08464-106">The processor mode returns to user mode before control returns to the function so that the system data is protected.</span></span>

<span data-ttu-id="08464-107">Если поток ожидает завершения обратного вызова режима ядра, то сторона пользовательского режима в потоке будет задерживаться при вызове функции **звкаллбаккретурн** .</span><span class="sxs-lookup"><span data-stu-id="08464-107">If a thread is waiting for a kernel-mode callback to complete, the user-mode side of the thread will delay at a call to the **ZwCallbackReturn** function.</span></span>

 

 



