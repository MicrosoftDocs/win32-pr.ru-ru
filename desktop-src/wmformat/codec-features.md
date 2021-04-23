---
title: Функции кодеков
description: Функции кодеков
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- Windows Media Format SDK, функции кодеков
- Windows Media Format SDK, функции
- кодеки, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3623bcb6f338fe11bef3089705801dc3ea047
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253265"
---
# <a name="codec-features"></a><span data-ttu-id="394e8-106">Функции кодеков</span><span class="sxs-lookup"><span data-stu-id="394e8-106">Codec Features</span></span>

<span data-ttu-id="394e8-107">Пакет SDK Windows Media Format поставляется с несколькими аудиокодеками аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="394e8-107">The Windows Media Format SDK is delivered with several audio and video codecs.</span></span> <span data-ttu-id="394e8-108">Вы можете использовать кодеки, предоставляемые для сжатия и распаковки содержимого в соответствии с различными потребностями.</span><span class="sxs-lookup"><span data-stu-id="394e8-108">You can use the codecs provided to compress and decompress content to suit a variety of needs.</span></span> <span data-ttu-id="394e8-109">Кодек, используемый модулем записи для сжатия данных, задается сведениями о конфигурации потока в профиле.</span><span class="sxs-lookup"><span data-stu-id="394e8-109">The codec that is used by the writer to compress data is specified by stream configuration information in the profile.</span></span> <span data-ttu-id="394e8-110">Сведения из профиля сохраняются в заголовке файла, созданного модулем записи.</span><span class="sxs-lookup"><span data-stu-id="394e8-110">Information from the profile is then stored in the header of the file created by the writer.</span></span> <span data-ttu-id="394e8-111">Затем, когда файл открывается модулем чтения или синхронным модулем чтения, сведения о профиле в заголовке определяют кодек, необходимый для распаковки данных.</span><span class="sxs-lookup"><span data-stu-id="394e8-111">Then, when the file is opened by the reader or synchronous reader, the profile information in the header identifies the codec needed to decompress the data.</span></span>

<span data-ttu-id="394e8-112">В этом разделе обсуждаются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="394e8-112">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="394e8-113">Поддерживаемые кодеки</span><span class="sxs-lookup"><span data-stu-id="394e8-113">Supported Codecs</span></span>](supported-codecs.md)
-   [<span data-ttu-id="394e8-114">Кодирование с постоянной скоростью (CBR)</span><span class="sxs-lookup"><span data-stu-id="394e8-114">Constant Bit Rate (CBR) Encoding</span></span>](constant-bit-rate--cbr--encoding.md)
-   [<span data-ttu-id="394e8-115">Кодирование переменной скорости (VBR)</span><span class="sxs-lookup"><span data-stu-id="394e8-115">Variable Bit Rate (VBR) Encoding</span></span>](variable-bit-rate--vbr--encoding.md)
-   [<span data-ttu-id="394e8-116">2-проходная кодировка</span><span class="sxs-lookup"><span data-stu-id="394e8-116">Two-Pass Encoding</span></span>](two-pass-encoding.md)
-   [<span data-ttu-id="394e8-117">Поддержка аудио в высоком разрешении</span><span class="sxs-lookup"><span data-stu-id="394e8-117">High-Resolution Audio Support</span></span>](high-resolution-audio-support.md)
-   [<span data-ttu-id="394e8-118">Низкое задержку звука</span><span class="sxs-lookup"><span data-stu-id="394e8-118">Low-Delay Audio</span></span>](low-delay-audio.md)
-   [<span data-ttu-id="394e8-119">Выходные данные S/PDIF Audio</span><span class="sxs-lookup"><span data-stu-id="394e8-119">S/PDIF Audio Output</span></span>](s-pdif-audio-output.md)
-   [<span data-ttu-id="394e8-120">Видеоизображение</span><span class="sxs-lookup"><span data-stu-id="394e8-120">Video Image</span></span>](video-image.md)
-   [<span data-ttu-id="394e8-121">Шаблоны соответствия устройств</span><span class="sxs-lookup"><span data-stu-id="394e8-121">Device Conformance Templates</span></span>](device-conformance-templates.md)
-   [<span data-ttu-id="394e8-122">Параметры сложности видео</span><span class="sxs-lookup"><span data-stu-id="394e8-122">Video Complexity Settings</span></span>](video-complexity-settings.md)
-   [<span data-ttu-id="394e8-123">Интерполяция кадров</span><span class="sxs-lookup"><span data-stu-id="394e8-123">Frame Interpolation</span></span>](frame-interpolation.md)

## <a name="related-topics"></a><span data-ttu-id="394e8-124">См. также</span><span class="sxs-lookup"><span data-stu-id="394e8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="394e8-125">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="394e8-125">**Features**</span></span>](features.md)
</dt> </dl>

 

 




