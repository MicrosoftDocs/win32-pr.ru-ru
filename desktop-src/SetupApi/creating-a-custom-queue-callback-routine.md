---
description: В дополнение к использованию обратного вызова по умолчанию очереди можно написать собственную подпрограммы обратного вызова.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Создание пользовательской подпрограммы обратного вызова очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911559"
---
# <a name="creating-a-custom-queue-callback-routine"></a><span data-ttu-id="ea74c-103">Создание пользовательской подпрограммы обратного вызова очереди</span><span class="sxs-lookup"><span data-stu-id="ea74c-103">Creating a Custom Queue Callback Routine</span></span>

<span data-ttu-id="ea74c-104">В дополнение к использованию обратного вызова по умолчанию очереди можно написать собственную подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ea74c-104">In addition to using the default queue callback, you can write a custom callback routine.</span></span> <span data-ttu-id="ea74c-105">Эта функция должна иметь ту же форму, что и [*филекаллбакк*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="ea74c-105">This function must have the same form as [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="ea74c-106">Это полезно, если необходима подпрограммы обратного вызова для обработки уведомления другими способами, чем предоставлено подпрограммыми обратного вызова очереди по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea74c-106">This is useful if you need a callback routine to handle a notification in a manner other than that provided by the default queue callback routine.</span></span>

<span data-ttu-id="ea74c-107">Если необходимо изменить только небольшую часть поведения подпрограммы обратного вызова очереди по умолчанию, можно создать пользовательскую подпрограммы обратного вызова для фильтрации уведомлений, обработки только тех, которые требуют специального поведения и вызова [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) для других.</span><span class="sxs-lookup"><span data-stu-id="ea74c-107">If only a small portion of the default queue callback routine's behavior needs to be changed, you can create a custom callback routine to filter the notifications, handling only those that require special behavior and calling [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) for the others.</span></span>

<span data-ttu-id="ea74c-108">Например, если вы хотите выполнить пользовательскую обработку ошибок удаления файла, можно создать пользовательскую функцию обратного вызова *микаллбакк*.</span><span class="sxs-lookup"><span data-stu-id="ea74c-108">For example, if you wanted to custom-handle file delete errors, you could create a custom callback function, *MyCallback*.</span></span> <span data-ttu-id="ea74c-109">Эта функция перехватывает и обрабатывает уведомления [**спфиленотифи \_ делетиррор**](spfilenotify-deleteerror.md) и вызывает функцию обратного вызова очереди по умолчанию для всех остальных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ea74c-109">This function would intercept and process [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md) notifications, and call the default queue callback function for all other notifications.</span></span> <span data-ttu-id="ea74c-110">*Микаллбакк* возвращает значение для уведомлений об ошибках удаления.</span><span class="sxs-lookup"><span data-stu-id="ea74c-110">*MyCallback* returns a value for the delete error notifications.</span></span> <span data-ttu-id="ea74c-111">Для всех остальных уведомлений *микаллбакк* передает любое значение подпрограммы обратного вызова очереди по умолчанию, возвращаемой в очередь.</span><span class="sxs-lookup"><span data-stu-id="ea74c-111">For all other notifications, *MyCallback* passes whatever value the default queue callback routine returned to the queue.</span></span>

<span data-ttu-id="ea74c-112">Этот поток управления показан на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="ea74c-112">This flow of control is illustrated in the following diagram.</span></span>

![стрелки и поля, отображающие поток данных для пользовательского функции обратного вызова](images/callback.png)

> [!IMPORTANT]
> <span data-ttu-id="ea74c-114">Если пользовательская функция обратного вызова вызывает подпрограммы обратного вызова очереди по умолчанию, она должна передать указатель void, возвращенный [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) или [**сетупинитдефаулткуеуекаллбаккекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) , в подпрограммы обратного вызова по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea74c-114">If the custom callback function calls the default queue callback routine, it must pass the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) to the default callback routine.</span></span>

 

 

 
