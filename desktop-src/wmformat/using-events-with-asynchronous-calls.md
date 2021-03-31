---
title: Использование событий с асинхронными вызовами
description: Использование событий с асинхронными вызовами
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media Format SDK, события с асинхронными вызовами
- Пакет SDK для Windows Media Format, события асинхронного вызова
- события, асинхронные вызовы
- события асинхронного вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411276"
---
# <a name="using-events-with-asynchronous-calls"></a><span data-ttu-id="0c62a-107">Использование событий с асинхронными вызовами</span><span class="sxs-lookup"><span data-stu-id="0c62a-107">Using Events with Asynchronous Calls</span></span>

<span data-ttu-id="0c62a-108">Часто при использовании методов, которые вызываются асинхронно, потребуется остановить дальнейшую обработку приложения, пока метод не завершит обработку.</span><span class="sxs-lookup"><span data-stu-id="0c62a-108">Frequently, when using methods that are called asynchronously, you will want to halt further processing of your application until after the method completes processing.</span></span> <span data-ttu-id="0c62a-109">Вы можете реализовать любую методику, которую вы хотите использовать для решения этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="0c62a-109">You can implement any technique you like to handle this situation.</span></span> <span data-ttu-id="0c62a-110">В этом разделе описывается использование события для ожидания асинхронных вызовов в вызывающем потоке.</span><span class="sxs-lookup"><span data-stu-id="0c62a-110">This section describes using an event to wait for asynchronous calls in the calling thread.</span></span> <span data-ttu-id="0c62a-111">Этот метод часто используется с пакетом SDK Windows Media Format и демонстрируется в некоторых примерах приложений.</span><span class="sxs-lookup"><span data-stu-id="0c62a-111">This technique is frequently used with the Windows Media Format SDK, and is demonstrated in some of the sample applications.</span></span>

<span data-ttu-id="0c62a-112">В следующем списке приведены сведения об использовании событий для ожидания асинхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="0c62a-112">The following list summarizes the use of events to wait for asynchronous calls.</span></span>

1.  <span data-ttu-id="0c62a-113">Создайте событие для использования с приложением, вызвав функцию **CreateEvent** пакета Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="0c62a-113">Create an event for use with your application by calling the **CreateEvent** function of the Platform SDK.</span></span>
2.  <span data-ttu-id="0c62a-114">При реализации соответствующих обратных вызовов для приложения захватите сообщения, для которых необходимо подождать.</span><span class="sxs-lookup"><span data-stu-id="0c62a-114">When implementing the appropriate callbacks for your application, trap the messages for which you need to wait.</span></span> <span data-ttu-id="0c62a-115">В логике обработки сообщений для нужных сообщений подается сигнал о событии путем вызова функции **выполнить SetEvent** пакета SDK платформы.</span><span class="sxs-lookup"><span data-stu-id="0c62a-115">In the message handling logic for the desired messages, signal the event by calling the **SetEvent** function of the Platform SDK.</span></span>
3.  <span data-ttu-id="0c62a-116">После вызова асинхронных событий в приложении дождитесь, пока событие подаст сигнал, вызвав функцию **WaitForSingleObject** пакета SDK платформы.</span><span class="sxs-lookup"><span data-stu-id="0c62a-116">After calls to asynchronous events are made in your application, wait for the event to signal by calling the **WaitForSingleObject** function of the Platform SDK.</span></span> <span data-ttu-id="0c62a-117">При разработке приложения Windows необходимо создать цикл для проверки сообщений Windows и включить в цикл вызов **WaitForSingleObject** с коротким временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="0c62a-117">If you are designing a Windows application, you should create a loop to check for Windows messages and include a call to **WaitForSingleObject** in the loop with a short wait time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c62a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0c62a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c62a-119">**Использование методов обратного вызова**</span><span class="sxs-lookup"><span data-stu-id="0c62a-119">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




