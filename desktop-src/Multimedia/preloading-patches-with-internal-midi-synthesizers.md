---
title: Предварительная загрузка исправлений с помощью внутренних синтезаторов MIDI
description: Предварительная загрузка исправлений с помощью внутренних синтезаторов MIDI
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), внутренние синтезаторы
- MIDI (цифровой интерфейс музыкального инструмента), внутренние синтезаторы
- Воспроизведение файлов MIDI, внутренних синтезаторов
- внутренние синтезаторы MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), Предварительная загрузка исправлений
- MIDI (цифровой интерфейс музыкального инструмента), Предварительная загрузка исправлений
- Воспроизведение файлов MIDI, Предварительная загрузка исправлений
- Предварительная загрузка исправлений MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987420"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a><span data-ttu-id="a469e-111">Предварительная загрузка исправлений с помощью внутренних синтезаторов MIDI</span><span class="sxs-lookup"><span data-stu-id="a469e-111">Preloading Patches with Internal MIDI Synthesizers</span></span>

<span data-ttu-id="a469e-112">Некоторые внутренние устройства MIDI синтезатора не могут одновременно загружать все свои исправления.</span><span class="sxs-lookup"><span data-stu-id="a469e-112">Some internal MIDI synthesizer devices cannot keep all of their patches loaded simultaneously.</span></span> <span data-ttu-id="a469e-113">Эти устройства должны предварительно загружать свои данные исправлений.</span><span class="sxs-lookup"><span data-stu-id="a469e-113">These devices must preload their patch data.</span></span>

<span data-ttu-id="a469e-114">Windows предоставляет следующие функции для запроса на предварительную загрузку и кэширование заданных исправлений.</span><span class="sxs-lookup"><span data-stu-id="a469e-114">Windows provides the following functions to request that a synthesizer preload and cache specified patches.</span></span>



| <span data-ttu-id="a469e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a469e-115">Value</span></span>                                                      | <span data-ttu-id="a469e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a469e-116">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a469e-117">**мидиауткачепатчес**</span><span class="sxs-lookup"><span data-stu-id="a469e-117">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | <span data-ttu-id="a469e-118">Запрашивает, что внутренняя Предварительная загрузка устройства MIDI синтезатора и кэширование указанных исправлений мелодик.</span><span class="sxs-lookup"><span data-stu-id="a469e-118">Requests that an internal MIDI synthesizer device preload and cache specified melodic patches.</span></span>              |
| [<span data-ttu-id="a469e-119">**мидиауткачедрумпатчес**</span><span class="sxs-lookup"><span data-stu-id="a469e-119">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | <span data-ttu-id="a469e-120">Запрашивает предварительную загрузку внутреннего устройства MIDI и кэширование заданных исправлений, основанных на ключах.</span><span class="sxs-lookup"><span data-stu-id="a469e-120">Requests that an internal MIDI synthesizer device preload and cache specified key-based percussion patches.</span></span> |



 

<span data-ttu-id="a469e-121">Сведения о том, как определить, поддерживает ли определенное устройство предварительную загрузку исправлений, см. в статье [запросы к выходным устройствам MIDI](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="a469e-121">For information on how to determine if a particular device supports preloading patches, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

 

 