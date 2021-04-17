---
title: Задачи анимации Windows
description: Разделы, содержащиеся в этом разделе, описывают основные задачи, необходимые для приложений, использующих Windows Animation Manager.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Анимация Windows анимация Windows, задачи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691342"
---
# <a name="windows-animation-tasks"></a><span data-ttu-id="e662e-104">Задачи анимации Windows</span><span class="sxs-lookup"><span data-stu-id="e662e-104">Windows Animation Tasks</span></span>

<span data-ttu-id="e662e-105">Разделы, содержащиеся в этом разделе, описывают основные задачи, необходимые для приложений, использующих Windows Animation Manager.</span><span class="sxs-lookup"><span data-stu-id="e662e-105">The topics contained in this section describe the basic tasks required of applications that use Windows Animation Manager.</span></span>

<span data-ttu-id="e662e-106">Эти задачи по порядку включают:</span><span class="sxs-lookup"><span data-stu-id="e662e-106">These tasks, in order, include:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e662e-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="e662e-107">In this section</span></span>



| <span data-ttu-id="e662e-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="e662e-108">Topic</span></span>                                                                                                | <span data-ttu-id="e662e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e662e-109">Description</span></span>                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e662e-110">Создание основных объектов анимации</span><span class="sxs-lookup"><span data-stu-id="e662e-110">Create the Main Animation Objects</span></span>](adding-animation-to-an-application.md)<br/>               | <span data-ttu-id="e662e-111">Чтобы использовать анимацию Windows в приложении, первым шагом является создание небольшого набора основных объектов анимации.</span><span class="sxs-lookup"><span data-stu-id="e662e-111">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="e662e-112">Создание переменных анимации</span><span class="sxs-lookup"><span data-stu-id="e662e-112">Create Animation Variables</span></span>](create-animation-variables.md)<br/>                              | <span data-ttu-id="e662e-113">Приложение должно создать переменную анимации для каждой визуальной характеристики, которая должна быть анимирована с помощью анимации Windows.</span><span class="sxs-lookup"><span data-stu-id="e662e-113">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="e662e-114">Обновление диспетчера анимации и рисование кадров</span><span class="sxs-lookup"><span data-stu-id="e662e-114">Update the Animation Manager and Draw Frames</span></span>](introducing-windows-animation-manager.md)<br/> | <span data-ttu-id="e662e-115">Каждый раз, когда приложение планирует раскадровку, приложение должно передать текущее время в диспетчер анимации.</span><span class="sxs-lookup"><span data-stu-id="e662e-115">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="e662e-116">Текущее время также требуется, если диспетчеру анимации нужно обновить свое состояние и задать для всех переменных анимации соответствующие значения интерполяции.</span><span class="sxs-lookup"><span data-stu-id="e662e-116">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span><br/> |
| [<span data-ttu-id="e662e-117">Чтение значений переменных анимации</span><span class="sxs-lookup"><span data-stu-id="e662e-117">Read the Animation Variable Values</span></span>](updating---application-driven-animation.md)<br/>         | <span data-ttu-id="e662e-118">Каждый раз, когда приложение рисуется, оно должно считывать текущие значения переменных анимации, представляющих визуальные характеристики для анимации.</span><span class="sxs-lookup"><span data-stu-id="e662e-118">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="e662e-119">Создание раскадровки и добавление переходов</span><span class="sxs-lookup"><span data-stu-id="e662e-119">Create a Storyboard and Add Transitions</span></span>](updating---timer-driven-animation.md)<br/>          | <span data-ttu-id="e662e-120">Чтобы создать анимацию, приложение должно создать раскадровку.</span><span class="sxs-lookup"><span data-stu-id="e662e-120">To create an animation, an application must construct a storyboard.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="e662e-121">Планирование раскадровки</span><span class="sxs-lookup"><span data-stu-id="e662e-121">Schedule a Storyboard</span></span>](scheduling-a-storyboard.md)<br/>                                      | <span data-ttu-id="e662e-122">После создания раскадровки она планируется диспетчером анимации.</span><span class="sxs-lookup"><span data-stu-id="e662e-122">After a storyboard is created, it is scheduled by the animation manager.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="e662e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e662e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e662e-124">Общие сведения о анимации Windows</span><span class="sxs-lookup"><span data-stu-id="e662e-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="e662e-125">Справочник по анимации Windows</span><span class="sxs-lookup"><span data-stu-id="e662e-125">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> <dt>

[<span data-ttu-id="e662e-126">Примеры анимации Windows</span><span class="sxs-lookup"><span data-stu-id="e662e-126">Windows Animation Samples</span></span>](windows-animation-samples.md)
</dt> </dl>

 

 





