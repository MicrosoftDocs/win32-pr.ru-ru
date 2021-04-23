---
title: Интерфейсы раскадровки
description: В этом разделе содержатся справочные спецификации для интерфейсов диспетчера анимации Windows, которые поддерживают раскадровки.
ms.assetid: 372D6348-3DF2-48EB-B495-BAD4E5DAAAD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fba60c480ef4c316731da6eefbe5334616a72b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070192"
---
# <a name="storyboard-interfaces"></a><span data-ttu-id="aa0f9-103">Интерфейсы раскадровки</span><span class="sxs-lookup"><span data-stu-id="aa0f9-103">Storyboard Interfaces</span></span>

<span data-ttu-id="aa0f9-104">В этом разделе содержатся справочные спецификации для интерфейсов диспетчера анимации Windows, которые поддерживают раскадровки.</span><span class="sxs-lookup"><span data-stu-id="aa0f9-104">This section contains the reference specifications for the Windows Animation Manager interfaces that support storyboards.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa0f9-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="aa0f9-105">In this section</span></span>



| <span data-ttu-id="aa0f9-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="aa0f9-106">Topic</span></span>                                                                                                 | <span data-ttu-id="aa0f9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="aa0f9-107">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa0f9-108">**иуианиматионсторибоард**</span><span class="sxs-lookup"><span data-stu-id="aa0f9-108">**IUIAnimationStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)<br/>                                   | <span data-ttu-id="aa0f9-109">Определяет раскадровку, которая содержит группу переходов, синхронизируемых относительно друг друга.</span><span class="sxs-lookup"><span data-stu-id="aa0f9-109">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="aa0f9-110">**IUIAnimationStoryboard2**</span><span class="sxs-lookup"><span data-stu-id="aa0f9-110">**IUIAnimationStoryboard2**</span></span>](/windows/win32/api/uianimation/nn-uianimation-iuianimationstoryboard2)<br/>                                 | <span data-ttu-id="aa0f9-111">Определяет раскадровку, которая содержит группу переходов, синхронизируемых относительно друг друга.</span><span class="sxs-lookup"><span data-stu-id="aa0f9-111">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="aa0f9-112">**иуианиматионсторибоардевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="aa0f9-112">**IUIAnimationStoryboardEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler)<br/>           | <span data-ttu-id="aa0f9-113">Определяет методы обработки событий состояния и обновления для раскадровки.</span><span class="sxs-lookup"><span data-stu-id="aa0f9-113">Defines methods for handling status and update events for a storyboard.</span></span><br/>                                    |
| [<span data-ttu-id="aa0f9-114">**IUIAnimationStoryboardEventHandler2**</span><span class="sxs-lookup"><span data-stu-id="aa0f9-114">**IUIAnimationStoryboardEventHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler2)<br/>         | <span data-ttu-id="aa0f9-115">Определяет методы для обработки событий раскадровки.</span><span class="sxs-lookup"><span data-stu-id="aa0f9-115">Defines methods for handling storyboard events.</span></span> <br/>                                                           |
| [<span data-ttu-id="aa0f9-116">**IUIAnimationLoopIterationChangeHandler2**</span><span class="sxs-lookup"><span data-stu-id="aa0f9-116">**IUIAnimationLoopIterationChangeHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationloopiterationchangehandler2)<br/> | <span data-ttu-id="aa0f9-117">Определяет метод обработки событий итерации цикла раскадровки.</span><span class="sxs-lookup"><span data-stu-id="aa0f9-117">Defines a method for handling storyboard loop iteration events.</span></span><br/>                                            |
| [<span data-ttu-id="aa0f9-118">**иуианиматионприоритикомпарисон**</span><span class="sxs-lookup"><span data-stu-id="aa0f9-118">**IUIAnimationPriorityComparison**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)<br/>                   | <span data-ttu-id="aa0f9-119">Определяет метод для сравнения приоритетов, который диспетчер анимации использует для разрешения конфликтов планирования.</span><span class="sxs-lookup"><span data-stu-id="aa0f9-119">Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.</span></span><br/>  |
| [<span data-ttu-id="aa0f9-120">**IUIAnimationPriorityComparison2**</span><span class="sxs-lookup"><span data-stu-id="aa0f9-120">**IUIAnimationPriorityComparison2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison2)<br/>                 | <span data-ttu-id="aa0f9-121">Определяет метод, который разрешает конфликты планирования с помощью сравнения приоритетов.</span><span class="sxs-lookup"><span data-stu-id="aa0f9-121">Defines a method that resolves scheduling conflicts through priority comparison.</span></span><br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="aa0f9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="aa0f9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa0f9-123">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="aa0f9-123">Interfaces</span></span>](windows-animation-reference.md)
</dt> </dl>

 

