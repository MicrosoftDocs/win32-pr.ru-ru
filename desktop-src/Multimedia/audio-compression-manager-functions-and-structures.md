---
title: Функции и структуры диспетчера аудиосжатия
description: Функции и структуры диспетчера аудиосжатия
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- мультимедиа аудио, функции ACM
- функции Audio, ACM
- Диспетчер аудиосжатия (ACM), функции
- ACM (диспетчер аудиосжатия), функции
- мультимедиа аудио, структуры ACM
- звуковые, ACM структуры
- Диспетчер аудиосжатия (ACM), структуры
- ACM (диспетчер аудиосжатия), структуры
- Структуры ACM
- Функции ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650326"
---
# <a name="audio-compression-manager-functions-and-structures"></a><span data-ttu-id="5fe3d-113">Функции и структуры диспетчера аудиосжатия</span><span class="sxs-lookup"><span data-stu-id="5fe3d-113">Audio Compression Manager Functions and Structures</span></span>

<span data-ttu-id="5fe3d-114">Функции ACM делятся на несколько категорий.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-114">The ACM functions fall into several categories.</span></span> <span data-ttu-id="5fe3d-115">Соглашения об именовании для функций упрощают определение этих категорий.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-115">Naming conventions for the functions make it easy to identify these categories.</span></span> <span data-ttu-id="5fe3d-116">Имена функций (с двумя исключениями) имеют форму *акмграупфунктион*, где *Group* определяет категорию ACM (например, "драйвер", "формат", "Форматтаг", "Filter", "Филтертаг" или "Stream"), а *функция* описывает действие, выполняемое функцией.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-116">Function names (with two exceptions) are of the form *acmGroupFunction*, where *Group* designates the ACM category (such as "Driver," "Format," "FormatTag," "Filter," "FilterTag," or "Stream"), and *Function* describes the action performed by the function.</span></span>

<span data-ttu-id="5fe3d-117">Функции в группах фильтров и форматов очень похожи.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-117">The functions in the filter and format groups are very similar.</span></span> <span data-ttu-id="5fe3d-118">Почти все функции, которые работают с фильтрами, имеют параллельную функцию, которая работает с форматами.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-118">Almost every function that acts on filters has a parallel function that acts on formats.</span></span>

<span data-ttu-id="5fe3d-119">В группе форматов некоторые функции используют Теги формата волн-Audio (элемент **вформаттаг** структуры [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ), а для других требуются полные форматы аудио-файлов (полная структура **вавеформатекс** ).</span><span class="sxs-lookup"><span data-stu-id="5fe3d-119">In the format group, some functions use waveform-audio format tags (the **wFormatTag** member of a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure) while others require full waveform-audio formats (the full **WAVEFORMATEX** structure).</span></span> <span data-ttu-id="5fe3d-120">(Справочные сведения о структуре **вавеформатекс** см. в разделе [Error](error.md).)</span><span class="sxs-lookup"><span data-stu-id="5fe3d-120">(For reference information about the **WAVEFORMATEX** structure, see [Error](error.md).)</span></span>

<span data-ttu-id="5fe3d-121">В группе фильтров некоторые функции используют теги фильтра волновой волны (элемент **двфилтертаг** структуры [**вавефилтер**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), а для других требуются полные фильтры аудио-сигнала (полная структура **вавефилтер** ).</span><span class="sxs-lookup"><span data-stu-id="5fe3d-121">In the filter group, some functions use waveform-audio filter tags (the **dwFilterTag** member of a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure), while others require full waveform-audio filters (the full **WAVEFILTER** structure).</span></span>

<span data-ttu-id="5fe3d-122">Функции в группе потока представляют собой множество шагов, участвующих в преобразовании: открытие экземпляра преобразования, подготовка к преобразованию, выполнение преобразования, очистка после завершения преобразования и закрытие экземпляра преобразования.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-122">The functions in the stream group represent the many steps involved in a conversion: opening a conversion instance, preparing for the conversion, performing the conversion, cleaning up after the conversion is complete, and closing the conversion instance.</span></span>

 

 