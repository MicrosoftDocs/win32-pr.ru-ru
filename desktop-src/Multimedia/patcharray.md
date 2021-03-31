---
title: ПАТЧАРРАЙ (Ммсистем. h)
description: ПАТЧАРРАЙ — это тип, используемый для определения массива исправлений MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- ПАТЧАРРАЙ МИДИПАТЧСИЗЕ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892749"
---
# <a name="patcharray"></a><span data-ttu-id="8b452-104">патчаррай</span><span class="sxs-lookup"><span data-stu-id="8b452-104">PATCHARRAY</span></span>

<span data-ttu-id="8b452-105">ПАТЧАРРАЙ — это тип, используемый для определения массива исправлений MIDI.</span><span class="sxs-lookup"><span data-stu-id="8b452-105">PATCHARRAY is a type used to define an array of MIDI patches.</span></span>


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="8b452-106">**ПАТЧАРРАЙ \[ мидипатчсизе\]**</span><span class="sxs-lookup"><span data-stu-id="8b452-106">**PATCHARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b452-107">Каждый элемент в массиве соответствует исправлению с каждым из 16 битов, представляющим один из 16 каналов MIDI.</span><span class="sxs-lookup"><span data-stu-id="8b452-107">Each element in the array corresponds to a patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="8b452-108">Биты задаются для каждого канала, который использует это конкретное исправление.</span><span class="sxs-lookup"><span data-stu-id="8b452-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="8b452-109">Например, если номер исправления 0 используется физическими каналами MIDI 0 и 8, то элемент 0 массива должен иметь значение 0x0101.</span><span class="sxs-lookup"><span data-stu-id="8b452-109">For example, if patch number 0 is used by physical MIDI channels 0 and 8, element 0 of the array should be set to 0x0101.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b452-110">Требования</span><span class="sxs-lookup"><span data-stu-id="8b452-110">Requirements</span></span>



| <span data-ttu-id="8b452-111">Требование</span><span class="sxs-lookup"><span data-stu-id="8b452-111">Requirement</span></span> | <span data-ttu-id="8b452-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8b452-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b452-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b452-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8b452-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b452-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8b452-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b452-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8b452-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b452-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8b452-117">Версия</span><span class="sxs-lookup"><span data-stu-id="8b452-117">Version</span></span><br/>                  | <span data-ttu-id="8b452-118">Цифровой интерфейс MIDI, типы MIDI</span><span class="sxs-lookup"><span data-stu-id="8b452-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="8b452-119">Header</span><span class="sxs-lookup"><span data-stu-id="8b452-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b452-120"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b452-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b452-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b452-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b452-122">Типы MIDI</span><span class="sxs-lookup"><span data-stu-id="8b452-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





