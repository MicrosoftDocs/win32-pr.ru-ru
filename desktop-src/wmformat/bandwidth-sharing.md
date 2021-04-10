---
title: Совместное использование пропускной способности
description: Совместное использование пропускной способности
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Media Format SDK, совместное использование пропускной способности
- Расширенный формат систем (ASF), совместное использование пропускной способности
- ASF (Расширенный системный формат), совместное использование пропускной способности
- Windows Media Format SDK, потоки
- Расширенный системный формат (ASF), потоки
- ASF (Расширенный системный формат), потоки
- Совместное использование пропускной способности, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069588"
---
# <a name="bandwidth-sharing"></a><span data-ttu-id="81595-110">Совместное использование пропускной способности</span><span class="sxs-lookup"><span data-stu-id="81595-110">Bandwidth Sharing</span></span>

<span data-ttu-id="81595-111">В файле можно указать потоки, которые при совместном использовании используют меньшую пропускную способность, чем сумма указанных бит.</span><span class="sxs-lookup"><span data-stu-id="81595-111">You can specify streams in a file that, when taken together, use less bandwidth than the sum of their stated bit rates combined.</span></span> <span data-ttu-id="81595-112">Указав совместное использование пропускной способности в профиле, вы можете понять, что доступная пропускная способность, необходимая для потоковой передачи файла, не так, как в противном случае.</span><span class="sxs-lookup"><span data-stu-id="81595-112">By specifying bandwidth sharing in the profile, you clarify to reading applications that the available bandwidth needed to stream the file is not what it might otherwise seem.</span></span>

<span data-ttu-id="81595-113">Ни один из объектов пакета SDK для формата Windows Media не изменяет их поведение в ответ на сведения о совместном использовании пропускной способности, что предоставляется исключительно таким образом, чтобы при чтении приложения можно было учитывать, можно ли воспроизвести файл с ограниченной пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="81595-113">None of the objects of the Windows Media Format SDK change their behavior in response to bandwidth sharing information, which is provided solely so that reading applications can take it into account when determining whether a file can be played with restricted bandwidth delivery.</span></span>

<span data-ttu-id="81595-114">Для общего доступа к пропускной способности настраивается объект совместного использования пропускной способности, который добавляется в профиль перед началом записи файла.</span><span class="sxs-lookup"><span data-stu-id="81595-114">Bandwidth sharing is configured with a bandwidth sharing object and is added to a profile before beginning to write a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81595-115">См. также</span><span class="sxs-lookup"><span data-stu-id="81595-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81595-116">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="81595-116">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="81595-117">**Объект, совместно использующие пропускную способность**</span><span class="sxs-lookup"><span data-stu-id="81595-117">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="81595-118">**Интерфейс Ивмбандвидсшаринг**</span><span class="sxs-lookup"><span data-stu-id="81595-118">**IWMBandwidthSharing Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="81595-119">**Интерфейс IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="81595-119">**IWMProfile3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[<span data-ttu-id="81595-120">**Совместное использование пропускной способности**</span><span class="sxs-lookup"><span data-stu-id="81595-120">**Using Bandwidth Sharing**</span></span>](using-bandwidth-sharing.md)
</dt> </dl>

 

 




