---
title: Скалярный том
description: Скалярный том
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- Цифровой интерфейс MIDI, скалярный том
- MIDI (цифровой интерфейс музыкального инструмента), скалярный том
- Сопоставитель MIDI, скалярная громкость
- скалярный объем
- Сопоставитель MIDI, Настройка уровней вывода
- Настройка уровней вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39566a10ca909030b60ff197f009b6afe05ce51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068633"
---
# <a name="the-volume-scalar"></a><span data-ttu-id="b01f4-109">Скалярный том</span><span class="sxs-lookup"><span data-stu-id="b01f4-109">The Volume Scalar</span></span>

<span data-ttu-id="b01f4-110">Скалярный уровень громкости состоит в том, чтобы разрешить корректировки между относительными уровнями вывода различных исправлений на синтезаторе.</span><span class="sxs-lookup"><span data-stu-id="b01f4-110">The purpose of the volume scalar is to allow adjustments between the relative output levels of different patches on a synthesizer.</span></span> <span data-ttu-id="b01f4-111">Например, если исправление басов на синтезаторе слишком громко по сравнению с его исправлением пианино, можно изменить схему установки, чтобы уменьшить громкость басов или уменьшить громкость.</span><span class="sxs-lookup"><span data-stu-id="b01f4-111">For example, if the bass patch on a synthesizer is too loud compared with its piano patch, you can change the setup map to scale the bass volume down or the piano volume up.</span></span>

<span data-ttu-id="b01f4-112">Скалярный уровень тома задает процентное значение для изменения всех сообщений основного контроллера MIDI, которые соответствуют сообщению, связанному с сообщением об изменении программы.</span><span class="sxs-lookup"><span data-stu-id="b01f4-112">The volume scalar specifies a percentage value for changing all MIDI main-volume controller messages that follow an associated program-change message.</span></span> <span data-ttu-id="b01f4-113">Например, если значение скаляра для тома равно 50%, средство сопоставления MIDI изменяет сообщения основного контроллера MIDI, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b01f4-113">For example, if the volume scalar value is 50%, the MIDI Mapper modifies MIDI main-volume controller messages as shown in the following illustration.</span></span>

![изображение сопоставителя MIDI](images/mmap-a04.gif)

 

 




