---
title: Манипуляции
description: В этом разделе описывается манипуляция объектами для Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Касание Windows, манипуляции
- манипуляции, о
- манипуляции, различия жестов
- жесты, различия в манипуляциях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328616"
---
# <a name="manipulations"></a><span data-ttu-id="9a965-107">Манипуляции</span><span class="sxs-lookup"><span data-stu-id="9a965-107">Manipulations</span></span>

<span data-ttu-id="9a965-108">В этом разделе описывается манипуляция объектами для Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="9a965-108">This section explains object manipulation for Windows Touch.</span></span>

## <a name="manipulation-overview"></a><span data-ttu-id="9a965-109">Общие сведения об управлении</span><span class="sxs-lookup"><span data-stu-id="9a965-109">Manipulation Overview</span></span>

<span data-ttu-id="9a965-110">Удобный способ подумать об манипуляциях заключается в том, чтобы рассматривать их как надмножество жестов.</span><span class="sxs-lookup"><span data-stu-id="9a965-110">A convenient way to think about manipulations is to consider them a superset of gestures.</span></span> <span data-ttu-id="9a965-111">Действия, выполняемые с помощью жестов, позволяют повысить гибкость и точность при помощи манипуляций.</span><span class="sxs-lookup"><span data-stu-id="9a965-111">What you can do with gestures, you can do with more flexibility and with finer precision by using manipulations.</span></span> <span data-ttu-id="9a965-112">Разница между манипуляциями и жестами лучше продемонстрировать с помощью простого примера.</span><span class="sxs-lookup"><span data-stu-id="9a965-112">The difference between manipulations and gestures is best demonstrated with a simple example.</span></span> <span data-ttu-id="9a965-113">Вы можете расширить объект и в то же время преобразовать его с помощью манипуляций; с помощью жестов можно выполнять только один за раз.</span><span class="sxs-lookup"><span data-stu-id="9a965-113">You can expand an object and at the same time translate it using manipulations; with gestures, you can do only one at a time.</span></span> <span data-ttu-id="9a965-114">Эта возможность манипулировать объектом в режиме реального времени делает приложения более понятными для пользователей, обеспечивая более реалистичную работу.</span><span class="sxs-lookup"><span data-stu-id="9a965-114">This ability to manipulate an object in real time makes applications more intuitive to users by enabling a more realistic experience.</span></span>

<span data-ttu-id="9a965-115">API манипуляции используются для упрощения операций преобразования объектов для приложений с поддержкой сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="9a965-115">The Manipulation APIs are used to simplify transformation operations on objects for touch-enabled applications.</span></span> <span data-ttu-id="9a965-116">Манипуляции выполняются в Windows 7 с помощью COM-объекта манипуляций.</span><span class="sxs-lookup"><span data-stu-id="9a965-116">Manipulations are performed in Windows 7 through the manipulations COM object.</span></span> <span data-ttu-id="9a965-117">С помощью манипуляций разработчики могут более легко поддерживать инерцию (объект физика) и легко выполнять преобразования объектов способом, согласованным с другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="9a965-117">By using manipulations, developers can more easily support inertia (object physics) and can easily perform transformations on objects in a way that is consistent with other applications.</span></span> <span data-ttu-id="9a965-118">В следующих разделах описаны различные способы выполнения манипуляций.</span><span class="sxs-lookup"><span data-stu-id="9a965-118">The following sections explain various ways that you can perform manipulations.</span></span>



| <span data-ttu-id="9a965-119">Section</span><span class="sxs-lookup"><span data-stu-id="9a965-119">Section</span></span>                                                                                            | <span data-ttu-id="9a965-120">Описание</span><span class="sxs-lookup"><span data-stu-id="9a965-120">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a965-121">Добавление поддержки манипуляций в неуправляемый код</span><span class="sxs-lookup"><span data-stu-id="9a965-121">Adding Manipulation Support to Unmanaged Code</span></span>](adding-manipulation-support-in-unmanaged-code.md) | <span data-ttu-id="9a965-122">Объясняет, как реализовать приемник событий для интерфейса [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) и добавить в код обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="9a965-122">Explains how to implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface and add event handlers to your code.</span></span> |
| [<span data-ttu-id="9a965-123">Расширенные манипуляции</span><span class="sxs-lookup"><span data-stu-id="9a965-123">Advanced Manipulations</span></span>](advanced-manipulations.md)                                               | <span data-ttu-id="9a965-124">Объясняет, как выполнять сложные манипуляции.</span><span class="sxs-lookup"><span data-stu-id="9a965-124">Explains how to perform complex manipulations.</span></span>                                                                                                       |
| [<span data-ttu-id="9a965-125">Поворот одного пальца</span><span class="sxs-lookup"><span data-stu-id="9a965-125">Single Finger Rotation</span></span>](single-finger-rotation.md)                                               | <span data-ttu-id="9a965-126">Объясняет, как вращать объект с помощью точки вращения и обработчика манипуляций.</span><span class="sxs-lookup"><span data-stu-id="9a965-126">Explains how to rotate an object by using a pivot point and the manipulation processor.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="9a965-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9a965-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a965-128">Манипуляции и инерция</span><span class="sxs-lookup"><span data-stu-id="9a965-128">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




