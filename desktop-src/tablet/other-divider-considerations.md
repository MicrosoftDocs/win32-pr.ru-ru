---
description: При принятии решения о том, когда и как использовать объект разделителя в приложении, учитывайте следующее.
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Другие аспекты использования разделителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265453"
---
# <a name="other-divider-considerations"></a><span data-ttu-id="2e227-103">Другие аспекты использования разделителя</span><span class="sxs-lookup"><span data-stu-id="2e227-103">Other Divider Considerations</span></span>

<span data-ttu-id="2e227-104">При принятии решения о том, когда и как использовать объект [**разделителя**](inkdivider-class.md) в приложении, учитывайте следующее.</span><span class="sxs-lookup"><span data-stu-id="2e227-104">Consider the following when deciding when and how to use the [**Divider**](inkdivider-class.md) object in an application:</span></span>

-   <span data-ttu-id="2e227-105">Объект- [**Разделитель**](inkdivider-class.md) предназначен для разделения рисунков и блоков рукописного текста, но не для распознавания более высоких уровней структуры, таких как таблицы или столбцы.</span><span class="sxs-lookup"><span data-stu-id="2e227-105">The [**Divider**](inkdivider-class.md) object is designed to separate drawings and blocks of handwriting, but not to recognize higher levels of structure, such as tables or columns.</span></span>
-   <span data-ttu-id="2e227-106">Объект [**разделителя**](inkdivider-class.md) не предоставляет интерфейсы, специально предназначенные для исправления результатов анализа макета.</span><span class="sxs-lookup"><span data-stu-id="2e227-106">The [**Divider**](inkdivider-class.md) object does not provide interfaces specifically for correction of results of layout analysis.</span></span>
-   <span data-ttu-id="2e227-107">Использование времени ожидания и числа эвристических методов Stroke для добавления или удаления нескольких штрихов за раз из штрихов объекта- [**разделителя**](inkdivider-class.md) может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="2e227-107">The use of timeout and number of stroke heuristics to add or remove multiple strokes at a time from the strokes in the [**Divider**](inkdivider-class.md) object may improve performance.</span></span>

## <a name="reanalysis-considerations"></a><span data-ttu-id="2e227-108">Рекомендации по переанализу</span><span class="sxs-lookup"><span data-stu-id="2e227-108">Reanalysis Considerations</span></span>

<span data-ttu-id="2e227-109">Если вы планируете использовать объект [**разделителя**](inkdivider-class.md) в приложении, где объект **разделителя** может потребоваться для повторного анализа больших объемов рукописного ввода, учитывайте следующее.</span><span class="sxs-lookup"><span data-stu-id="2e227-109">If you are considering using the [**Divider**](inkdivider-class.md) object in an application where the **Divider** object may have to reanalyze large amounts of ink, keep the following in mind.</span></span>

### <a name="retaining-copies-of-ink-and-strokes"></a><span data-ttu-id="2e227-110">Сохраняемые копии рукописного ввода и штрихов</span><span class="sxs-lookup"><span data-stu-id="2e227-110">Retaining Copies of Ink and Strokes</span></span>

<span data-ttu-id="2e227-111">Приложение может хранить копии объектов [**рукописного ввода**](inkdisp-class.md) и [**дивисионресулт**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) для элементов приложения, которые могут быть просмотрены позже в сеансе приложения.</span><span class="sxs-lookup"><span data-stu-id="2e227-111">An application can keep copies of [**Ink**](inkdisp-class.md) and [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) objects for application elements that may be revisited later in the application session.</span></span> <span data-ttu-id="2e227-112">Это устраняет необходимость в повторном анализе объекта **Ink** , если пользователь возвращается к элементу.</span><span class="sxs-lookup"><span data-stu-id="2e227-112">This eliminates the need to reanalyze the **Ink** object if the user returns to the element.</span></span> <span data-ttu-id="2e227-113">Этот подход приводит к повышению производительности памяти.</span><span class="sxs-lookup"><span data-stu-id="2e227-113">This approach trades off memory for better performance.</span></span>

### <a name="data-reduction-heuristics"></a><span data-ttu-id="2e227-114">Эвристика сокращения объема данных</span><span class="sxs-lookup"><span data-stu-id="2e227-114">Data Reduction Heuristics</span></span>

<span data-ttu-id="2e227-115">Вы можете записать результаты анализа в виде данных приложения и реализовать эвристику, чтобы определить, когда следует повторно анализировать набор штрихов.</span><span class="sxs-lookup"><span data-stu-id="2e227-115">You may be able to record the analysis results as application data, and implement heuristics to determine when to reanalyze a set of strokes.</span></span> <span data-ttu-id="2e227-116">Это позволит снизить необходимость повторного анализа всех рукописных данных в приложении между сеансами приложения.</span><span class="sxs-lookup"><span data-stu-id="2e227-116">This practice would reduce the need to reanalyze all the ink in the application between application sessions.</span></span> <span data-ttu-id="2e227-117">Однако необходимо соблюдать осторожность, чтобы сохранить границы структурных элементов или повторно проанализировать все штрихи для затронутых элементов.</span><span class="sxs-lookup"><span data-stu-id="2e227-117">However, care must be taken to preserve structural element boundaries or to reanalyze all the strokes for affected elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e227-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2e227-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e227-119">**Класс Инкдивидер**</span><span class="sxs-lookup"><span data-stu-id="2e227-119">**InkDivider Class**</span></span>](inkdivider-class.md)
</dt> <dt>

<span data-ttu-id="2e227-120">[Класс Microsoft. Ink. делитель](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="2e227-120">[Microsoft.Ink.Divider Class](/previous-versions/ms583616(v=vs.100))</span></span>
</dt> </dl>

 

 
