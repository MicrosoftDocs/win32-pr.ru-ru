---
description: В дополнение к распознаванию текста распознаватели могут распознать класс связанных объектов.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Распознаватели объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999047"
---
# <a name="object-recognizers"></a><span data-ttu-id="90c18-103">Распознаватели объектов</span><span class="sxs-lookup"><span data-stu-id="90c18-103">Object Recognizers</span></span>

<span data-ttu-id="90c18-104">В дополнение к распознаванию текста распознаватели могут распознать класс связанных объектов.</span><span class="sxs-lookup"><span data-stu-id="90c18-104">In addition to recognizing text, recognizers can recognize a class of related objects.</span></span> <span data-ttu-id="90c18-105">Распознаватели объектов распознают общие фигуры в соответствии с их целями.</span><span class="sxs-lookup"><span data-stu-id="90c18-105">Object recognizers recognize general shapes, according to their purpose.</span></span> <span data-ttu-id="90c18-106">Распознаватели объектов используются для распознавания:</span><span class="sxs-lookup"><span data-stu-id="90c18-106">Object recognizers are used to recognize:</span></span>

-   <span data-ttu-id="90c18-107">Музыкальные заметки</span><span class="sxs-lookup"><span data-stu-id="90c18-107">Musical notes</span></span>
-   <span data-ttu-id="90c18-108">Геометрические фигуры</span><span class="sxs-lookup"><span data-stu-id="90c18-108">Geometric shapes</span></span>
-   <span data-ttu-id="90c18-109">Математические уравнения</span><span class="sxs-lookup"><span data-stu-id="90c18-109">Math equations</span></span>
-   <span data-ttu-id="90c18-110">Элементы блоковой диаграммы</span><span class="sxs-lookup"><span data-stu-id="90c18-110">Flow chart elements</span></span>

<span data-ttu-id="90c18-111">Как правило, объекты, распознаваемые таким распознавателем, находятся в двумерной пространственной или функциональной связи друг с другом.</span><span class="sxs-lookup"><span data-stu-id="90c18-111">Usually, the objects that are recognized by such a recognizer are in a two-dimensional spatial or functional relationship with each other.</span></span> <span data-ttu-id="90c18-112">Например, в сложных отношениях в математическом уравнении распознаватель может возвращать разные результаты для верхнего предела определенного целого числа, а не числителя в дробной части.</span><span class="sxs-lookup"><span data-stu-id="90c18-112">For example, within the complex relationships in a math equation, a recognizer can return different results for an upper limit on a definite integral as opposed to a numerator in a fraction.</span></span>

<span data-ttu-id="90c18-113">Из-за общего характера этих связей чрезвычайно сложно определить набор интерфейсов, которые будут работать для каждого распознавателя объектов.</span><span class="sxs-lookup"><span data-stu-id="90c18-113">Because of the very general nature of these relationships, it is extremely difficult to define the set of interfaces that will work for every object recognizer.</span></span>

<span data-ttu-id="90c18-114">Технология планшетных ПК предоставляет базовую платформу для распознавателей объектов в управляемых библиотеках и интерфейсах автоматизации.</span><span class="sxs-lookup"><span data-stu-id="90c18-114">The Tablet PC Technology provides a basic framework for object recognizers in the Managed Library and Automation interfaces.</span></span> <span data-ttu-id="90c18-115">Однако необходимо разработать пользовательские интерфейсы, описывающие сложные пространственные связи между распознаваемыми объектами для каждого распознавателя объектов.</span><span class="sxs-lookup"><span data-stu-id="90c18-115">However, you must develop custom interfaces that describe complex spatial relationships between recognized objects for each object recognizer.</span></span> <span data-ttu-id="90c18-116">В частности, для распознавателей объектов платформа предоставляет базовый объект [**рекогнизерконтекст**](inkrecognizercontext-class.md) для связывания объекта [**рукописного ввода**](inkdisp-class.md) с контекстом распознавателя и для вызова распознавателя для выполнения распознавания.</span><span class="sxs-lookup"><span data-stu-id="90c18-116">Specifically, for object recognizers, the platform provides the basic [**RecognizerContext**](inkrecognizercontext-class.md) object for associating the [**Ink**](inkdisp-class.md) object with the recognizer context and for calling the recognizer to perform the recognition.</span></span>

 

 



