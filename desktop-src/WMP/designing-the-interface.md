---
title: Проектирование интерфейса
description: Проектирование интерфейса
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, пользовательские интерфейсы
- обложки, пользовательские интерфейсы
- Создание обложек, пользовательских интерфейсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8070ef6fd4589f762624d7a0b5ee1d380a264066
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133006"
---
# <a name="designing-the-interface"></a><span data-ttu-id="4b366-106">Проектирование интерфейса</span><span class="sxs-lookup"><span data-stu-id="4b366-106">Designing the Interface</span></span>

<span data-ttu-id="4b366-107">После выбора функций можно разработать интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4b366-107">Once the functions have been chosen, the interface can be designed.</span></span> <span data-ttu-id="4b366-108">Для соответствия функциональным возможностям выбран простой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4b366-108">A simple interface was chosen to match the functionality.</span></span> <span data-ttu-id="4b366-109">Символы для элементов управления были выбраны из стандартных элементов управления ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="4b366-109">Symbols for the controls were chosen from standard VCR controls.</span></span>

<span data-ttu-id="4b366-110">На следующем рисунке показано, как будет выглядеть интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4b366-110">The following image shows what the interface will look like.</span></span>

![образец интерфейса](images/ceswmful.png)

-   <span data-ttu-id="4b366-112">**Кнопка Плайпаусе или Плайпаусестоп.**</span><span class="sxs-lookup"><span data-stu-id="4b366-112">**PlayPause or PlayPauseStop button.**</span></span> <span data-ttu-id="4b366-113">Пользователь будет в большей мере коснуться этого, поэтому вы можете подумать о большей кнопке.</span><span class="sxs-lookup"><span data-stu-id="4b366-113">The user will be tapping this the most, so you might consider a larger button.</span></span> <span data-ttu-id="4b366-114">Правый верхний угол обеспечивает хорошее расположение, которое пользователь может быстро найти.</span><span class="sxs-lookup"><span data-stu-id="4b366-114">The upper-right corner makes a good location that the user can find quickly.</span></span> <span data-ttu-id="4b366-115">Сплошная стрелка используется для обозначения воспроизведения и двух вертикальных полос (не показанных здесь) для обозначения приостановки.</span><span class="sxs-lookup"><span data-stu-id="4b366-115">A solid arrow is used to indicate play and two vertical bars (not shown here) will be used to indicate pause.</span></span>
    > [!Note]  
    > <span data-ttu-id="4b366-116">Кнопка Плайпаусестоп может использоваться только при создании обложки для проигрывателя Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4b366-116">The PlayPauseStop button can only be used when creating a skin for Windows Media Player 10 Mobile or later.</span></span>

     

-   <span data-ttu-id="4b366-117">**Кнопка "Закрыть".**</span><span class="sxs-lookup"><span data-stu-id="4b366-117">**Stop button.**</span></span> <span data-ttu-id="4b366-118">Чтобы упростить поиск, он размещается в левом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="4b366-118">To make this easy to find, it is placed at the upper-left corner.</span></span> <span data-ttu-id="4b366-119">Квадрат используется для обозначения «останавливаться».</span><span class="sxs-lookup"><span data-stu-id="4b366-119">A square is used to indicate stop.</span></span> <span data-ttu-id="4b366-120">Если вы создаете обложку для проигрывателя Windows Media 10 Mobile или более поздней версии, кнопка Плайпаусестоп уже предоставляет эту функцию.</span><span class="sxs-lookup"><span data-stu-id="4b366-120">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop button already provides this functionality.</span></span>
-   <span data-ttu-id="4b366-121">**Кнопки "Далее" и "назад".**</span><span class="sxs-lookup"><span data-stu-id="4b366-121">**Next and Prev buttons.**</span></span> <span data-ttu-id="4b366-122">Так как они не будут использоваться как можно чаще, они помещаются слева.</span><span class="sxs-lookup"><span data-stu-id="4b366-122">Since these will not be used as often, they are placed on the left.</span></span> <span data-ttu-id="4b366-123">Следующая кнопка находится выше кнопки назад, так как людям, скорее всего, потребуется переместиться вперед в список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4b366-123">The Next is above the Prev button because people will more likely want to move forward in a playlist.</span></span> <span data-ttu-id="4b366-124">Используются символы двойной стрелки, так как они похожи в функции на элемент управления быстрого перемотки вперед.</span><span class="sxs-lookup"><span data-stu-id="4b366-124">The double-arrow symbols are used because they are similar in function to a fast-forward control.</span></span>
-   <span data-ttu-id="4b366-125">**Ползунок громкости.**</span><span class="sxs-lookup"><span data-stu-id="4b366-125">**Volume trackbar.**</span></span> <span data-ttu-id="4b366-126">Он размещается в нижней части экрана и представляет собой простую линию с кнопкой Thumb на поверх нее.</span><span class="sxs-lookup"><span data-stu-id="4b366-126">This is placed at the bottom of the screen and is a simple line with a thumb button on top of it.</span></span>
-   <span data-ttu-id="4b366-127">**Текстовое поле области.**</span><span class="sxs-lookup"><span data-stu-id="4b366-127">**Marquee text box.**</span></span> <span data-ttu-id="4b366-128">Он помещается под кнопкой Плайпаусе или Плайпаусестоп, чтобы его было легко увидеть.</span><span class="sxs-lookup"><span data-stu-id="4b366-128">This is placed under the PlayPause or PlayPauseStop button so that it is easy to see.</span></span>

<span data-ttu-id="4b366-129">Вы можете запланировать эту первую и поэкспериментировать с размещением каждого элемента пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4b366-129">You may want to sketch this first and experiment with the placement of each user interface element.</span></span> <span data-ttu-id="4b366-130">Показанная здесь схема была выбрана для простоты и простоты использования.</span><span class="sxs-lookup"><span data-stu-id="4b366-130">The design shown here was chosen for simplicity and ease of use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b366-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4b366-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b366-132">**Путеводитель по обложкам**</span><span class="sxs-lookup"><span data-stu-id="4b366-132">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




