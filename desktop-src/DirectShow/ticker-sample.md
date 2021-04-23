---
description: Пример использования Tick
ms.assetid: 1a3de957-70ea-4b9d-94a0-9b0a74f15d78
title: Пример использования Tick
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ecee7400d6a1cad71101359b0ce538077a25673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684644"
---
# <a name="ticker-sample"></a><span data-ttu-id="a1212-103">Пример использования Tick</span><span class="sxs-lookup"><span data-stu-id="a1212-103">Ticker Sample</span></span>

## <a name="description"></a><span data-ttu-id="a1212-104">Описание</span><span class="sxs-lookup"><span data-stu-id="a1212-104">Description</span></span>

<span data-ttu-id="a1212-105">В этом примере для смешения видео и текста используется модуль подготовки видео с смешением.</span><span class="sxs-lookup"><span data-stu-id="a1212-105">This sample uses the Video Mixing Renderer to blend video and text.</span></span> <span data-ttu-id="a1212-106">Он использует интерфейс [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) для смешения текста с нижней частью окна видео.</span><span class="sxs-lookup"><span data-stu-id="a1212-106">It uses the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface to blend text onto the bottom portion of the video window.</span></span>

<span data-ttu-id="a1212-107">Приложение создает точечный рисунок с текстовой строкой по умолчанию и прокручивает его в нижней части экрана.</span><span class="sxs-lookup"><span data-stu-id="a1212-107">The application creates a bitmap with a default text string and scrolls it across the bottom of the screen.</span></span> <span data-ttu-id="a1212-108">Чтобы изменить текст, выберите команду **задать текстовую строку...** в меню " **деление** ".</span><span class="sxs-lookup"><span data-stu-id="a1212-108">To change the text, choose **Set text string...** from the **Ticker** menu.</span></span> <span data-ttu-id="a1212-109">Чтобы задать шрифт, выберите пункт **задать шрифт...** в меню " **деление** ".</span><span class="sxs-lookup"><span data-stu-id="a1212-109">To set the font, choose **Set font...** from the **Ticker** menu.</span></span> <span data-ttu-id="a1212-110">При выборе параметра **использовать статическое изображение** из меню **Ticks** приложение переключается с динамической текстовой строки на статическое растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="a1212-110">If you select **Use static image** from the **Ticker** menu, the application switches from a dynamic text string to a static bitmap image.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a1212-111">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="a1212-111">Downloading the Sample</span></span>

<span data-ttu-id="a1212-112">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1212-112">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1212-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a1212-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1212-114">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1212-114">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



