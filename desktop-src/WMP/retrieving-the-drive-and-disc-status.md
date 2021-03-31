---
title: Получение состояния диска и диска
description: Получение состояния диска и диска
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Проигрыватель Windows Media, запись компакт-дисков
- Объектная модель проигрывателя Windows Media, запись компакт-дисков
- Объектная модель, запись компакт-диска
- Элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Элемент управления ActiveX, запись компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Проигрыватель Windows Media Mobile, запись компакт-дисков
- Запись компакт-дисков, получение состояния диска и диска
- запись компакт-дисков, получение состояния диска и диска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890259"
---
# <a name="retrieving-the-drive-and-disc-status"></a><span data-ttu-id="55a13-112">Получение состояния диска и диска</span><span class="sxs-lookup"><span data-stu-id="55a13-112">Retrieving the Drive and Disc Status</span></span>

<span data-ttu-id="55a13-113">Перед запуском операции записи компакт-дисков необходимо убедиться, что выбранный дисковод компакт-дисков поддерживает операцию, которую необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="55a13-113">Before starting a CD burning operation, you must ensure that the selected CD-ROM drive supports the operation you want to perform.</span></span> <span data-ttu-id="55a13-114">Например, перед вызовом [ивмпкдромбурн:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase)необходимо убедиться, что компакт-диск может быть удален.</span><span class="sxs-lookup"><span data-stu-id="55a13-114">For instance, you must check that a CD is capable of being erased before calling [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span> <span data-ttu-id="55a13-115">В следующем коде показан пример использования [ивмпкдромбурн::](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) an, чтобы определить, поддерживается ли операция:</span><span class="sxs-lookup"><span data-stu-id="55a13-115">The following code shows an example of using [IWMPCdromBurn::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) to determine whether an operation is supported:</span></span>


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="55a13-116">См. также</span><span class="sxs-lookup"><span data-stu-id="55a13-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55a13-117">**Запись компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="55a13-117">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="55a13-118">**Получение интерфейса записи компакт-дисков**</span><span class="sxs-lookup"><span data-stu-id="55a13-118">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="55a13-119">**Запуск процесса записи**</span><span class="sxs-lookup"><span data-stu-id="55a13-119">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="55a13-120">**Стирание перезаписываемого компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="55a13-120">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="55a13-121">**Получение состояния записи**</span><span class="sxs-lookup"><span data-stu-id="55a13-121">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




