---
description: Анализ макета работает с коллекцией штрихов и классифицирует штрихи на рукописные и графические элементы. Объект разделителя предоставляет доступ к функциям анализа макета планшетных ПК.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Анализ макета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719546"
---
# <a name="layout-analysis"></a><span data-ttu-id="7b2c8-104">Анализ макета</span><span class="sxs-lookup"><span data-stu-id="7b2c8-104">Layout Analysis</span></span>

<span data-ttu-id="7b2c8-105">Анализ макета работает с коллекцией [**штрихов**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) и классифицирует штрихи на рукописные и графические элементы.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-105">Layout analysis operates on a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and classifies the strokes into handwriting and drawing elements.</span></span> <span data-ttu-id="7b2c8-106">Объект [**разделителя**](inkdivider-class.md) предоставляет доступ к функциям анализа макета планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-106">The [**Divider**](inkdivider-class.md) object provides access to the Tablet PC layout analysis features.</span></span>

<span data-ttu-id="7b2c8-107">В следующей таблице описаны типы структурных элементов перечисления [**инкдивисионтипе**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) , в которых объект- [**Разделитель**](inkdivider-class.md) классифицирует штрихи.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-107">The following table describes the structural element types of the [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration into which the [**Divider**](inkdivider-class.md) object classifies strokes.</span></span>



| <span data-ttu-id="7b2c8-108">Тип</span><span class="sxs-lookup"><span data-stu-id="7b2c8-108">Type</span></span>          | <span data-ttu-id="7b2c8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7b2c8-109">Description</span></span>                                                                      |
|---------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7b2c8-110">**Segment**</span><span class="sxs-lookup"><span data-stu-id="7b2c8-110">**Segment**</span></span>   | <span data-ttu-id="7b2c8-111">Сегмент распознавания.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-111">A recognition segment.</span></span><br/>                                                |
| <span data-ttu-id="7b2c8-112">**Line**</span><span class="sxs-lookup"><span data-stu-id="7b2c8-112">**Line**</span></span>      | <span data-ttu-id="7b2c8-113">Строка рукописного ввода, содержащая один или несколько сегментов распознавания.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-113">A line of handwriting that contains one or more recognition segments.</span></span><br/> |
| <span data-ttu-id="7b2c8-114">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="7b2c8-114">**Paragraph**</span></span> | <span data-ttu-id="7b2c8-115">Блок штрихов, содержащий одну или несколько строк рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-115">A block of strokes that contains one or more lines of handwriting.</span></span><br/>    |
| <span data-ttu-id="7b2c8-116">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="7b2c8-116">**Drawing**</span></span>   | <span data-ttu-id="7b2c8-117">Рукописный ввод, не являющийся почерком.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-117">Ink that is not handwriting.</span></span><br/>                                          |



 

<span data-ttu-id="7b2c8-118">Объект- [**Разделитель**](inkdivider-class.md) содержит коллекцию [**штрихов**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , в которой объект- **Разделитель** динамически анализирует каждый раз при добавлении или удалении из коллекции.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-118">The [**Divider**](inkdivider-class.md) object has a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection, which the **Divider** object dynamically analyzes each time you add to or delete from the collection.</span></span> <span data-ttu-id="7b2c8-119">Объект- **Разделитель** не является сериализуемым, и его состояние анализа невозможно сохранить.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-119">The **Divider** object is not serializable, and you cannot save its analysis state.</span></span> <span data-ttu-id="7b2c8-120">Таким образом, объект- **Разделитель** предназначен для приложений, которые должны различать смешанные рукописные и графические входные данные, но не требуют повторного анализа больших объемов рукописного ввода между сеансами.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-120">Thus the **Divider** object is designed for applications that must differentiate between mixed handwriting and drawing input, but do not need to reanalyze large amounts of ink between sessions.</span></span>

<span data-ttu-id="7b2c8-121">Можно получить статический моментальный снимок текущего результата анализа, который возвращается в объекте [**дивисионресулт**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="7b2c8-121">You can obtain a static snapshot of the current analysis result, which is returned in a [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span> <span data-ttu-id="7b2c8-122">Можно получить объекты [**дивисионунит**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , каждый из которых представляет один структурный элемент объекта **дивисионресулт** .</span><span class="sxs-lookup"><span data-stu-id="7b2c8-122">You can obtain [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) objects, each which represents a single structural element of a **DivisionResult** object.</span></span> <span data-ttu-id="7b2c8-123">Объекты **дивисионресулт** и **дивисионунит** не поддерживают сериализацию.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-123">The **DivisionResult** and **DivisionUnit** objects are not serializable.</span></span> <span data-ttu-id="7b2c8-124">Однако доступны сведения о состоянии этих объектов.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-124">However, state information from these objects is available.</span></span>

<span data-ttu-id="7b2c8-125">Объект- [**Разделитель**](inkdivider-class.md) работает только с рукописным письмом слева направо.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-125">The [**Divider**](inkdivider-class.md) object works only with left-to-right handwriting.</span></span> <span data-ttu-id="7b2c8-126">Чтобы объект- **Разделитель** выполнял анализ вертикальных языков, таких как китайский, символы должны быть выведены слева направо, а не сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="7b2c8-126">For the **Divider** object to analyze vertical languages such as Chinese correctly, the characters must be drawn left-to-right instead of top-to-bottom.</span></span>

 

