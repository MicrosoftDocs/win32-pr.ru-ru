---
title: Поведение отката шрифта HTML
description: Поведение отката шрифта HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105700967"
---
# <a name="html-font-fallback-behavior"></a><span data-ttu-id="babcf-103">Поведение отката шрифта HTML</span><span class="sxs-lookup"><span data-stu-id="babcf-103">HTML font fallback behavior</span></span>

## <a name="platform"></a><span data-ttu-id="babcf-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="babcf-104">Platform</span></span>

<span data-ttu-id="babcf-105">Клиенты — \* \* Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="babcf-105">Clients -\*\* Windows 8.1</span></span>  
<span data-ttu-id="babcf-106">**Серверы —** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="babcf-106">**Servers -** Windows Server 2012 R2</span></span>  


## <a name="description"></a><span data-ttu-id="babcf-107">Описание</span><span class="sxs-lookup"><span data-stu-id="babcf-107">Description</span></span>

<span data-ttu-id="babcf-108">Корпорация Майкрософт обновляет логику шрифтов пользовательского интерфейса для нескольких языков в приложениях для Магазина Windows, использующих HTML.</span><span class="sxs-lookup"><span data-stu-id="babcf-108">Microsoft is updating the logic for UI fonts for several languages in Windows Store apps using HTML.</span></span> <span data-ttu-id="babcf-109">Вместо того чтобы использовать один шрифт для всех языков, шрифт пользовательского интерфейса теперь будет определяться на основе каждого языка.</span><span class="sxs-lookup"><span data-stu-id="babcf-109">Rather than using a single font for all languages, the UI font will now be determined on a per language basis.</span></span> <span data-ttu-id="babcf-110">Например, шрифты пользовательского интерфейса для японского языка теперь будут Меирйо пользовательский интерфейс в приложениях, использующих HTML.</span><span class="sxs-lookup"><span data-stu-id="babcf-110">For example, UI fonts for Japanese will now be Meiryo UI in apps that use HTML.</span></span>

## <a name="manifestation"></a><span data-ttu-id="babcf-111">Проявление</span><span class="sxs-lookup"><span data-stu-id="babcf-111">Manifestation</span></span>

<span data-ttu-id="babcf-112">Приложения, зависящие от старого шрифта, могут выглядеть иначе. Хотя внешний вид приложения будет значительно улучшен благодаря более удобочитаемым шрифтам, возможны проблемы с макетами, которые зависят от размера содержимого, отличного от пикселей.</span><span class="sxs-lookup"><span data-stu-id="babcf-112">Apps that depended on an old font may look different; while your app appearance will be improved overall thanks to more readable fonts, there could be an issue with layouts that depend on pixel-perfect content sizes.</span></span> <span data-ttu-id="babcf-113">Например, некоторые строки содержимого могут быть больше, чем раньше, что привело к непредвиденным разрывам строк и (или) изменению размера элементов контейнера.</span><span class="sxs-lookup"><span data-stu-id="babcf-113">For example, some lines of content may be bigger than they were previously, causing unexpected line breaks and/or resizing of container elements.</span></span> <span data-ttu-id="babcf-114">Однако на практике мы не заметили каких бы то ни было проблем с существующими приложениями.</span><span class="sxs-lookup"><span data-stu-id="babcf-114">However, in practice we haven’t noticed any issues with any existing apps.</span></span>

## <a name="solution"></a><span data-ttu-id="babcf-115">Решение</span><span class="sxs-lookup"><span data-stu-id="babcf-115">Solution</span></span>

<span data-ttu-id="babcf-116">Затронутые приложения могут уменьшить это поведение, указав заданный шрифт через CSS (например, "Font-Family: Меирйо UI"), а не полагаться на старые шрифты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="babcf-116">Affected apps can mitigate this behavior by specifying a given font via CSS (for example, “font-family: Meiryo UI”) instead of relying on the old default fonts.</span></span> <span data-ttu-id="babcf-117">В следующей таблице приведены шрифты пользовательского интерфейса для каждого из имен сценариев.</span><span class="sxs-lookup"><span data-stu-id="babcf-117">The following table provides the UI font for each of the script names.</span></span>



