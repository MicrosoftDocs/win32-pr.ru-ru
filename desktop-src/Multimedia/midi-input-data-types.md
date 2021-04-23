---
title: Типы входных данных MIDI
description: Типы входных данных MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), типы входных данных
- MIDI (цифровой интерфейс музыкального инструмента), типы входных данных
- запись аудио MIDI, типов входных данных
- Типы входных данных MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672279"
---
# <a name="midi-input-data-types"></a><span data-ttu-id="5ff41-107">Типы входных данных MIDI</span><span class="sxs-lookup"><span data-stu-id="5ff41-107">MIDI Input Data Types</span></span>

<span data-ttu-id="5ff41-108">Windows определяет следующие типы данных для входных функций MIDI.</span><span class="sxs-lookup"><span data-stu-id="5ff41-108">Windows defines the following data types for the MIDI input functions.</span></span>



| <span data-ttu-id="5ff41-109">Значение</span><span class="sxs-lookup"><span data-stu-id="5ff41-109">Value</span></span>                            | <span data-ttu-id="5ff41-110">Значение</span><span class="sxs-lookup"><span data-stu-id="5ff41-110">Meaning</span></span>                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff41-111">**хмидиин**</span><span class="sxs-lookup"><span data-stu-id="5ff41-111">**HMIDIIN**</span></span>                      | <span data-ttu-id="5ff41-112">Работа устройства ввода MIDI.</span><span class="sxs-lookup"><span data-stu-id="5ff41-112">Handle of a MIDI input device.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="5ff41-113">**мидихдр**</span><span class="sxs-lookup"><span data-stu-id="5ff41-113">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | <span data-ttu-id="5ff41-114">Заголовок для буфера потока или блок данных, исключающих систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="5ff41-114">Header for a stream buffer or a block of MIDI system-exclusive data.</span></span> <span data-ttu-id="5ff41-115">Для входных приложений эта структура записывает только данные, не зависящие от системы (потоковая передача не поддерживается для ввода MIDI).</span><span class="sxs-lookup"><span data-stu-id="5ff41-115">For input applications, this structure records only system-exclusive data (streaming is not supported for MIDI input).</span></span> |
| [<span data-ttu-id="5ff41-116">**мидиинкапс**</span><span class="sxs-lookup"><span data-stu-id="5ff41-116">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | <span data-ttu-id="5ff41-117">Структура, используемая для получения сведений о возможностях входного устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="5ff41-117">Structure used to inquire about the capabilities of a MIDI input device.</span></span>                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="5ff41-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5ff41-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff41-119">Запись звука MIDI</span><span class="sxs-lookup"><span data-stu-id="5ff41-119">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 