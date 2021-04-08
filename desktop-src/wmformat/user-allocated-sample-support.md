---
title: Поддержка примера, выделенного пользователем
description: Поддержка примера, выделенного пользователем
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Пакет SDK для Windows Media Format, поддержка образцов, выделенных пользователем
- Расширенный формат систем (ASF), поддержка образцов, выделенных пользователем
- ASF (Расширенный системный формат), поддержка образцов, выделенных пользователем
- Поддержка примера, выделенного пользователем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067733"
---
# <a name="user-allocated-sample-support"></a><span data-ttu-id="91fd2-107">Поддержка примера, выделенного пользователем</span><span class="sxs-lookup"><span data-stu-id="91fd2-107">User Allocated Sample Support</span></span>

<span data-ttu-id="91fd2-108">В обычных обстоятельствах и объект чтения, и синхронный объект Reader создают новый объект buffer для каждого примера, доставляемого в приложение.</span><span class="sxs-lookup"><span data-stu-id="91fd2-108">Under normal circumstances, both the reader object and the synchronous reader object create a new buffer object for each sample delivered to your application.</span></span> <span data-ttu-id="91fd2-109">Это обусловлено тем, что объект чтения не позволяет понять, что делает приложение с примерами после его получения.</span><span class="sxs-lookup"><span data-stu-id="91fd2-109">This is because the reading object has no way of knowing what your application does with the samples after it gets them.</span></span> <span data-ttu-id="91fd2-110">Несмотря на то, что многие приложения считывают образцы только для немедленного отображения, некоторым приложениям может потребоваться хранить образцы в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="91fd2-110">Even though many applications read samples only to render them immediately, some applications may need to maintain samples for a long time.</span></span> <span data-ttu-id="91fd2-111">Объект чтения не может, следовательно, повторно использовать любой из выделенных буферов. он доставляет их в приложение, которое управляет ими.</span><span class="sxs-lookup"><span data-stu-id="91fd2-111">The reading object cannot, therefore, reuse any of the buffers it allocates; it delivers them to your application, which then has control over them.</span></span>

<span data-ttu-id="91fd2-112">Проблема с этим подходом заключается в том, что файл может содержать огромное количество выборок.</span><span class="sxs-lookup"><span data-stu-id="91fd2-112">The problem with this approach is that a file can contain an immense number of samples.</span></span> <span data-ttu-id="91fd2-113">Если для каждого из них требуется создать новый объект buffer, большое количество процессорного времени будет излишним при выделении и освобождении памяти.</span><span class="sxs-lookup"><span data-stu-id="91fd2-113">If each one of them requires a new buffer object to be created, a lot of processor time is wasted allocating and releasing memory.</span></span> <span data-ttu-id="91fd2-114">В приложениях с учетом времени, таких как проигрыватели мультимедиа, эти издержки могут негативно помешать производительности.</span><span class="sxs-lookup"><span data-stu-id="91fd2-114">In time-sensitive applications such as media players, this overhead can be very detrimental to performance.</span></span>

<span data-ttu-id="91fd2-115">Чтобы устранить проблемы с производительностью образцов, выделенных для чтения, модуль чтения и синхронное средство чтения поддерживают образцы, выделенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="91fd2-115">To alleviate the performance issues of reader-allocated samples, both the reader and the synchronous reader support user-allocated samples.</span></span> <span data-ttu-id="91fd2-116">Чтобы использовать образцы, выделенные приложением, объект чтения выполняет вызовы примера метода обратного вызова выделения, который вы реализуете.</span><span class="sxs-lookup"><span data-stu-id="91fd2-116">To use samples allocated by your application, the reading object makes calls to a sample allocation callback method that you implement.</span></span> <span data-ttu-id="91fd2-117">Логика, используемая обратным вызовом для доставки буферов объекту Read, полностью зависит от вас.</span><span class="sxs-lookup"><span data-stu-id="91fd2-117">The logic used by the callback to deliver buffers to the reading object is entirely up to you.</span></span> <span data-ttu-id="91fd2-118">Вы можете использовать пул буферов для всего файла или использовать несколько пулов буферов, по одному для каждого выходного или потока или любую другую схему, которая подходит для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="91fd2-118">You can use a pool of buffers for the entire file or use multiple pools of buffers, one for each output or stream, or any other scheme that works for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91fd2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="91fd2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91fd2-120">**Выделение буферов для чтения файлов**</span><span class="sxs-lookup"><span data-stu-id="91fd2-120">**Allocating Buffers for File Reading**</span></span>](allocating-buffers-for-file-reading.md)
</dt> <dt>

[<span data-ttu-id="91fd2-121">**Функции чтения файлов**</span><span class="sxs-lookup"><span data-stu-id="91fd2-121">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




