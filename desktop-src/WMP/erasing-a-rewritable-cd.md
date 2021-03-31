---
title: Стирание перезаписываемого компакт-диска
description: Стирание перезаписываемого компакт-диска
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Проигрыватель Windows Media, запись компакт-дисков
- Объектная модель проигрывателя Windows Media, запись компакт-дисков
- Объектная модель, запись компакт-диска
- Элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Элемент управления ActiveX, запись компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Проигрыватель Windows Media Mobile, запись компакт-дисков
- Запись компакт-дисков, очистка перезаписываемых компактных дисков
- запись компакт-дисков, очистка перезаписываемых компакт-дисков
- Удаление перезаписываемых компакт-дисков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069568"
---
# <a name="erasing-a-rewritable-cd"></a><span data-ttu-id="3d609-113">Стирание перезаписываемого компакт-диска</span><span class="sxs-lookup"><span data-stu-id="3d609-113">Erasing a Rewritable CD</span></span>

<span data-ttu-id="3d609-114">Интерфейс [ивмпкдромбурн](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) предоставляет метод для СТИРАНИЯ дисков CD-RW.</span><span class="sxs-lookup"><span data-stu-id="3d609-114">The [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface provides a method for erasing CD-RW discs.</span></span> <span data-ttu-id="3d609-115">Перед стиранием компакт-диска необходимо убедиться, что операция поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3d609-115">Before erasing a CD, you must first ensure that the operation is supported.</span></span> <span data-ttu-id="3d609-116">Дополнительные сведения см. [в разделе Получение состояния диска и](retrieving-the-drive-and-disc-status.md)диска.</span><span class="sxs-lookup"><span data-stu-id="3d609-116">For more information, see [Retrieving the Drive and Disc Status](retrieving-the-drive-and-disc-status.md).</span></span>

<span data-ttu-id="3d609-117">Чтобы начать Стирание содержимого перезаписываемого компакт-диска, вызовите метод [ивмпкдромбурн:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="3d609-117">To begin erasing the contents of a rewritable CD, call [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span>


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a><span data-ttu-id="3d609-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3d609-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d609-119">**Запись компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="3d609-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="3d609-120">**Получение интерфейса записи компакт-дисков**</span><span class="sxs-lookup"><span data-stu-id="3d609-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="3d609-121">**Запуск процесса записи**</span><span class="sxs-lookup"><span data-stu-id="3d609-121">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="3d609-122">**Получение состояния диска и диска**</span><span class="sxs-lookup"><span data-stu-id="3d609-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="3d609-123">**Получение состояния записи**</span><span class="sxs-lookup"><span data-stu-id="3d609-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




