---
title: Типы выходных данных MIDI
description: Типы выходных данных MIDI
ms.assetid: d0cb0614-e979-4b9f-81ce-13457fdde906
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), типы выходных данных
- MIDI (цифровой интерфейс музыкального инструмента), типы выходных данных
- Воспроизведение файлов MIDI, типы выходных данных
- Типы выходных данных MIDI
- Тип данных МИДИХДР
- Тип данных МИДИАУТКАПС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57911800e0d45c1db515e5b57045aae3856732c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790896"
---
# <a name="midi-output-data-types"></a><span data-ttu-id="ecde1-109">Типы выходных данных MIDI</span><span class="sxs-lookup"><span data-stu-id="ecde1-109">MIDI Output Data Types</span></span>

<span data-ttu-id="ecde1-110">Windows определяет следующие типы данных для выходных функций MIDI.</span><span class="sxs-lookup"><span data-stu-id="ecde1-110">Windows defines the following data types for MIDI output functions.</span></span>



| <span data-ttu-id="ecde1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ecde1-111">Value</span></span>                              | <span data-ttu-id="ecde1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ecde1-112">Meaning</span></span>                                                                              |
|------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ecde1-113">**хмидиаут**</span><span class="sxs-lookup"><span data-stu-id="ecde1-113">**HMIDIOUT**</span></span>                       | <span data-ttu-id="ecde1-114">Маркер устройства вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="ecde1-114">Handle of a MIDI output device.</span></span>                                                      |
| [<span data-ttu-id="ecde1-115">**мидихдр**</span><span class="sxs-lookup"><span data-stu-id="ecde1-115">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)         | <span data-ttu-id="ecde1-116">Заголовок для блока безсистемных или потоковых данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ecde1-116">Header for a block of MIDI system-exclusive or stream data.</span></span>                          |
| [<span data-ttu-id="ecde1-117">**мидиауткапс**</span><span class="sxs-lookup"><span data-stu-id="ecde1-117">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) | <span data-ttu-id="ecde1-118">Структура, используемая для получения сведений о возможностях конкретного выходного устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="ecde1-118">Structure used to inquire about the capabilities of a particular MIDI output device.</span></span> |



 

 

 