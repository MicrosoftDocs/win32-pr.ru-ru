---
description: Потоковая передача — это процесс сохранения только небольшой части воспроизводимого звукового файла в памяти. Это позволяет воспроизводить большие звуковые файлы, например фоновую музыку, и не занимать большой объем памяти.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: XAudio2 потоковая передача звуковых данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703030"
---
# <a name="xaudio2-streaming-audio-data"></a><span data-ttu-id="7eabb-104">XAudio2 потоковая передача звуковых данных</span><span class="sxs-lookup"><span data-stu-id="7eabb-104">XAudio2 Streaming Audio Data</span></span>

<span data-ttu-id="7eabb-105">Потоковая передача — это процесс сохранения только небольшой части воспроизводимого звукового файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="7eabb-105">Streaming is the process of maintaining only a small portion of a playing audio file in memory.</span></span> <span data-ttu-id="7eabb-106">Это позволяет воспроизводить большие звуковые файлы, например фоновую музыку, и не занимать большой объем памяти.</span><span class="sxs-lookup"><span data-stu-id="7eabb-106">This allows large audio files such as background music to be played, and not take up a large amount of memory.</span></span>

<span data-ttu-id="7eabb-107">При потоковой передаче звукового файла его данные считываются с диска в виде фрагментов, а не загружаются сразу весь файл.</span><span class="sxs-lookup"><span data-stu-id="7eabb-107">When an audio file is streamed, its data is read from disk in chunks rather than loading the entire file at once.</span></span> <span data-ttu-id="7eabb-108">Потоковая передача осуществляется асинхронным чтением звуковых данных в очередь буферов диска.</span><span class="sxs-lookup"><span data-stu-id="7eabb-108">Streaming is accomplished by asynchronously reading audio data into a queue of disk buffers.</span></span> <span data-ttu-id="7eabb-109">Каждый буфер заполняется, а затем отправляется на исходный голоса.</span><span class="sxs-lookup"><span data-stu-id="7eabb-109">Each buffer is filled, and then submitted to a source voice.</span></span> <span data-ttu-id="7eabb-110">После того, как голосовое воспроизведение пойдет из буфера, буфер снова станет доступным для чтения.</span><span class="sxs-lookup"><span data-stu-id="7eabb-110">After the voice finishes playing a buffer, the buffer becomes available for reading again.</span></span> <span data-ttu-id="7eabb-111">Таким образом, циклический перебор буферов позволяет воспроизводить большой звуковой файл, пока загружается только часть его данных.</span><span class="sxs-lookup"><span data-stu-id="7eabb-111">Looping through the disk buffers in this manner allows a large audio file to be played while only a portion of its data is loaded.</span></span> <span data-ttu-id="7eabb-112">Код потоковой передачи должен размещаться в отдельном потоке, где он может находиться в спящем режиме при ожидании завершения длительных операций с диском и аудио.</span><span class="sxs-lookup"><span data-stu-id="7eabb-112">The streaming code should be placed in a separate thread, where it can sleep while waiting for long-running disk and audio operations to finish.</span></span> <span data-ttu-id="7eabb-113">Класс обратного вызова используется для пробуждения потока путем активации событий после завершения операций аудио.</span><span class="sxs-lookup"><span data-stu-id="7eabb-113">A callback class is used to wake the thread by triggering events when audio operations have finished.</span></span>

<span data-ttu-id="7eabb-114">Пример того, как можно выполнить потоковую передачу с помощью XAudio2, см. [в разделе как передавать звук с диска](how-to--stream-a-sound-from-disk.md).</span><span class="sxs-lookup"><span data-stu-id="7eabb-114">For an example of how streaming can be accomplished with XAudio2, see [How to: Stream a Sound from Disk](how-to--stream-a-sound-from-disk.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eabb-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7eabb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eabb-116">Потоковая передача звуковых данных</span><span class="sxs-lookup"><span data-stu-id="7eabb-116">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="7eabb-117">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="7eabb-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



