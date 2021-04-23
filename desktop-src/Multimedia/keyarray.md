---
title: КЭЙАРРАЙ (Ммсистем. h)
description: КЭЙАРРАЙ указывает тип, используемый для определения массива ключей.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- КЭЙАРРАЙ МИДИПАТЧСИЗЕ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672671"
---
# <a name="keyarray"></a><span data-ttu-id="f3328-104">кэйаррай</span><span class="sxs-lookup"><span data-stu-id="f3328-104">KEYARRAY</span></span>

<span data-ttu-id="f3328-105">КЭЙАРРАЙ указывает тип, используемый для определения массива ключей.</span><span class="sxs-lookup"><span data-stu-id="f3328-105">KEYARRAY specifies a type used to define an array of keys.</span></span>


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="f3328-106">**КЭЙАРРАЙ \[ мидипатчсизе\]**</span><span class="sxs-lookup"><span data-stu-id="f3328-106">**KEYARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="f3328-107">Каждый элемент массива соответствует исправлению, основанному на ключах, с каждым из 16 битов, представляющим один из 16 каналов MIDI.</span><span class="sxs-lookup"><span data-stu-id="f3328-107">Each element in the array corresponds to a key-based percussion patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="f3328-108">Биты задаются для каждого канала, который использует это конкретное исправление.</span><span class="sxs-lookup"><span data-stu-id="f3328-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="f3328-109">Например, если исправление для раздела номер 60 используется физическими каналами MIDI 9 и 15, то элементу 60 массива должно быть присвоено значение 0x8200.</span><span class="sxs-lookup"><span data-stu-id="f3328-109">For example, if the percussion patch for key number 60 is used by physical MIDI channels 9 and 15, element 60 of the array should be set to 0x8200.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3328-110">Требования</span><span class="sxs-lookup"><span data-stu-id="f3328-110">Requirements</span></span>



| <span data-ttu-id="f3328-111">Требование</span><span class="sxs-lookup"><span data-stu-id="f3328-111">Requirement</span></span> | <span data-ttu-id="f3328-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f3328-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3328-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3328-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f3328-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f3328-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f3328-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3328-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f3328-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f3328-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f3328-117">Версия</span><span class="sxs-lookup"><span data-stu-id="f3328-117">Version</span></span><br/>                  | <span data-ttu-id="f3328-118">Цифровой интерфейс MIDI, типы MIDI</span><span class="sxs-lookup"><span data-stu-id="f3328-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="f3328-119">Header</span><span class="sxs-lookup"><span data-stu-id="f3328-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3328-120"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3328-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3328-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3328-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3328-122">Типы MIDI</span><span class="sxs-lookup"><span data-stu-id="f3328-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





