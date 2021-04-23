---
description: В следующем разделе описывается, как выполнить простое воспроизведение.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Простое воспроизведение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674360"
---
# <a name="simple-playback"></a><span data-ttu-id="86ebd-103">Простое воспроизведение</span><span class="sxs-lookup"><span data-stu-id="86ebd-103">Simple Playback</span></span>

<span data-ttu-id="86ebd-104">В следующем разделе описывается, как выполнить простое воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="86ebd-104">The following topic describes how to perform simple playback.</span></span>

<span data-ttu-id="86ebd-105">**Выполнение простого воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="86ebd-105">**To perform simple playback**</span></span>

1.  <span data-ttu-id="86ebd-106">Выберите терминал воспроизведения файлов на уровне вызовов.</span><span class="sxs-lookup"><span data-stu-id="86ebd-106">Select the File Playback Terminal at the call level.</span></span>
2.  <span data-ttu-id="86ebd-107">Создайте терминал воспроизведения в вызове TAPI.</span><span class="sxs-lookup"><span data-stu-id="86ebd-107">Create the Playback Terminal on the TAPI call.</span></span>
3.  <span data-ttu-id="86ebd-108">Задайте свойства — имя файла и тип хранилища.</span><span class="sxs-lookup"><span data-stu-id="86ebd-108">Set properties—file name and type of storage.</span></span>
4.  <span data-ttu-id="86ebd-109">Вызовите метод [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) в терминале воспроизведения файлов, чтобы начать воспроизведение потоков.</span><span class="sxs-lookup"><span data-stu-id="86ebd-109">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of streams.</span></span>

<span data-ttu-id="86ebd-110">В следующем примере кода демонстрируется простое воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="86ebd-110">The following example code demonstrates simple playback.</span></span>

<span data-ttu-id="86ebd-111">Сначала используйте интерфейс [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) , чтобы создать терминал для записи.</span><span class="sxs-lookup"><span data-stu-id="86ebd-111">First, use the [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) interface to create the terminal for recording.</span></span> <span data-ttu-id="86ebd-112">Это указывает TSP/MSP выполнить воспроизведение файла в этом вызове.</span><span class="sxs-lookup"><span data-stu-id="86ebd-112">This instructs the TSP/MSP to perform file playback on this call.</span></span> <span data-ttu-id="86ebd-113">TSP/MSP создает терминал для использования приложением и возвращает его при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="86ebd-113">The TSP/MSP creates a terminal for the application to use, and returns it on success.</span></span>


```C++

```



<span data-ttu-id="86ebd-114">Получите указатель интерфейса [**итмедиаплайбакк**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) из интерфейса терминала и используйте его, чтобы задать имя файла для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="86ebd-114">Get the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface pointer from the terminal interface and use it to set the file name to play back.</span></span>


```C++
pMediaPlayback->Release();
```



<span data-ttu-id="86ebd-115">Предполагая, что файл содержит один звуковой поток, а в вызове есть звуковой поток записи, в этом потоке будет воспроизводиться звуковое содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="86ebd-115">Assuming that the file contains one audio stream, and the call has a capture audio stream, the audio content in the file will play back on that stream.</span></span>

 

 



