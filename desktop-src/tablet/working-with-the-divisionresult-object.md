---
description: Объект Дивисионресулт представляет собой моментальный снимок анализа макета для штрихов, содержащихся в объекте-разделителе. Он содержит классификацию штрихов и сведения о группировании из анализа макета.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Работа с объектом Дивисионресулт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542543"
---
# <a name="working-with-the-divisionresult-object"></a><span data-ttu-id="4832c-104">Работа с объектом Дивисионресулт</span><span class="sxs-lookup"><span data-stu-id="4832c-104">Working with the DivisionResult Object</span></span>

<span data-ttu-id="4832c-105">Объект **дивисионресулт** представляет собой моментальный снимок анализа макета для штрихов, содержащихся в объекте- **разделителе** .</span><span class="sxs-lookup"><span data-stu-id="4832c-105">The **DivisionResult** object represents a snapshot of the layout analysis of the strokes contained by the **Divider** object.</span></span> <span data-ttu-id="4832c-106">Он содержит классификацию штрихов и сведения о группировании из анализа макета.</span><span class="sxs-lookup"><span data-stu-id="4832c-106">It contains the stroke classification and grouping information from the layout analysis.</span></span>

<span data-ttu-id="4832c-107">Сведения из объекта **дивисионресулт** можно получить по типу структурного элемента, например по рисованию или линиям рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="4832c-107">You can get information from the **DivisionResult** object by structural element type, such as drawing or lines of handwriting.</span></span> <span data-ttu-id="4832c-108">Объект **дивисионресулт** может сохраняться после уничтожения объекта- **разделителя** .</span><span class="sxs-lookup"><span data-stu-id="4832c-108">The **DivisionResult** object can persist after the **Divider** object is destroyed.</span></span> <span data-ttu-id="4832c-109">В службе автоматизации этот объект называется объектом [**интерфейса иинкдивисионресулт**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="4832c-109">In Automation, this object is called the [**IInkDivisionResult Interface**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="4832c-110">Свойство [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) объекта **дивисионресулт** содержит копию коллекции **штрихов** в объекте- **разделителе** на момент создания объекта **дивисионресулт** .</span><span class="sxs-lookup"><span data-stu-id="4832c-110">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the **DivisionResult** object contains a copy of the **Strokes** collection in the **Divider** object at the time the **DivisionResult** object was created.</span></span>

<span data-ttu-id="4832c-111">Перечисление [**инкдивисионтипе**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) определяет типы структурных элементов, распознаваемые анализом макета.</span><span class="sxs-lookup"><span data-stu-id="4832c-111">The [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration defines the structural element types that the layout analysis recognizes.</span></span>

<span data-ttu-id="4832c-112">Метод [**ресултбитипе**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) объекта **Дивисионресулт** Возвращает коллекцию **дивисионунитс** , содержащую все структурные элементы данного типа.</span><span class="sxs-lookup"><span data-stu-id="4832c-112">The [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method of the **DivisionResult** object returns a **DivisionUnits** collection that contains all structural elements of a given type.</span></span> <span data-ttu-id="4832c-113">Отдельный структурный элемент представлен объектом **дивисионунит** .</span><span class="sxs-lookup"><span data-stu-id="4832c-113">An individual structural element is represented by a **DivisionUnit** object.</span></span> <span data-ttu-id="4832c-114">Каждый раз при вызове метода **ресултбитипе** объект **Дивисионресулт** создает коллекцию **дивисионунитс** .</span><span class="sxs-lookup"><span data-stu-id="4832c-114">Each time you call the **ResultByType** method, the **DivisionResult** object creates a **DivisionUnits** collection.</span></span> <span data-ttu-id="4832c-115">Дополнительные сведения об объекте **дивисионунит** см. в разделе [Работа с объектом дивисионунит](working-with-the-divisionunit-object.md).</span><span class="sxs-lookup"><span data-stu-id="4832c-115">For more information about the **DivisionUnit** object, see [Working with the DivisionUnit Object](working-with-the-divisionunit-object.md).</span></span>

 

 
