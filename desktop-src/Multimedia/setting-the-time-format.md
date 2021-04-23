---
title: Задание формата времени
description: Задание формата времени
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- Сообщение команды MCI_SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890537"
---
# <a name="setting-the-time-format"></a><span data-ttu-id="0ca57-104">Задание формата времени</span><span class="sxs-lookup"><span data-stu-id="0ca57-104">Setting the Time Format</span></span>

<span data-ttu-id="0ca57-105">Чтобы задать формат времени для открытого устройства, используйте команду [**MCI \_ Set**](mci-set.md) с помощью команды MCI [**\_ Set \_ пармс**](mci-set-parms.md) Structure.</span><span class="sxs-lookup"><span data-stu-id="0ca57-105">Use the [**MCI\_SET**](mci-set.md) command message along with the [**MCI\_SET\_PARMS**](mci-set-parms.md) structure to set the time format for an open device.</span></span> <span data-ttu-id="0ca57-106">Задайте для элемента **двтимеформат** одну из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="0ca57-106">Set the **dwTimeFormat** member to one of the following constants.</span></span>



| <span data-ttu-id="0ca57-107">Константа</span><span class="sxs-lookup"><span data-stu-id="0ca57-107">Constant</span></span>                   | <span data-ttu-id="0ca57-108">Формат времени</span><span class="sxs-lookup"><span data-stu-id="0ca57-108">Time format</span></span>                                          |
|----------------------------|------------------------------------------------------|
| <span data-ttu-id="0ca57-109">\_ \_ байты формата MCI</span><span class="sxs-lookup"><span data-stu-id="0ca57-109">MCI\_FORMAT\_BYTES</span></span>         | <span data-ttu-id="0ca57-110">Байты (в \[ файлах формата PCM с модуляцией кода \] )</span><span class="sxs-lookup"><span data-stu-id="0ca57-110">Bytes (in pulse code modulated \[PCM\] format files)</span></span> |
| <span data-ttu-id="0ca57-111">\_ \_ миллисекунды формата MCI</span><span class="sxs-lookup"><span data-stu-id="0ca57-111">MCI\_FORMAT\_MILLISECONDS</span></span>  | <span data-ttu-id="0ca57-112">Миллисекунды</span><span class="sxs-lookup"><span data-stu-id="0ca57-112">Milliseconds</span></span>                                         |
| <span data-ttu-id="0ca57-113">формат MCI, \_ \_ MSF</span><span class="sxs-lookup"><span data-stu-id="0ca57-113">MCI\_FORMAT\_MSF</span></span>           | <span data-ttu-id="0ca57-114">Минуты в секунду на кадр</span><span class="sxs-lookup"><span data-stu-id="0ca57-114">Minute/second/frame</span></span>                                  |
| <span data-ttu-id="0ca57-115">\_примеры формата \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0ca57-115">MCI\_FORMAT\_SAMPLES</span></span>       | <span data-ttu-id="0ca57-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="0ca57-116">Samples</span></span>                                              |
| <span data-ttu-id="0ca57-117">\_Формат MCI \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="0ca57-117">MCI\_FORMAT\_SMPTE\_24</span></span>     | <span data-ttu-id="0ca57-118">SMPTE, 24 кадра</span><span class="sxs-lookup"><span data-stu-id="0ca57-118">SMPTE, 24 frame</span></span>                                      |
| <span data-ttu-id="0ca57-119">\_Формат MCI \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="0ca57-119">MCI\_FORMAT\_SMPTE\_25</span></span>     | <span data-ttu-id="0ca57-120">SMPTE, 25 кадров</span><span class="sxs-lookup"><span data-stu-id="0ca57-120">SMPTE, 25 frame</span></span>                                      |
| <span data-ttu-id="0ca57-121">\_Формат MCI \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="0ca57-121">MCI\_FORMAT\_SMPTE\_30</span></span>     | <span data-ttu-id="0ca57-122">SMPTE, 30 кадров</span><span class="sxs-lookup"><span data-stu-id="0ca57-122">SMPTE, 30 frame</span></span>                                      |
| <span data-ttu-id="0ca57-123">\_Формат MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="0ca57-123">MCI\_FORMAT\_SMPTE\_30DROP</span></span> | <span data-ttu-id="0ca57-124">SMPTE, 30 кадров</span><span class="sxs-lookup"><span data-stu-id="0ca57-124">SMPTE, 30 frame drop</span></span>                                 |
| <span data-ttu-id="0ca57-125">\_Формат MCI \_ тмсф</span><span class="sxs-lookup"><span data-stu-id="0ca57-125">MCI\_FORMAT\_TMSF</span></span>          | <span data-ttu-id="0ca57-126">Записано/мин в секунду на кадр</span><span class="sxs-lookup"><span data-stu-id="0ca57-126">Track/minute/second/frame</span></span>                            |
| <span data-ttu-id="0ca57-127">MCI \_ Seq \_ Формат \_ сонгптр</span><span class="sxs-lookup"><span data-stu-id="0ca57-127">MCI\_SEQ\_FORMAT\_SONGPTR</span></span>  | <span data-ttu-id="0ca57-128">Указатель песни MIDI</span><span class="sxs-lookup"><span data-stu-id="0ca57-128">MIDI song pointer</span></span>                                    |



 

<span data-ttu-id="0ca57-129">В следующем примере в качестве формата времени задается миллисекунда на устройстве, указанном переменной Вдевицеид с помощью функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0ca57-129">The following example sets the time format to milliseconds on the device specified by the wDeviceID variable using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 