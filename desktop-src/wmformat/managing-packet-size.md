---
title: Управление размером пакетов
description: Управление размером пакетов
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media Format SDK, управление размерами пакетов
- Windows Media Format SDK, размеры пакетов
- профили, размеры пакетов
- профили, Управление размером пакетов
- пакеты, размеры
- пакеты, интерфейс Ивмпаккетсизе
- ивмпаккетсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412698"
---
# <a name="managing-packet-size"></a><span data-ttu-id="28d8b-110">Управление размером пакетов</span><span class="sxs-lookup"><span data-stu-id="28d8b-110">Managing Packet Size</span></span>

<span data-ttu-id="28d8b-111">Модуль записи предназначен для внутреннего управления размером пакетов.</span><span class="sxs-lookup"><span data-stu-id="28d8b-111">The writer is designed to manage the size of packets internally.</span></span> <span data-ttu-id="28d8b-112">Однако у вас могут быть особые требования к приложению, которые вызывают ручное управление размером пакетов в файлах ASF, которые вы пишете.</span><span class="sxs-lookup"><span data-stu-id="28d8b-112">However, you may have specific requirements for your application that call for some manual control over the size of packets in the ASF files that you write.</span></span> <span data-ttu-id="28d8b-113">Windows Media Format SDK предоставляет два интерфейса, [**ивмпаккетсизе**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) и [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , которые позволяют управлять максимальным и минимальным размером пакетов.</span><span class="sxs-lookup"><span data-stu-id="28d8b-113">The Windows Media Format SDK provides two interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) and [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) that enable you to control the maximum and minimum size of packets.</span></span>

<span data-ttu-id="28d8b-114">Оба интерфейса размера пакета представлены в объекте Profile.</span><span class="sxs-lookup"><span data-stu-id="28d8b-114">Both packet size interfaces are exposed in the profile object.</span></span> <span data-ttu-id="28d8b-115">Они также доступны для объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="28d8b-115">They are also available to the reader object.</span></span> <span data-ttu-id="28d8b-116">Как и в случае с другими интерфейсами, связанными с профилями, читатель может обращаться только к методам чтения.</span><span class="sxs-lookup"><span data-stu-id="28d8b-116">As with other profile-related interfaces, the reader can access only the reading methods.</span></span>

<span data-ttu-id="28d8b-117">Размер пакетов оказывает некоторое воздействие на производительность.</span><span class="sxs-lookup"><span data-stu-id="28d8b-117">The size of packets has some effect on performance.</span></span> <span data-ttu-id="28d8b-118">Как правило, чем меньше размер пакета, тем более фрагментированными являются данные в файле.</span><span class="sxs-lookup"><span data-stu-id="28d8b-118">In general, the smaller the packet size, the more fragmented the data is within a file.</span></span> <span data-ttu-id="28d8b-119">Чем сложнее Фрагментирование файла, тем менее эффективным будет его перестроение.</span><span class="sxs-lookup"><span data-stu-id="28d8b-119">The more fragmented a file is, the less efficient it will be to reconstruct it.</span></span> <span data-ttu-id="28d8b-120">В сценарии потоковой передачи это может не быть важным фактором, поскольку процесс чтения файла из источника в Интернете обычно неэффективен.</span><span class="sxs-lookup"><span data-stu-id="28d8b-120">In a streaming scenario, this may not be an important consideration, as the process of reading a file from an Internet source is generally inefficient.</span></span> <span data-ttu-id="28d8b-121">Тем не менее, при работе с файлом локально это может быть важно.</span><span class="sxs-lookup"><span data-stu-id="28d8b-121">When dealing with a file locally however, this might be a consideration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28d8b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="28d8b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28d8b-123">**Интерфейс Ивмпаккетсизе**</span><span class="sxs-lookup"><span data-stu-id="28d8b-123">**IWMPacketSize Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[<span data-ttu-id="28d8b-124">**Интерфейс IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="28d8b-124">**IWMPacketSize2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[<span data-ttu-id="28d8b-125">**Работа с профилями**</span><span class="sxs-lookup"><span data-stu-id="28d8b-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




