---
title: Справочник по программированию для обложки
description: Справочник по программированию для обложки
ms.assetid: 914f6045-7252-4a06-a514-d31ef6d2d03b
keywords:
- Проигрыватель Windows Media, обложки
- Обложки проигрывателя Windows Media, Справочник по программированию
- обложки, Справочник по программированию
- Справочник по обложкам, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30194f0048f4ef66cf32b7c5f3f94c2bd4e190ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773724"
---
# <a name="skin-programming-reference"></a><span data-ttu-id="81d16-107">Справочник по программированию для обложки</span><span class="sxs-lookup"><span data-stu-id="81d16-107">Skin Programming Reference</span></span>

<span data-ttu-id="81d16-108">В справочнике по программированию для обложки документируется следующие элементы и связанные с ними атрибуты, методы и события.</span><span class="sxs-lookup"><span data-stu-id="81d16-108">The Skin Programming Reference documents the following elements and their associated attributes, methods, and events.</span></span>

<span data-ttu-id="81d16-109">Для элементов и атрибутов в этом разделе требуется проигрыватель Windows Media 7,0 или более поздней версии, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="81d16-109">The elements and attributes in this section require Windows Media Player 7.0 or later unless otherwise noted.</span></span>



| <span data-ttu-id="81d16-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="81d16-110">Element</span></span>                                                  | <span data-ttu-id="81d16-111">Описание</span><span class="sxs-lookup"><span data-stu-id="81d16-111">Description</span></span>                                                                         |
|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="81d16-112">Атрибуты окружения</span><span class="sxs-lookup"><span data-stu-id="81d16-112">Ambient Attributes</span></span>](ambient-attributes.md)             | <span data-ttu-id="81d16-113">Атрибуты, применяемые ко всем элементам обложки с упомянутыми исключениями.</span><span class="sxs-lookup"><span data-stu-id="81d16-113">Attributes that apply to all skin elements with exceptions noted.</span></span>                   |
| [<span data-ttu-id="81d16-114">Обработчики событий окружения</span><span class="sxs-lookup"><span data-stu-id="81d16-114">Ambient Event Handlers</span></span>](ambient-event-handlers.md)     | <span data-ttu-id="81d16-115">Обработчики событий, которые могут быть реализованы большинством элементов Skin.</span><span class="sxs-lookup"><span data-stu-id="81d16-115">Event handlers that can be implemented by most skin elements.</span></span>                       |
| [<span data-ttu-id="81d16-116">Атрибуты внешнего события</span><span class="sxs-lookup"><span data-stu-id="81d16-116">Ambient Event Attributes</span></span>](ambient-event-attributes.md) | <span data-ttu-id="81d16-117">Атрибуты, описывающие состояние проигрывателя Windows Media при срабатывании события.</span><span class="sxs-lookup"><span data-stu-id="81d16-117">Attributes detailing the state of Windows Media Player when an event is fired.</span></span>      |
| [<span data-ttu-id="81d16-118">АВТОМЕНЮ</span><span class="sxs-lookup"><span data-stu-id="81d16-118">AUTOMENU</span></span>](automenu-element.md)                         | <span data-ttu-id="81d16-119">Предоставляет способ показа панели быстрого доступа в обложке.</span><span class="sxs-lookup"><span data-stu-id="81d16-119">Provides a way to display the Quick Access Panel in a skin.</span></span>                         |
| [<span data-ttu-id="81d16-120">ПЕРЕКЛЮЧАТЕЛЬ</span><span class="sxs-lookup"><span data-stu-id="81d16-120">BUTTON</span></span>](button-element.md)                             | <span data-ttu-id="81d16-121">Отдельная кнопка.</span><span class="sxs-lookup"><span data-stu-id="81d16-121">A standalone button.</span></span>                                                                |
| [<span data-ttu-id="81d16-122">буттонелемент</span><span class="sxs-lookup"><span data-stu-id="81d16-122">BUTTONELEMENT</span></span>](buttonelement-element.md)               | <span data-ttu-id="81d16-123">Кнопка в группе кнопок.</span><span class="sxs-lookup"><span data-stu-id="81d16-123">A button within a button group.</span></span>                                                     |
| [<span data-ttu-id="81d16-124">BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="81d16-124">BUTTONGROUP</span></span>](buttongroup-element.md)                   | <span data-ttu-id="81d16-125">Группа элементов Button.</span><span class="sxs-lookup"><span data-stu-id="81d16-125">A group of button elements.</span></span>                                                         |
| [<span data-ttu-id="81d16-126">COLUMN</span><span class="sxs-lookup"><span data-stu-id="81d16-126">COLUMN</span></span>](column-element.md)                             | <span data-ttu-id="81d16-127">Представляет столбец внутри элемента управления списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="81d16-127">Represents a column within a playlist control.</span></span>                                      |
| [<span data-ttu-id="81d16-128">ЭЛЕМЕНТЫ управления</span><span class="sxs-lookup"><span data-stu-id="81d16-128">CONTROLS</span></span>](controls-element.md)                         | <span data-ttu-id="81d16-129">Предоставляет доступ к объекту [Controls](controls-object.md) из обложки.</span><span class="sxs-lookup"><span data-stu-id="81d16-129">Provides access to the [Controls](controls-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="81d16-130">кустомслидер</span><span class="sxs-lookup"><span data-stu-id="81d16-130">CUSTOMSLIDER</span></span>](customslider-element.md)                 | <span data-ttu-id="81d16-131">Настраиваемый элемент управления Slider.</span><span class="sxs-lookup"><span data-stu-id="81d16-131">A customizable slider control.</span></span>                                                      |
| [<span data-ttu-id="81d16-132">ПОЛЕ</span><span class="sxs-lookup"><span data-stu-id="81d16-132">EDITBOX</span></span>](editbox-element.md)                           | <span data-ttu-id="81d16-133">Предоставляет пользователям способ ввода текста в обложке.</span><span class="sxs-lookup"><span data-stu-id="81d16-133">Provides a way for users to enter text within a skin.</span></span>                               |
| [<span data-ttu-id="81d16-134">ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="81d16-134">EFFECTS</span></span>](effects-element.md)                           | <span data-ttu-id="81d16-135">Элемент, который содержит и управляет коллекцией эффектов.</span><span class="sxs-lookup"><span data-stu-id="81d16-135">An element that contains and controls a collection of effects.</span></span>                      |
| [<span data-ttu-id="81d16-136">екуализерсеттингс</span><span class="sxs-lookup"><span data-stu-id="81d16-136">EQUALIZERSETTINGS</span></span>](equalizersettings-element.md)       | <span data-ttu-id="81d16-137">Элемент, позволяющий управлять графическим эквалайзером.</span><span class="sxs-lookup"><span data-stu-id="81d16-137">An element allowing manipulation of the graphic equalizer.</span></span>                          |
| [<span data-ttu-id="81d16-138">ДЕТАЛИЗИРОВАН</span><span class="sxs-lookup"><span data-stu-id="81d16-138">ITEM</span></span>](item-element.md)                                 | <span data-ttu-id="81d16-139">Представляет элемент в списке или элементе управления всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="81d16-139">Represents an item in a list box or pop-up control.</span></span>                                 |
| [<span data-ttu-id="81d16-140">LISTBOX</span><span class="sxs-lookup"><span data-stu-id="81d16-140">LISTBOX</span></span>](listbox-element.md)                           | <span data-ttu-id="81d16-141">Предоставляет пользователям возможность выбирать элементы из списка.</span><span class="sxs-lookup"><span data-stu-id="81d16-141">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="81d16-142">МНОГОПОЛЬЗОВАТЕЛЬСКИЕ</span><span class="sxs-lookup"><span data-stu-id="81d16-142">PLAYER</span></span>](player-element.md)                             | <span data-ttu-id="81d16-143">Предоставляет доступ к объекту [Player](player-object.md) из обложки.</span><span class="sxs-lookup"><span data-stu-id="81d16-143">Provides access to the [Player](player-object.md) object from within a skin.</span></span>       |
| [<span data-ttu-id="81d16-144">СПИСКОМ</span><span class="sxs-lookup"><span data-stu-id="81d16-144">PLAYLIST</span></span>](playlist-element.md)                         | <span data-ttu-id="81d16-145">Элемент для управления внешним видом списка воспроизведения в обложке.</span><span class="sxs-lookup"><span data-stu-id="81d16-145">An element for controlling the appearance of a playlist within a skin.</span></span>              |
| [<span data-ttu-id="81d16-146">ПОДСКАЗКИ</span><span class="sxs-lookup"><span data-stu-id="81d16-146">POPUP</span></span>](popup-element.md)                               | <span data-ttu-id="81d16-147">Предоставляет пользователям возможность выбирать элементы из списка.</span><span class="sxs-lookup"><span data-stu-id="81d16-147">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="81d16-148">PROGRESSBAR</span><span class="sxs-lookup"><span data-stu-id="81d16-148">PROGRESSBAR</span></span>](progressbar-element.md)                   | <span data-ttu-id="81d16-149">Предоставляет способ вывода сведений о ходе выполнения в горизонтальном или вертикальном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="81d16-149">Provides a way to display progress information in a horizontal or vertical control.</span></span> |
| [<span data-ttu-id="81d16-150">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81d16-150">SETTINGS</span></span>](settings-element.md)                         | <span data-ttu-id="81d16-151">Предоставляет доступ к объекту [параметров](settings-object.md) из обложки.</span><span class="sxs-lookup"><span data-stu-id="81d16-151">Provides access to the [Settings](settings-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="81d16-152">ГРУППУ</span><span class="sxs-lookup"><span data-stu-id="81d16-152">SLIDER</span></span>](slider-element.md)                             | <span data-ttu-id="81d16-153">Элемент управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="81d16-153">A slider control.</span></span>                                                                   |
| [<span data-ttu-id="81d16-154">ВЛОЖЕННОЕ представление</span><span class="sxs-lookup"><span data-stu-id="81d16-154">SUBVIEW</span></span>](subview-element.md)                           | <span data-ttu-id="81d16-155">Подразделы в представлении, которые могут быть перемещены или скрыты.</span><span class="sxs-lookup"><span data-stu-id="81d16-155">Subsections within a view that can be moved or hidden.</span></span>                              |
| [<span data-ttu-id="81d16-156">ПОЛНОТЕКСТОВЫМ</span><span class="sxs-lookup"><span data-stu-id="81d16-156">TEXT</span></span>](text-element.md)                                 | <span data-ttu-id="81d16-157">Элемент управления, содержащий текст.</span><span class="sxs-lookup"><span data-stu-id="81d16-157">A control containing text.</span></span>                                                          |
| [<span data-ttu-id="81d16-158">THEME</span><span class="sxs-lookup"><span data-stu-id="81d16-158">THEME</span></span>](theme-element.md)                               | <span data-ttu-id="81d16-159">Элемент Main, определяющий файл обложки.</span><span class="sxs-lookup"><span data-stu-id="81d16-159">The main element identifying a skin file.</span></span>                                           |
| [<span data-ttu-id="81d16-160">РОЛИ</span><span class="sxs-lookup"><span data-stu-id="81d16-160">VIDEO</span></span>](video-element.md)                               | <span data-ttu-id="81d16-161">Элемент для указания внешнего вида окна видео.</span><span class="sxs-lookup"><span data-stu-id="81d16-161">An element for specifying the appearance of a video window.</span></span>                         |
| [<span data-ttu-id="81d16-162">видеосеттингс</span><span class="sxs-lookup"><span data-stu-id="81d16-162">VIDEOSETTINGS</span></span>](videosettings-element.md)               | <span data-ttu-id="81d16-163">Элемент, который позволяет управлять различными параметрами видео.</span><span class="sxs-lookup"><span data-stu-id="81d16-163">An element allowing control of various video settings.</span></span>                              |
| [<span data-ttu-id="81d16-164">VIEW</span><span class="sxs-lookup"><span data-stu-id="81d16-164">VIEW</span></span>](view-element.md)                                 | <span data-ttu-id="81d16-165">Указывает, как будет выглядеть пользовательский интерфейс для каждой категории носителя.</span><span class="sxs-lookup"><span data-stu-id="81d16-165">Specifies what the user interface (UI) looks like for each category of media.</span></span>       |
| [<span data-ttu-id="81d16-166">Прочее</span><span class="sxs-lookup"><span data-stu-id="81d16-166">Miscellaneous</span></span>](miscellaneous.md)                       | <span data-ttu-id="81d16-167">Специализированные атрибуты и другие разделы, которые используются при создании обложек.</span><span class="sxs-lookup"><span data-stu-id="81d16-167">Specialized attributes and other miscellaneous topics for use in creating skins.</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="81d16-168">См. также</span><span class="sxs-lookup"><span data-stu-id="81d16-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81d16-169">**Обложки проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="81d16-169">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




