---
title: Разработка анимации
description: Разработка анимации
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986357"
---
# <a name="animation-design"></a><span data-ttu-id="9a125-103">Разработка анимации</span><span class="sxs-lookup"><span data-stu-id="9a125-103">Animation Design</span></span>

<span data-ttu-id="9a125-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a125-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

### <a name="image-design"></a><span data-ttu-id="9a125-105">Разработка образа</span><span class="sxs-lookup"><span data-stu-id="9a125-105">Image Design</span></span>

<span data-ttu-id="9a125-106">Палитра Microsoft Office используется при проектировании символов, чтобы максимально сокращать возможные проблемы при реализации палитры.</span><span class="sxs-lookup"><span data-stu-id="9a125-106">Use the Microsoft Office Palette when designing your characters to minimize any potential palette realization issues.</span></span> <span data-ttu-id="9a125-107">Избегайте выбора цвета прозрачности, аналогичного цвету, используемому в документе.</span><span class="sxs-lookup"><span data-stu-id="9a125-107">Avoid selecting a transparency color that is similar to the colors that you use in your document.</span></span>

### <a name="sounds"></a><span data-ttu-id="9a125-108">Звуки</span><span class="sxs-lookup"><span data-stu-id="9a125-108">Sounds</span></span>

<span data-ttu-id="9a125-109">Microsoft Agent позволяет воспроизводить звуки в анимации.</span><span class="sxs-lookup"><span data-stu-id="9a125-109">Microsoft Agent enables you to play sounds in your animations.</span></span> <span data-ttu-id="9a125-110">Мы рекомендуем не включать звуки для **неактивных** анимаций.</span><span class="sxs-lookup"><span data-stu-id="9a125-110">We recommend you do not include sounds for your **Idle** animations.</span></span> <span data-ttu-id="9a125-111">Это значит, что задержка в середине анимации не будет задерживаться, если агент должен загрузить системную БИБЛИОТЕКУ мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9a125-111">This is so there won't be a delay in the middle of the animation, if Agent has to load the system multimedia DLL.</span></span>

### <a name="frame-size"></a><span data-ttu-id="9a125-112">Размер кадра</span><span class="sxs-lookup"><span data-stu-id="9a125-112">Frame Size</span></span>

<span data-ttu-id="9a125-113">Обычные помощники Office имеют 123 x 93 пикселей.</span><span class="sxs-lookup"><span data-stu-id="9a125-113">Typical Office Assistants are 123 x 93 pixels.</span></span> <span data-ttu-id="9a125-114">Хотя можно создавать символы других размеров, они будут масштабироваться до 123 x 93 в галерее помощников.</span><span class="sxs-lookup"><span data-stu-id="9a125-114">While you can create characters of other sizes, they will be scaled to 123 x 93 in the Assistant Gallery.</span></span>

### <a name="frame-transition"></a><span data-ttu-id="9a125-115">Переход кадров</span><span class="sxs-lookup"><span data-stu-id="9a125-115">Frame Transition</span></span>

<span data-ttu-id="9a125-116">Все **анимации, за** исключением конца, **приветствия**, **показа** и **скрытия** , должны начинаться и заканчиваться анимацией рестпосе.</span><span class="sxs-lookup"><span data-stu-id="9a125-116">All animations except for **Goodbye**, **Greeting**, **Show** and **Hide** should begin and end with the RestPose animation.</span></span> <span data-ttu-id="9a125-117">Microsoft Office не воспроизводит явные анимации **возврата** , поэтому их не следует определять.</span><span class="sxs-lookup"><span data-stu-id="9a125-117">Microsoft Office does not play explicit **Return** animations, so you should not define them.</span></span> <span data-ttu-id="9a125-118">Все анимации также должны иметь ветвь Exit.</span><span class="sxs-lookup"><span data-stu-id="9a125-118">All animations should also have Exit Branching.</span></span> <span data-ttu-id="9a125-119">Выход из ветви позволяет нам "Спешите вверх и завершить" текущую анимацию перед вызовом следующей анимации.</span><span class="sxs-lookup"><span data-stu-id="9a125-119">Exit branching enables us to 'hurry up and finish' the current animation before we call the next animation.</span></span> <span data-ttu-id="9a125-120">Если ветвь Exit не указана, переход между анимациями может быть жерки.</span><span class="sxs-lookup"><span data-stu-id="9a125-120">If you don't supply Exit Branching, the transition between animations may be jerky.</span></span>

### <a name="character-properties"></a><span data-ttu-id="9a125-121">Свойства символов</span><span class="sxs-lookup"><span data-stu-id="9a125-121">Character Properties</span></span>

<span data-ttu-id="9a125-122">Microsoft Agent позволяет задать свойства [**Name**](name-property.md), [**Description**](description-property.md) и [**екстрадата**](extradata-property.md) символа.</span><span class="sxs-lookup"><span data-stu-id="9a125-122">Microsoft Agent enables you to set the character's [**Name**](name-property.md), [**Description**](description-property.md) and [**ExtraData**](extradata-property.md) properties.</span></span> <span data-ttu-id="9a125-123">Microsoft Office использует поле **екстрадата** для хранения одной или нескольких вводной фраз и фраз напоминаний.</span><span class="sxs-lookup"><span data-stu-id="9a125-123">Microsoft Office uses the **ExtraData** field to hold to one or more Introduction Phrases and Reminder Phrases.</span></span> <span data-ttu-id="9a125-124">Microsoft Office выбрать другие фразы для введения в выноску в галерее помощника.</span><span class="sxs-lookup"><span data-stu-id="9a125-124">Microsoft Office picks from the other Introduction Phrases to put in the speech balloon in the Assistant Gallery.</span></span> <span data-ttu-id="9a125-125">Мы используем фразы напоминания при получении напоминания из Outlook.</span><span class="sxs-lookup"><span data-stu-id="9a125-125">We use the Reminder Phrases when you receive a reminder from Outlook.</span></span>

<span data-ttu-id="9a125-126">Поле [**екстрадата**](extradata-property.md) имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="9a125-126">The [**ExtraData**](extradata-property.md) field is formatted as follows:</span></span>

<span data-ttu-id="9a125-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span><span class="sxs-lookup"><span data-stu-id="9a125-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span></span>

<span data-ttu-id="9a125-128">Вводные фразы разделяются парой символов тильды (~), за которой следуют фразы с напоминаниями.</span><span class="sxs-lookup"><span data-stu-id="9a125-128">Intro Phrases are separated by a pair of tilde characters (~), followed by Reminder Phrases.</span></span> <span data-ttu-id="9a125-129">Эти фразы-напоминания также разделяются парой символов тильды.</span><span class="sxs-lookup"><span data-stu-id="9a125-129">These Reminder Phrases are also separated by a pair of tilde characters.</span></span> <span data-ttu-id="9a125-130">Два набора фраз разделяются двумя знаками вставки (^^).</span><span class="sxs-lookup"><span data-stu-id="9a125-130">The two sets of phrases are separated by two caret characters (^^).</span></span> <span data-ttu-id="9a125-131">Количество таких фраз не ограничено, за исключением того, что по крайней мере один из них должен иметь значение.</span><span class="sxs-lookup"><span data-stu-id="9a125-131">There is no limit to the number of each kind of phrase, except that there must be at least one of each.</span></span>

 

 




