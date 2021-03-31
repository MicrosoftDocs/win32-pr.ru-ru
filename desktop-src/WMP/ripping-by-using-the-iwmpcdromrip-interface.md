---
title: Копирование с помощью интерфейса Ивмпкдромрип
description: Копирование с помощью интерфейса Ивмпкдромрип
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Проигрыватель Windows Media, копирование компакт-дисков
- Объектная модель проигрывателя Windows Media, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- Элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Элемент управления ActiveX, копирование компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Проигрыватель Windows Media Mobile, копирование компакт-дисков
- Копирование компакт-дисков, интерфейс Ивмпкдромрип
- Копирование компакт-дисков, интерфейс Ивмпкдромрип
- Интерфейс Ивмпкдромрип
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890256"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a><span data-ttu-id="0c84b-113">Копирование с помощью интерфейса Ивмпкдромрип</span><span class="sxs-lookup"><span data-stu-id="0c84b-113">Ripping by Using the IWMPCdromRip Interface</span></span>

<span data-ttu-id="0c84b-114">В этом разделе описывается использование интерфейса [ивмпкдромрип](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) для копирования музыки с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="0c84b-114">This section describes how to use the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface to rip music from a CD.</span></span>

<span data-ttu-id="0c84b-115">Копирование компакт-диска с помощью интерфейса **ивмпкдромрип** действует так же, как копирование музыки с помощью пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c84b-115">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="0c84b-116">Скопированное содержимое автоматически добавляется в библиотеку в соответствии с предпочтениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c84b-116">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="0c84b-117">Дополнительные сведения о копировании с компакт-диска см. в разделе «Копирование музыки с CD» в справке проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c84b-117">For more information about CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="0c84b-118">В примерах кода в этом разделе используются классы библиотеки активных шаблонов (ATL), такие как **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="0c84b-118">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="0c84b-119">Включаемые заголовки</span><span class="sxs-lookup"><span data-stu-id="0c84b-119">Included Headers</span></span>

<span data-ttu-id="0c84b-120">Чтобы использовать код в этом разделе, включите следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="0c84b-120">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a><span data-ttu-id="0c84b-121">Указатели интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c84b-121">Interface Pointers</span></span>

<span data-ttu-id="0c84b-122">Интерфейсы для проигрывателя Windows Media хранятся в следующих переменных члена.</span><span class="sxs-lookup"><span data-stu-id="0c84b-122">The interfaces for Windows Media Player are stored in the following member variables.</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="0c84b-123">В следующих разделах описывается использование интерфейса Ивмпкдромрип</span><span class="sxs-lookup"><span data-stu-id="0c84b-123">The Following Sections Describe How to Use the IWMPCdromRip Interface</span></span>

-   [<span data-ttu-id="0c84b-124">Получение интерфейса копирования данных с компакт-диска</span><span class="sxs-lookup"><span data-stu-id="0c84b-124">Retrieving the Ripping Interface</span></span>](retrieving-the-ripping-interface.md)
-   [<span data-ttu-id="0c84b-125">Запуск процесса копирования</span><span class="sxs-lookup"><span data-stu-id="0c84b-125">Starting the Rip Process</span></span>](starting-the-rip-process.md)
-   [<span data-ttu-id="0c84b-126">Получение состояния копирования</span><span class="sxs-lookup"><span data-stu-id="0c84b-126">Retrieving the Rip Status</span></span>](retrieving-the-rip-status.md)
-   [<span data-ttu-id="0c84b-127">Выбор элементов для копирования</span><span class="sxs-lookup"><span data-stu-id="0c84b-127">Selecting Items for Ripping</span></span>](selecting-items-for-ripping.md)

 

 




