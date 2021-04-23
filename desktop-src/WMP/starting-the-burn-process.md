---
title: Запуск процесса записи
description: Запуск процесса записи
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Проигрыватель Windows Media, запись компакт-дисков
- Объектная модель проигрывателя Windows Media, запись компакт-дисков
- Объектная модель, запись компакт-диска
- Элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Элемент управления ActiveX, запись компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Проигрыватель Windows Media Mobile, запись компакт-дисков
- Запись компакт-дисков, запуск процесса записи
- запись компакт-дисков, запуск процесса записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987208"
---
# <a name="starting-the-burn-process"></a><span data-ttu-id="ca0dc-112">Запуск процесса записи</span><span class="sxs-lookup"><span data-stu-id="ca0dc-112">Starting the Burn Process</span></span>

<span data-ttu-id="ca0dc-113">Перед началом записи необходимо назначить список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ca0dc-113">Before burning can begin, you must assign a playlist to be burned.</span></span> <span data-ttu-id="ca0dc-114">Используйте [ивмпкдромбурн::p UT \_ бурнплайлист](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) , чтобы указать список воспроизведения для записи.</span><span class="sxs-lookup"><span data-stu-id="ca0dc-114">Use [IWMPCdromBurn::put\_burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) to specify a playlist for burning.</span></span>


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



<span data-ttu-id="ca0dc-115">Дополнительные сведения об использовании списков воспроизведения см. в разделе [ивмпплайлист](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span><span class="sxs-lookup"><span data-stu-id="ca0dc-115">For information about using playlists, see [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span></span>

<span data-ttu-id="ca0dc-116">Чтобы начать операцию записи, вызовите метод [ивмпкдромбурн:: стартбурн](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span><span class="sxs-lookup"><span data-stu-id="ca0dc-116">To start the burning operation, call [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span></span>


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



<span data-ttu-id="ca0dc-117">Можно прерывать операцию записи путем вызова [ивмпкдромбурн:: стопбурн](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span><span class="sxs-lookup"><span data-stu-id="ca0dc-117">You can stop the burning operation by calling [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span></span>


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a><span data-ttu-id="ca0dc-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ca0dc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca0dc-119">**Запись компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="ca0dc-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="ca0dc-120">**Получение интерфейса записи компакт-дисков**</span><span class="sxs-lookup"><span data-stu-id="ca0dc-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="ca0dc-121">**Стирание перезаписываемого компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="ca0dc-121">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="ca0dc-122">**Получение состояния диска и диска**</span><span class="sxs-lookup"><span data-stu-id="ca0dc-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="ca0dc-123">**Получение состояния записи**</span><span class="sxs-lookup"><span data-stu-id="ca0dc-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




