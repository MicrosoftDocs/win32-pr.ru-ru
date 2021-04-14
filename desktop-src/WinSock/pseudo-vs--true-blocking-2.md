---
description: Псеудоблоккинг операции с псевдо-блокирующими в сокетах Windows (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Псевдо и истинная блокировка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692716"
---
# <a name="pseudo-blocking-and-true-blocking"></a><span data-ttu-id="46e38-103">Псевдо и истинная блокировка</span><span class="sxs-lookup"><span data-stu-id="46e38-103">Pseudo Blocking and True Blocking</span></span>

<span data-ttu-id="46e38-104">В 16 средах Windows Блокировка true не поддерживается операционной системой; Таким образом, операция блокирования, которая не может быть выполнена немедленно, обрабатывается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="46e38-104">In 16 Windows environments, true blocking is not supported by the operating system; therefore, a blocking operation that cannot be completed immediately is handled as follows:</span></span>

-   <span data-ttu-id="46e38-105">Поставщик услуг инициирует операцию, а затем входит в цикл, в течение которого он отправляет любые сообщения Windows (при необходимости передавая процессор другому потоку).</span><span class="sxs-lookup"><span data-stu-id="46e38-105">The service provider initiates the operation, and then enters a loop during which it dispatches any Windows messages (yielding the processor to another thread if necessary)</span></span>
-   <span data-ttu-id="46e38-106">Затем он проверяет завершение функции сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="46e38-106">It then checks for the completion of the Windows Sockets function.</span></span>
-   <span data-ttu-id="46e38-107">Если функция завершена или при вызове [**вспканцелблоккингкалл**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) был вызван, цикл завершается, а функция блокировки завершается с соответствующим результатом.</span><span class="sxs-lookup"><span data-stu-id="46e38-107">If the function has completed, or if [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) has been invoked, the loop is terminated and the blocking function completes with an appropriate result.</span></span>

<span data-ttu-id="46e38-108">Это относится к термину «псевдо-Block», а цикл, упомянутый выше, называется блокирующим обработчиком по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46e38-108">This is what is meant by the term pseudo blocking, and the loop referred to above is known as the default blocking hook.</span></span>

 

 
