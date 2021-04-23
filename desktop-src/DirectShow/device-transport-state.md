---
description: Состояние транспорта устройства
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Состояние транспорта устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423162"
---
# <a name="device-transport-state"></a><span data-ttu-id="742a9-103">Состояние транспорта устройства</span><span class="sxs-lookup"><span data-stu-id="742a9-103">Device Transport State</span></span>

<span data-ttu-id="742a9-104">Чтобы получить текущее состояние устройства, например воспроизведение, пауза или остановка, вызовите метод [**иамексттранспорт:: Get \_**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) .</span><span class="sxs-lookup"><span data-stu-id="742a9-104">To retrieve the current state of the device, such as play, pause, or stop, call the [**IAMExtTransport::get\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) method.</span></span> <span data-ttu-id="742a9-105">Метод получает константу, которая указывает состояние устройства:</span><span class="sxs-lookup"><span data-stu-id="742a9-105">The method retrieves a constant that indicates the device state:</span></span>



| <span data-ttu-id="742a9-106">Значение</span><span class="sxs-lookup"><span data-stu-id="742a9-106">Value</span></span>                    | <span data-ttu-id="742a9-107">Состояние устройства</span><span class="sxs-lookup"><span data-stu-id="742a9-107">Device State</span></span> |
|--------------------------|--------------|
| <span data-ttu-id="742a9-108">\_Воспроизведение в режиме ED \_</span><span class="sxs-lookup"><span data-stu-id="742a9-108">ED\_MODE\_PLAY</span></span>           | <span data-ttu-id="742a9-109">Воспроизведение</span><span class="sxs-lookup"><span data-stu-id="742a9-109">Play</span></span>         |
| <span data-ttu-id="742a9-110">\_точка в режиме ED \_</span><span class="sxs-lookup"><span data-stu-id="742a9-110">ED\_MODE\_STOP</span></span>           | <span data-ttu-id="742a9-111">Stop</span><span class="sxs-lookup"><span data-stu-id="742a9-111">Stop</span></span>         |
| <span data-ttu-id="742a9-112">\_заморозить режим ED \_</span><span class="sxs-lookup"><span data-stu-id="742a9-112">ED\_MODE\_FREEZE</span></span>         | <span data-ttu-id="742a9-113">Пауза</span><span class="sxs-lookup"><span data-stu-id="742a9-113">Pause</span></span>        |
| <span data-ttu-id="742a9-114">ED, \_ режим \_ FF</span><span class="sxs-lookup"><span data-stu-id="742a9-114">ED\_MODE\_FF</span></span>             | <span data-ttu-id="742a9-115">Перемотка вперед</span><span class="sxs-lookup"><span data-stu-id="742a9-115">Fast-forward</span></span> |
| <span data-ttu-id="742a9-116">ED \_ Mode \_ выгру</span><span class="sxs-lookup"><span data-stu-id="742a9-116">ED\_MODE\_REW</span></span>            | <span data-ttu-id="742a9-117">Rewind</span><span class="sxs-lookup"><span data-stu-id="742a9-117">Rewind</span></span>       |
| <span data-ttu-id="742a9-118">\_запись в режиме ED \_</span><span class="sxs-lookup"><span data-stu-id="742a9-118">ED\_MODE\_RECORD</span></span>         | <span data-ttu-id="742a9-119">Record</span><span class="sxs-lookup"><span data-stu-id="742a9-119">Record</span></span>       |
| <span data-ttu-id="742a9-120">\_закрепление записи в режиме ED \_ \_</span><span class="sxs-lookup"><span data-stu-id="742a9-120">ED\_MODE\_RECORD\_FREEZE</span></span> | <span data-ttu-id="742a9-121">Запись — приостановка</span><span class="sxs-lookup"><span data-stu-id="742a9-121">Record-pause</span></span> |



 

<span data-ttu-id="742a9-122">Следующий код проверяет состояние устройства:</span><span class="sxs-lookup"><span data-stu-id="742a9-122">The following code checks the device state:</span></span>


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="742a9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="742a9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="742a9-124">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="742a9-124">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



