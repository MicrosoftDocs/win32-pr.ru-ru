---
title: Запись компакт-диска
description: Запись компакт-диска
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Проигрыватель Windows Media, запись компакт-дисков
- Объектная модель проигрывателя Windows Media, запись компакт-дисков
- Объектная модель, запись компакт-диска
- Элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Элемент управления ActiveX, запись компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Проигрыватель Windows Media Mobile, запись компакт-дисков
- Запись компакт-дисков, о программе
- запись компакт-дисков, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133507"
---
# <a name="burning-a-cd"></a><span data-ttu-id="220bc-112">Запись компакт-диска</span><span class="sxs-lookup"><span data-stu-id="220bc-112">Burning a CD</span></span>

<span data-ttu-id="220bc-113">В этом разделе описывается, как использовать интерфейс [ивмпкдромбурн](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) для записи музыки на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="220bc-113">This section describes how to use the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface to burn music to a CD.</span></span> <span data-ttu-id="220bc-114">Интерфейс **ивмпкдромбурн** предоставляет функциональные возможности для записи списков воспроизведения на компакт-диски в виде данных или звуковых дорожек, а также для стирания CD RWS.</span><span class="sxs-lookup"><span data-stu-id="220bc-114">The **IWMPCdromBurn** interface provides functionality for burning playlists to CDs as either data or audio tracks, as well as erasing CD-RWs.</span></span>

<span data-ttu-id="220bc-115">Использование кода</span><span class="sxs-lookup"><span data-stu-id="220bc-115">Code Usage</span></span>

<span data-ttu-id="220bc-116">В примерах кода в этом разделе используются классы библиотеки активных шаблонов (ATL), такие как **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="220bc-116">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

<span data-ttu-id="220bc-117">Включаемые заголовки</span><span class="sxs-lookup"><span data-stu-id="220bc-117">Included Headers</span></span>

<span data-ttu-id="220bc-118">Чтобы использовать код в этом разделе, включите следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="220bc-118">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



<span data-ttu-id="220bc-119">Указатели интерфейса</span><span class="sxs-lookup"><span data-stu-id="220bc-119">Interface Pointers</span></span>

<span data-ttu-id="220bc-120">Интерфейсы для проигрывателя Windows Media хранятся в следующих переменных члена:</span><span class="sxs-lookup"><span data-stu-id="220bc-120">The interfaces for Windows Media Player are stored in the following member variables:</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="220bc-121">В следующих разделах описывается использование API записи компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="220bc-121">The following topics describe how to use the CD burning API.</span></span>

-   [<span data-ttu-id="220bc-122">Получение интерфейса записи компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="220bc-122">Retrieving the CD Burning Interface</span></span>](retrieving-the-cd-burning-interface.md)
-   [<span data-ttu-id="220bc-123">Запуск процесса записи</span><span class="sxs-lookup"><span data-stu-id="220bc-123">Starting the Burn Process</span></span>](starting-the-burn-process.md)
-   [<span data-ttu-id="220bc-124">Стирание перезаписываемого компакт-диска</span><span class="sxs-lookup"><span data-stu-id="220bc-124">Erasing a Rewritable CD</span></span>](erasing-a-rewritable-cd.md)
-   [<span data-ttu-id="220bc-125">Получение состояния диска и диска</span><span class="sxs-lookup"><span data-stu-id="220bc-125">Retrieving the Drive and Disc Status</span></span>](retrieving-the-drive-and-disc-status.md)
-   [<span data-ttu-id="220bc-126">Получение состояния записи</span><span class="sxs-lookup"><span data-stu-id="220bc-126">Retrieving the Burn Status</span></span>](retrieving-the-burn-status.md)

## <a name="related-topics"></a><span data-ttu-id="220bc-127">См. также</span><span class="sxs-lookup"><span data-stu-id="220bc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="220bc-128">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="220bc-128">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




