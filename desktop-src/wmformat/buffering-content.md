---
title: Буферизация содержимого
description: Буферизация содержимого
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK, буферизация содержимого
- буферизация содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700475"
---
# <a name="buffering-content"></a><span data-ttu-id="4afaf-105">Буферизация содержимого</span><span class="sxs-lookup"><span data-stu-id="4afaf-105">Buffering Content</span></span>

<span data-ttu-id="4afaf-106">Когда объект DataReader открывает потоковый файл, он определяет размер буфера на основе параметров в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="4afaf-106">When the reader object opens a streaming file, it determines the size of the buffer based upon settings in the header of the file.</span></span> <span data-ttu-id="4afaf-107">Вы можете считать, что буфер является сегментом с отверстием в нижней части, в котором утечки по постоянной ставке.</span><span class="sxs-lookup"><span data-stu-id="4afaf-107">You can think of the buffer as a bucket with a hole in the bottom that leaks at a constant rate.</span></span> <span data-ttu-id="4afaf-108">При условии, что скорость заполнения контейнера не превышает скорость, с которой происходит утечка, контейнер никогда не будет переполнен.</span><span class="sxs-lookup"><span data-stu-id="4afaf-108">As long as the rate at which the bucket is filled is not, on average, greater than the rate at which it is leaking, the bucket will never overflow.</span></span>

<span data-ttu-id="4afaf-109">Скорость, с которой утечки мнимых сегментов является скоростью потока.</span><span class="sxs-lookup"><span data-stu-id="4afaf-109">The rate at which the imaginary bucket leaks is the bit rate of the stream.</span></span> <span data-ttu-id="4afaf-110">Скорость, с которой заполняется контейнер, — фактическая скорость потока потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="4afaf-110">The rate at which the bucket fills is the actual streaming bit rate.</span></span> <span data-ttu-id="4afaf-111">Размер данных в сжатом потоке различается по размеру от выборки до выборки в зависимости от объема сжатия, которое было достигнуто.</span><span class="sxs-lookup"><span data-stu-id="4afaf-111">The data in a compressed stream varies in size from sample to sample depending on the amount of compression that was achieved.</span></span> <span data-ttu-id="4afaf-112">Таким же, несмотря на то, что скорость потока в профиле задана, она представляет среднюю скорость, а не константу.</span><span class="sxs-lookup"><span data-stu-id="4afaf-112">Thus, even though the bit rate of the stream is set in the profile, it represents the average bit rate, not a constant.</span></span>

<span data-ttu-id="4afaf-113">Другим параметром потока, важным для процесса буферизации, является окно буфера.</span><span class="sxs-lookup"><span data-stu-id="4afaf-113">The other stream setting important to the buffering process is the buffer window.</span></span> <span data-ttu-id="4afaf-114">Окно буфера измеряется в течение времени и указывает, какой объем содержимого может быть помещен в буфер.</span><span class="sxs-lookup"><span data-stu-id="4afaf-114">The buffer window is measured in time and specifies how much content can be buffered.</span></span> <span data-ttu-id="4afaf-115">Емкость мнимого контейнера можно найти в окне буфера.</span><span class="sxs-lookup"><span data-stu-id="4afaf-115">The capacity of the imaginary bucket can be found using the buffer window.</span></span> <span data-ttu-id="4afaf-116">Например, при наличии потока со скоростью 32 кбит/с и окном буфера, равным 3 секундам, размер буфера составляет 3 секунды от 32 кбит/с или 12 000 байт (32 000 бит в секунду x 3 секунды/8 бит на байт).</span><span class="sxs-lookup"><span data-stu-id="4afaf-116">For example, if you have a stream with a bit rate of 32 Kbps and a buffer window of 3 seconds, the buffer is sized to hold 3 seconds of 32 Kbps content, or 12,000 bytes (32,000 bits per second x 3 seconds / 8 bits per byte).</span></span> <span data-ttu-id="4afaf-117">Кодек ограничивает вариант между фактической скоростью потока потоковой передачи кодированных образцов так, чтобы в течение периода времени, равного окну буфера, средняя скорость не превышала скорость потока.</span><span class="sxs-lookup"><span data-stu-id="4afaf-117">The codec limits the variation between the actual streaming bit rate of encoded samples so that over a period of time equal to the buffer window, the average bit rate is no greater than the bit rate of the stream.</span></span>

<span data-ttu-id="4afaf-118">Как правило, для потока в профиле устанавливается скорость и окно буфера, а модуль записи обрабатывает остальное.</span><span class="sxs-lookup"><span data-stu-id="4afaf-118">Normally, you set the bit rate and buffer window for a stream in a profile, and the writer handles the rest.</span></span> <span data-ttu-id="4afaf-119">Однако при передаче сжатых образцов в средство чтения необходимо обеспечить передачу правильных значений в новый файл, задав скорость потока и окно буфера в целевом профиле в качестве значений из сжатого потока.</span><span class="sxs-lookup"><span data-stu-id="4afaf-119">When passing compressed samples to the reader, however, you must ensure that the correct values are transferred to the new file by setting the bit rate and buffer window for the stream in the destination profile to the values from the compressed stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4afaf-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4afaf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4afaf-121">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="4afaf-121">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="4afaf-122">**Примеры носителей**</span><span class="sxs-lookup"><span data-stu-id="4afaf-122">**Media Samples**</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="4afaf-123">**Входы, потоки и выходные данные**</span><span class="sxs-lookup"><span data-stu-id="4afaf-123">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




