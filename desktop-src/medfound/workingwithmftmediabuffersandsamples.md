---
description: Работа с буферами и примерами мультимедиа MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Работа с буферами и примерами мультимедиа MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351335"
---
# <a name="working-with-mft-media-buffers-and-samples"></a><span data-ttu-id="9ab3a-103">Работа с буферами и примерами мультимедиа MFT</span><span class="sxs-lookup"><span data-stu-id="9ab3a-103">Working with MFT Media Buffers and Samples</span></span>

<span data-ttu-id="9ab3a-104">Кодек МФТС передает мультимедийные данные назад и вперед с помощью буферов мультимедиа и примеров.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-104">Codec MFTs pass media data back and forth by using media buffers and samples.</span></span>

<span data-ttu-id="9ab3a-105">Буфер мультимедиа — это COM-объект, который управляет блоком памяти, обычно для хранения данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-105">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="9ab3a-106">Когда данные передаются в таблицу MFT или из нее, они всегда передаются в виде буфера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-106">When data is passed to or from an MFT, it is always passed in the form of a media buffer.</span></span>

<span data-ttu-id="9ab3a-107">Все буферы мультимедиа предоставляют интерфейс **имфмедиабуффер** .</span><span class="sxs-lookup"><span data-stu-id="9ab3a-107">All media buffers expose the **IMFMediaBuffer** interface.</span></span> <span data-ttu-id="9ab3a-108">Этот интерфейс предназначен для любого типа данных.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-108">This interface is designed for any type of data.</span></span> <span data-ttu-id="9ab3a-109">Буферы, содержащие данные видео, часто также предоставляют **IMF2DBuffer**.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-109">Buffers containing video data often also expose **IMF2DBuffer**.</span></span>

<span data-ttu-id="9ab3a-110">Максимальный размер буфера мультимедиа — это объем памяти, выделенной для буфера.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-110">A media buffer has a maximum size, which is the amount of memory allocated for the buffer.</span></span> <span data-ttu-id="9ab3a-111">Чтобы найти максимальный размер, вызовите **имфмедиабуффер:: @ MaxLength**.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-111">To find the maximum size, call **IMFMediaBuffer::GetMaxLength**.</span></span> <span data-ttu-id="9ab3a-112">В любой момент времени буфер мультимедиа также имеет текущую длину, которая представляет собой объем допустимых данных в буфере, в диапазоне от нуля до максимального размера.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-112">At any point in time, a media buffer also has a current length, which is the amount of valid data in the buffer, ranging from zero bytes up to the maximum size.</span></span> <span data-ttu-id="9ab3a-113">Чтобы получить текущую длину, вызовите метод **имфмедиабуффер:: жеткуррентленгс**.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-113">To get the current length, call **IMFMediaBuffer::GetCurrentLength**.</span></span> <span data-ttu-id="9ab3a-114">При создании буфера Текущая длина равна нулю.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-114">When the buffer is created, the current length is zero.</span></span> <span data-ttu-id="9ab3a-115">При записи данных в буфер вызовите **имфмедиабуффер:: сеткуррентленгс** , чтобы обновить текущую длину.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-115">If you write data to the buffer, call **IMFMediaBuffer::SetCurrentLength** to update the current length.</span></span>

<span data-ttu-id="9ab3a-116">Чтобы получить доступ к памяти в буфере, вызовите **имфмедиабуффер:: Lock**.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-116">To access the memory in the buffer, call **IMFMediaBuffer::Lock**.</span></span> <span data-ttu-id="9ab3a-117">Этот метод возвращает указатель на начало блока памяти.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-117">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="9ab3a-118">По завершении использования указателя вызовите **имфмедиабуффер:: Unlock**.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-118">When you are done using the pointer, call **IMFMediaBuffer::Unlock**.</span></span> <span data-ttu-id="9ab3a-119">Метод **Lock** не является механизмом синхронизации потоков; Это не гарантирует, что другие потоки не смогут получить доступ к буферу.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-119">The **Lock** method is not a thread synchronization mechanism; it does not guarantee that other threads cannot access the buffer.</span></span> <span data-ttu-id="9ab3a-120">Метод **Lock** используется, чтобы гарантировать, что память, к которой осуществлялся доступ, останется действительной до тех пор, пока не будет вызван метод **Unlock** .</span><span class="sxs-lookup"><span data-stu-id="9ab3a-120">The **Lock** method is used to assure that the memory accessed will remain valid until you call the **Unlock** method.</span></span>

<span data-ttu-id="9ab3a-121">Пример объекта мультимедиа (в контексте Media Foundation пакета SDK) — это объект, содержащий упорядоченный список из нуля или более буферов.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-121">A media sample object (in the context of the Media Foundation SDK) is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="9ab3a-122">Примеры носителей предоставляют интерфейс **имфсампле** .</span><span class="sxs-lookup"><span data-stu-id="9ab3a-122">Media samples expose the **IMFSample** interface.</span></span>

<span data-ttu-id="9ab3a-123">Чтобы создать новый пример, вызовите функцию **мфкреатесампле** .</span><span class="sxs-lookup"><span data-stu-id="9ab3a-123">To create a new sample, call the **MFCreateSample** function.</span></span> <span data-ttu-id="9ab3a-124">Изначально список буферов примера пуст.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-124">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="9ab3a-125">Чтобы добавить буфер в конец списка, вызовите метод **имфсампле:: аддбуффер**.</span><span class="sxs-lookup"><span data-stu-id="9ab3a-125">To add a buffer to the end of the list, call **IMFSample::AddBuffer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ab3a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9ab3a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ab3a-127">Работа с кодеками дмос</span><span class="sxs-lookup"><span data-stu-id="9ab3a-127">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> <dt>

[<span data-ttu-id="9ab3a-128">Работа с кодеками МФТС</span><span class="sxs-lookup"><span data-stu-id="9ab3a-128">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



