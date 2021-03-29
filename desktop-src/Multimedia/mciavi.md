---
title: мЦиави
description: мЦиави
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Устройства MCI, драйвер МЦИАВИ
- Команды MCI, драйвер МЦИАВИ
- Драйвер МЦИАВИ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486897"
---
# <a name="mciavi"></a><span data-ttu-id="7a3a3-106">мЦиави</span><span class="sxs-lookup"><span data-stu-id="7a3a3-106">MCIAVI</span></span>

<span data-ttu-id="7a3a3-107">AVI-файл может содержать более двух потоков — например, последовательность видео, звуковая дорожка на английском языке и французская звуковая дорожка.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-107">An AVI file can contain more than two streams — for example, a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="7a3a3-108">Приложение может использовать поток независимо от других потоков в файле.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-108">Your application can use a stream independently of the other streams in the file.</span></span>

<span data-ttu-id="7a3a3-109">Тип устройства **дигиталвидео** управляет видеофайлами.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-109">The **digitalvideo** device type controls video files.</span></span> <span data-ttu-id="7a3a3-110">Список команд MCI, распознаваемых цифровыми устройствами, см. в разделе [набор команд цифрового видео](digital-video-command-set.md).</span><span class="sxs-lookup"><span data-stu-id="7a3a3-110">For a list of the MCI commands recognized by digital-video devices, see [Digital-Video Command Set](digital-video-command-set.md).</span></span>

<span data-ttu-id="7a3a3-111">Драйвер МЦИАВИ воспроизводит видеопоследовательности и другие потоки данных под контролем команд MCI.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-111">The MCIAVI driver plays video sequences and other data streams under the control of MCI commands.</span></span> <span data-ttu-id="7a3a3-112">Потоки данных могут содержать изображения, звук и палитры.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-112">Data streams can contain images, audio, and palettes.</span></span> <span data-ttu-id="7a3a3-113">Данные изображения могут состоять из изображений с цветовыми палитрами или со сведениями о истинном цвете.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-113">The image data can consist of images with either color palettes or true-color information.</span></span>

<span data-ttu-id="7a3a3-114">Звук синхронизируется с видео в пределах одного сиртиес секунды.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-114">Audio is synchronized with the video within one-thirtieth of a second.</span></span> <span data-ttu-id="7a3a3-115">Однако если звуковое оборудование недоступно, драйвер воспроизводит только поток видео.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-115">If audio hardware is not available, however, the driver plays only the video stream.</span></span> <span data-ttu-id="7a3a3-116">Драйвер МЦИАВИ может удалять видеокадры, если это необходимо, для воспроизведения потока без прерывания звука.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-116">The MCIAVI driver can drop video frames, if necessary, to play a stream without audio interruption.</span></span>

<span data-ttu-id="7a3a3-117">Приложение может использовать службы классов окон МЦивнд вместо интерфейса команд MCI для управления любым драйвером MCI.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-117">Your application can use the MCIWnd window class services instead of the MCI command interface to control any MCI driver.</span></span> <span data-ttu-id="7a3a3-118">Этот класс окон обрабатывает множество деталей управления окном, поддерживающим устройство MCI, и упрощает программирование, необходимое для отправки команд MCI.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-118">This window class handles many of the details of managing the window supporting the MCI device and simplifies the programming required to send the MCI commands.</span></span> <span data-ttu-id="7a3a3-119">Приложение может напрямую использовать службы библиотеки МЦивнд для управления устройством MCI или МЦивнд отображать панель инструментов, полосу прокрутки и меню, позволяющие пользователю управлять устройством.</span><span class="sxs-lookup"><span data-stu-id="7a3a3-119">Your application can use the MCIWnd library services directly to control the MCI device, or it can have MCIWnd display a toolbar, scroll bar, and menus that let the user control the device.</span></span> <span data-ttu-id="7a3a3-120">Дополнительные сведения о классе окна МЦивнд см. в разделе [класс окна мЦивнд](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="7a3a3-120">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span>

 

 




