---
description: Работа с буферами мультимедиа DMO
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Работа с буферами мультимедиа DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703445"
---
# <a name="working-with-dmo-media-buffers"></a><span data-ttu-id="97b7b-103">Работа с буферами мультимедиа DMO</span><span class="sxs-lookup"><span data-stu-id="97b7b-103">Working with DMO Media Buffers</span></span>

<span data-ttu-id="97b7b-104">Входные данные передаются кодеку дмос с помощью буферов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="97b7b-104">Input data is passed to the codec DMOs using media buffers.</span></span> <span data-ttu-id="97b7b-105">Буфер мультимедиа — это объект, реализующий интерфейс [**имедиабуффер**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="97b7b-105">A media buffer is an object that implements the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="97b7b-106">Можно реализовать класс для этой цели или, если в приложении используется пакет SDK Windows Media Format, можно использовать объекты буфера, определенные в этом пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="97b7b-106">You can implement a class for this purpose or, if you are using the Windows Media Format SDK in your application, you can use the buffer objects that are defined in that SDK.</span></span>

<span data-ttu-id="97b7b-107">Если вы реализуете собственный класс буфера, будьте внимательны при обработке памяти буфера.</span><span class="sxs-lookup"><span data-stu-id="97b7b-107">If you implement your own buffer class, be careful about how the buffer memory is handled.</span></span> <span data-ttu-id="97b7b-108">При передаче примера входных данных DMO сохраняет ссылку на буфер до завершения работы с примером.</span><span class="sxs-lookup"><span data-stu-id="97b7b-108">When you pass an input sample, the DMO keeps a reference to the buffer until it is finished with the sample.</span></span> <span data-ttu-id="97b7b-109">Вы можете немедленно освободить ссылку на интерфейс [**имедиабуффер**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , но у вас нет способа узнать, когда кодек больше не нуждается в его ссылке.</span><span class="sxs-lookup"><span data-stu-id="97b7b-109">You can immediately release your reference to the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface, but you have no way of knowing when the codec no longer needs its reference.</span></span> <span data-ttu-id="97b7b-110">Чтобы быть уверенным в том, что память освобождается при удалении объекта, следует реализовать класс таким образом, чтобы он выделил и освободил память для внутреннего буфера.</span><span class="sxs-lookup"><span data-stu-id="97b7b-110">To be certain that the memory is freed when the object deletes itself, you should implement your class so that it allocates and frees the memory for the buffer internally.</span></span>

<span data-ttu-id="97b7b-111">Так как дмос сохраняет ссылки на буферы в течение неизвестного периода времени, довольно просто использовать ограниченный пул буферов.</span><span class="sxs-lookup"><span data-stu-id="97b7b-111">Because the DMOs keep references to buffers for an unknown period of time, it is not a trivial matter to use a limited pool of buffers.</span></span> <span data-ttu-id="97b7b-112">Самым простым решением является выделение нового буфера для каждого образца, хотя это неэффективно.</span><span class="sxs-lookup"><span data-stu-id="97b7b-112">The simplest solution is to allocate a new buffer for each sample, although doing so is inefficient.</span></span>

<span data-ttu-id="97b7b-113">Лучшим решением является реализация объекта для управления пулом буферов.</span><span class="sxs-lookup"><span data-stu-id="97b7b-113">A better solution is to implement an object to manage a pool of buffers.</span></span> <span data-ttu-id="97b7b-114">Для этого напишите код в методе **Release** реализации [**имедиабуффер**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , который вызывает метод диспетчера буферов (вместо удаления самого себя), когда счетчик ссылок становится равным нулю.</span><span class="sxs-lookup"><span data-stu-id="97b7b-114">To do this, write code in the **Release** method of your [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) implementation that calls a method of your buffer manager (instead of deleting itself) when the reference count drops to zero.</span></span> <span data-ttu-id="97b7b-115">Диспетчер буферов может затем поддерживать список указателей на выделенные объекты буфера.</span><span class="sxs-lookup"><span data-stu-id="97b7b-115">The buffer manager can then maintain a list of pointers to allocated buffer objects.</span></span> <span data-ttu-id="97b7b-116">Создайте метод в диспетчере буферов, чтобы проверить список свободных буферов и вернуть указатель, чтобы приложение могла получить доступ к буферам при необходимости.</span><span class="sxs-lookup"><span data-stu-id="97b7b-116">Create a method in your buffer manager to check the list of free buffers and return a pointer so that your application can access buffers when needed.</span></span> <span data-ttu-id="97b7b-117">Этот метод должен создавать новые буферы по мере необходимости и добавлять их в список.</span><span class="sxs-lookup"><span data-stu-id="97b7b-117">This method should create new buffers as needed and add them to the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97b7b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="97b7b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b7b-119">Работа с кодеками дмос</span><span class="sxs-lookup"><span data-stu-id="97b7b-119">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