| <span data-ttu-id="babcf-118">Имя сценария</span><span class="sxs-lookup"><span data-stu-id="babcf-118">Script Name</span></span>        | <span data-ttu-id="babcf-119">Шрифт пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="babcf-119">UI Font</span></span>               |
|--------------------|-----------------------|
| <span data-ttu-id="babcf-120">Арабский</span><span class="sxs-lookup"><span data-stu-id="babcf-120">Arabic</span></span>             | <span data-ttu-id="babcf-121">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="babcf-121">Segoe UI</span></span>              |
| <span data-ttu-id="babcf-122">Армянский</span><span class="sxs-lookup"><span data-stu-id="babcf-122">Armenian</span></span>           | <span data-ttu-id="babcf-123">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="babcf-123">Segoe UI</span></span>              |
| <span data-ttu-id="babcf-124">Бенгальский</span><span class="sxs-lookup"><span data-stu-id="babcf-124">Bengali</span></span>            | <span data-ttu-id="babcf-125">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-125">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-126">Бопомофо</span><span class="sxs-lookup"><span data-stu-id="babcf-126">Bopomofo</span></span>           | <span data-ttu-id="babcf-127">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="babcf-127">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="babcf-128">Брайля</span><span class="sxs-lookup"><span data-stu-id="babcf-128">Braille</span></span>            | <span data-ttu-id="babcf-129">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-129">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-130">Бугийский</span><span class="sxs-lookup"><span data-stu-id="babcf-130">Buginese</span></span>           | <span data-ttu-id="babcf-131">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="babcf-131">Leelawadee UI</span></span>         |
| <span data-ttu-id="babcf-132">Канадское слоговое письмо</span><span class="sxs-lookup"><span data-stu-id="babcf-132">Canadian Syllabics</span></span> | <span data-ttu-id="babcf-133">Gadugi</span><span class="sxs-lookup"><span data-stu-id="babcf-133">Gadugi</span></span>                |
| <span data-ttu-id="babcf-134">Чероки</span><span class="sxs-lookup"><span data-stu-id="babcf-134">Cherokee</span></span>           | <span data-ttu-id="babcf-135">Gadugi</span><span class="sxs-lookup"><span data-stu-id="babcf-135">Gadugi</span></span>                |
| <span data-ttu-id="babcf-136">Коптский</span><span class="sxs-lookup"><span data-stu-id="babcf-136">Coptic</span></span>             | <span data-ttu-id="babcf-137">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-137">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-138">(Упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="babcf-138">Han (Simplified)</span></span>   | <span data-ttu-id="babcf-139">Microsoft YaHei UI</span><span class="sxs-lookup"><span data-stu-id="babcf-139">Microsoft YaHei UI</span></span>    |
| <span data-ttu-id="babcf-140">(Традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="babcf-140">Han (Traditional)</span></span>  | <span data-ttu-id="babcf-141">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="babcf-141">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="babcf-142">Кириллица</span><span class="sxs-lookup"><span data-stu-id="babcf-142">Cyrillic</span></span>           | <span data-ttu-id="babcf-143">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="babcf-143">Segoe UI</span></span>              |
| <span data-ttu-id="babcf-144">Девангари</span><span class="sxs-lookup"><span data-stu-id="babcf-144">Devanagari</span></span>         | <span data-ttu-id="babcf-145">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-145">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-146">Дезерет</span><span class="sxs-lookup"><span data-stu-id="babcf-146">Deseret</span></span>            | <span data-ttu-id="babcf-147">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-147">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-148">Эфиопского</span><span class="sxs-lookup"><span data-stu-id="babcf-148">Ethiopic</span></span>           | <span data-ttu-id="babcf-149">Ebrima</span><span class="sxs-lookup"><span data-stu-id="babcf-149">Ebrima</span></span>                |
| <span data-ttu-id="babcf-150">Грузинский</span><span class="sxs-lookup"><span data-stu-id="babcf-150">Georgian</span></span>           | <span data-ttu-id="babcf-151">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="babcf-151">Segoe UI</span></span>              |
| <span data-ttu-id="babcf-152">глаголитик</span><span class="sxs-lookup"><span data-stu-id="babcf-152">Glagolitic</span></span>         | <span data-ttu-id="babcf-153">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-153">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-154">Arial</span><span class="sxs-lookup"><span data-stu-id="babcf-154">Gothic</span></span>             | <span data-ttu-id="babcf-155">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-155">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-156">Греческий</span><span class="sxs-lookup"><span data-stu-id="babcf-156">Greek</span></span>              | <span data-ttu-id="babcf-157">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="babcf-157">Segoe UI</span></span>              |
| <span data-ttu-id="babcf-158">Гуджарати</span><span class="sxs-lookup"><span data-stu-id="babcf-158">Gujarati</span></span>           | <span data-ttu-id="babcf-159">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-159">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-160">Гурмукхи</span><span class="sxs-lookup"><span data-stu-id="babcf-160">Gurmukhi</span></span>           | <span data-ttu-id="babcf-161">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-161">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-162">Иврит</span><span class="sxs-lookup"><span data-stu-id="babcf-162">Hebrew</span></span>             | <span data-ttu-id="babcf-163">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="babcf-163">Segoe UI</span></span>              |
| <span data-ttu-id="babcf-164">Старый курсив</span><span class="sxs-lookup"><span data-stu-id="babcf-164">Old Italic</span></span>         | <span data-ttu-id="babcf-165">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-165">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-166">Яванская письменность</span><span class="sxs-lookup"><span data-stu-id="babcf-166">Javanese</span></span>           | <span data-ttu-id="babcf-167">Текст на яванский</span><span class="sxs-lookup"><span data-stu-id="babcf-167">Javanese Text</span></span>         |
| <span data-ttu-id="babcf-168">Японский</span><span class="sxs-lookup"><span data-stu-id="babcf-168">Japanese</span></span>           | <span data-ttu-id="babcf-169">Пользовательский интерфейс меирйо</span><span class="sxs-lookup"><span data-stu-id="babcf-169">Meiryo UI</span></span>             |
| <span data-ttu-id="babcf-170">Каннада</span><span class="sxs-lookup"><span data-stu-id="babcf-170">Kannada</span></span>            | <span data-ttu-id="babcf-171">Пользовательский интерфейс мирмала</span><span class="sxs-lookup"><span data-stu-id="babcf-171">Mirmala UI</span></span>            |
| <span data-ttu-id="babcf-172">Кхмерский</span><span class="sxs-lookup"><span data-stu-id="babcf-172">Khmer</span></span>              | <span data-ttu-id="babcf-173">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="babcf-173">Leelawadee UI</span></span>         |
| <span data-ttu-id="babcf-174">Корейский</span><span class="sxs-lookup"><span data-stu-id="babcf-174">Korean</span></span>             | <span data-ttu-id="babcf-175">Malgun Gothic</span><span class="sxs-lookup"><span data-stu-id="babcf-175">Malgun Gothic</span></span>         |
| <span data-ttu-id="babcf-176">Лаосский</span><span class="sxs-lookup"><span data-stu-id="babcf-176">Lao</span></span>                | <span data-ttu-id="babcf-177">лилавади</span><span class="sxs-lookup"><span data-stu-id="babcf-177">Leelawadee</span></span>            |
| <span data-ttu-id="babcf-178">Латиница</span><span class="sxs-lookup"><span data-stu-id="babcf-178">Latin</span></span>              | <span data-ttu-id="babcf-179">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="babcf-179">Segoe UI</span></span>              |
| <span data-ttu-id="babcf-180">Малаялам</span><span class="sxs-lookup"><span data-stu-id="babcf-180">Malayalam</span></span>          | <span data-ttu-id="babcf-181">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-181">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-182">Монгольский</span><span class="sxs-lookup"><span data-stu-id="babcf-182">Mongolian</span></span>          | <span data-ttu-id="babcf-183">Mongolian Baiti</span><span class="sxs-lookup"><span data-stu-id="babcf-183">Mongolian Baiti</span></span>       |
| <span data-ttu-id="babcf-184">Мьянма</span><span class="sxs-lookup"><span data-stu-id="babcf-184">Myanmar</span></span>            | <span data-ttu-id="babcf-185">Myanmar Text</span><span class="sxs-lookup"><span data-stu-id="babcf-185">Myanmar Text</span></span>          |
| <span data-ttu-id="babcf-186">н'ко</span><span class="sxs-lookup"><span data-stu-id="babcf-186">N'Ko</span></span>               | <span data-ttu-id="babcf-187">Ebrima</span><span class="sxs-lookup"><span data-stu-id="babcf-187">Ebrima</span></span>                |
| <span data-ttu-id="babcf-188">Блок</span><span class="sxs-lookup"><span data-stu-id="babcf-188">Ogham</span></span>              | <span data-ttu-id="babcf-189">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-189">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-190">Письменность ол-чики</span><span class="sxs-lookup"><span data-stu-id="babcf-190">Ol Chiki</span></span>           | <span data-ttu-id="babcf-191">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-191">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-192">Старая локали Turkic</span><span class="sxs-lookup"><span data-stu-id="babcf-192">Old Turkic</span></span>         | <span data-ttu-id="babcf-193">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-193">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-194">Ория</span><span class="sxs-lookup"><span data-stu-id="babcf-194">Oriya</span></span>              | <span data-ttu-id="babcf-195">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-195">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-196">османя</span><span class="sxs-lookup"><span data-stu-id="babcf-196">Osmanya</span></span>            | <span data-ttu-id="babcf-197">Ebrima</span><span class="sxs-lookup"><span data-stu-id="babcf-197">Ebrima</span></span>                |
| <span data-ttu-id="babcf-198">Блок-PA</span><span class="sxs-lookup"><span data-stu-id="babcf-198">Phags-pa</span></span>           | <span data-ttu-id="babcf-199">Microsoft PhagsPa</span><span class="sxs-lookup"><span data-stu-id="babcf-199">Microsoft PhagsPa</span></span>     |
| <span data-ttu-id="babcf-200">руник</span><span class="sxs-lookup"><span data-stu-id="babcf-200">Runic</span></span>              | <span data-ttu-id="babcf-201">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="babcf-201">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="babcf-202">Сора Сомпенг</span><span class="sxs-lookup"><span data-stu-id="babcf-202">Sora Sompeng</span></span>       | <span data-ttu-id="babcf-203">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-203">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-204">Сингальский</span><span class="sxs-lookup"><span data-stu-id="babcf-204">Sinhala</span></span>            | <span data-ttu-id="babcf-205">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-205">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-206">Сирийский</span><span class="sxs-lookup"><span data-stu-id="babcf-206">Syriac</span></span>             | <span data-ttu-id="babcf-207">Естранжело Едесса</span><span class="sxs-lookup"><span data-stu-id="babcf-207">Estrangelo Edessa</span></span>     |
| <span data-ttu-id="babcf-208">Тай Le</span><span class="sxs-lookup"><span data-stu-id="babcf-208">Tai Le</span></span>             | <span data-ttu-id="babcf-209">Microsoft Tai Le</span><span class="sxs-lookup"><span data-stu-id="babcf-209">Microsoft Tai Le</span></span>      |
| <span data-ttu-id="babcf-210">Новая письменность тай-лю</span><span class="sxs-lookup"><span data-stu-id="babcf-210">New Tai Lue</span></span>        | <span data-ttu-id="babcf-211">Microsoft New Tai Lue</span><span class="sxs-lookup"><span data-stu-id="babcf-211">Microsoft New Tai Lue</span></span> |
| <span data-ttu-id="babcf-212">Тамильский</span><span class="sxs-lookup"><span data-stu-id="babcf-212">Tamil</span></span>              | <span data-ttu-id="babcf-213">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-213">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-214">Телугу</span><span class="sxs-lookup"><span data-stu-id="babcf-214">Telugu</span></span>             | <span data-ttu-id="babcf-215">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="babcf-215">Nirmala UI</span></span>            |
| <span data-ttu-id="babcf-216">Тифинаг</span><span class="sxs-lookup"><span data-stu-id="babcf-216">Tifinagh</span></span>           | <span data-ttu-id="babcf-217">Ebrima</span><span class="sxs-lookup"><span data-stu-id="babcf-217">Ebrima</span></span>                |
| <span data-ttu-id="babcf-218">мальдивский</span><span class="sxs-lookup"><span data-stu-id="babcf-218">Thaana</span></span>             | <span data-ttu-id="babcf-219">MV Boli</span><span class="sxs-lookup"><span data-stu-id="babcf-219">MV Boli</span></span>               |
| <span data-ttu-id="babcf-220">Тайский</span><span class="sxs-lookup"><span data-stu-id="babcf-220">Thai</span></span>               | <span data-ttu-id="babcf-221">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="babcf-221">Leelawadee UI</span></span>         |
| <span data-ttu-id="babcf-222">Тибетский</span><span class="sxs-lookup"><span data-stu-id="babcf-222">Tibetan</span></span>            | <span data-ttu-id="babcf-223">Microsoft Himalaya</span><span class="sxs-lookup"><span data-stu-id="babcf-223">Microsoft Himalaya</span></span>    |
| <span data-ttu-id="babcf-224">Ваи</span><span class="sxs-lookup"><span data-stu-id="babcf-224">Vai</span></span>                | <span data-ttu-id="babcf-225">Ebrima</span><span class="sxs-lookup"><span data-stu-id="babcf-225">Ebrima</span></span>                |
| <span data-ttu-id="babcf-226">Носу</span><span class="sxs-lookup"><span data-stu-id="babcf-226">Yi</span></span>                 | <span data-ttu-id="babcf-227">Microsoft Yi Baiti</span><span class="sxs-lookup"><span data-stu-id="babcf-227">Microsoft Yi Baiti</span></span>    |



 

 

 




