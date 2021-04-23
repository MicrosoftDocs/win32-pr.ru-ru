---
description: Режим ошибки указывает системе, как приложение будет реагировать на серьезные ошибки.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Режим ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140795"
---
# <a name="error-mode"></a><span data-ttu-id="07a36-103">Режим ошибок</span><span class="sxs-lookup"><span data-stu-id="07a36-103">Error Mode</span></span>

<span data-ttu-id="07a36-104">Режим ошибки указывает системе, как приложение будет реагировать на серьезные ошибки.</span><span class="sxs-lookup"><span data-stu-id="07a36-104">The error mode indicates to the system how the application is going to respond to serious errors.</span></span> <span data-ttu-id="07a36-105">К серьезным ошибкам относятся сбой диска, ошибки неготовности диска, неправильное выравнивание данных и необработанные исключения.</span><span class="sxs-lookup"><span data-stu-id="07a36-105">Serious errors include disk failure, drive-not-ready errors, data misalignment, and unhandled exceptions.</span></span> <span data-ttu-id="07a36-106">Этот режим ошибок может управляться как для каждого потока, так и для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="07a36-106">This error mode can be managed by either a per-thread or per-process basis.</span></span> <span data-ttu-id="07a36-107">Приложение может позволить системе отображать окно сообщения, информирующее пользователя о том, что произошла ошибка, или же она может решить ошибки.</span><span class="sxs-lookup"><span data-stu-id="07a36-107">An application can let the system display a message box informing the user that an error has occurred, or it can handle the errors.</span></span>

<span data-ttu-id="07a36-108">Для обработки этих ошибок без вмешательства пользователя используйте [**функцию SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) или [**сетсреадеррормоде**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)для конкретного потока.</span><span class="sxs-lookup"><span data-stu-id="07a36-108">To handle these errors without user intervention, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) or the thread-specific [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode).</span></span> <span data-ttu-id="07a36-109">После вызова одной из этих функций и указания соответствующих флагов система не отобразит соответствующие окна сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="07a36-109">After calling one of these functions and specifying appropriate flags, the system will not display the corresponding error message boxes.</span></span>

<span data-ttu-id="07a36-110">Процесс может получить свой режим ошибок с помощью [**жетеррормоде**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) или [**жетсреадеррормоде**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span><span class="sxs-lookup"><span data-stu-id="07a36-110">A process can retrieve its error mode using [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) or [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span></span>

<span data-ttu-id="07a36-111">Рекомендуется, чтобы все приложения вызывали функцию [**функцию SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) на уровне процесса с параметром **SEM \_ фаилкритикалеррорс** при запуске.</span><span class="sxs-lookup"><span data-stu-id="07a36-111">Best practice is that all applications call the process-wide [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with a parameter of **SEM\_FAILCRITICALERRORS** at startup.</span></span> <span data-ttu-id="07a36-112">Это позволяет предотвратить зависание приложений с помощью диалоговых окон режима ошибок.</span><span class="sxs-lookup"><span data-stu-id="07a36-112">This is to prevent error mode dialogs from hanging the application.</span></span>

<span data-ttu-id="07a36-113">Кроме того, вызывающие объекты должны предпочитать версии этих функций для конкретного потока, так как они менее нарушают нормальную работу системы.</span><span class="sxs-lookup"><span data-stu-id="07a36-113">Other than that, callers should favor the thread-specific versions of these functions since they are less disruptive to the normal behavior of the system.</span></span>

 

 
