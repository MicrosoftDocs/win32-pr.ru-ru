---
title: Ошибка структуры сетки ARIA
description: Ошибка структуры сетки ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- ариагридструктуриррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797095"
---
# <a name="aria-grid-structure-error"></a><span data-ttu-id="8ea97-104">Ошибка структуры сетки ARIA</span><span class="sxs-lookup"><span data-stu-id="8ea97-104">ARIA Grid Structure Error</span></span>

## <a name="text"></a><span data-ttu-id="8ea97-105">Текст</span><span class="sxs-lookup"><span data-stu-id="8ea97-105">Text</span></span>

<span data-ttu-id="8ea97-106">Элемент с ролью **сетки** не имеет соответствующей структуры сетки или доступной разметки.</span><span class="sxs-lookup"><span data-stu-id="8ea97-106">Element with the **grid** role doesn't have a corresponding grid structure or accessible markup.</span></span>

## <a name="type"></a><span data-ttu-id="8ea97-107">Тип</span><span class="sxs-lookup"><span data-stu-id="8ea97-107">Type</span></span>

<span data-ttu-id="8ea97-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="8ea97-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="8ea97-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8ea97-109">Description</span></span>

<span data-ttu-id="8ea97-110">Эта ошибка применяется к пользовательским элементам, для которых атрибут **Role** имеет значение Grid.</span><span class="sxs-lookup"><span data-stu-id="8ea97-110">This error applies to custom elements that have the **role** attribute set to "grid".</span></span> <span data-ttu-id="8ea97-111">Он не применяется к тегам таблицы HTML, которые имеют неявную **роль** "Grid".</span><span class="sxs-lookup"><span data-stu-id="8ea97-111">It does not apply to HTML table tags that have an implicit **role** of "grid".</span></span>

<span data-ttu-id="8ea97-112">У элемента, у которого атрибут **Role** имеет значение "Grid", должна быть структура, определенная ролью сетки "веб-приложения специальных возможностей" (ожидать-ARIA), включая доступное имя для сетки и вложенные элементы заголовка.</span><span class="sxs-lookup"><span data-stu-id="8ea97-112">An element that has its **role** attribute set to "grid" must have the structure defined by the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) grid role, including the accessible name for the grid and its header subelements.</span></span>

<span data-ttu-id="8ea97-113">Чтобы устранить эту ошибку, проверьте реализацию, чтобы убедиться, что она соответствует спецификации ожидать-ARIA.</span><span class="sxs-lookup"><span data-stu-id="8ea97-113">To fix this error, review your implementation to ensure that it complies with the WAI-ARIA specification.</span></span> <span data-ttu-id="8ea97-114">В частности, убедитесь, что структура соответствует следующим правилам.</span><span class="sxs-lookup"><span data-stu-id="8ea97-114">Specifically, ensure that the structure meets the following rules.</span></span>

-   <span data-ttu-id="8ea97-115">**Сетка** содержит элементы **Row** или **группы строк** .</span><span class="sxs-lookup"><span data-stu-id="8ea97-115">**grid** contains **row** or **rowgroup** elements.</span></span>
-   <span data-ttu-id="8ea97-116">**группы строк** содержит элементы **Row** .</span><span class="sxs-lookup"><span data-stu-id="8ea97-116">**rowgroup** contains **row** elements.</span></span>
-   <span data-ttu-id="8ea97-117">элементы **Row** содержат элементы **колумнхеадер** или **гридцелл** или **ровхеадер** .</span><span class="sxs-lookup"><span data-stu-id="8ea97-117">**row** elements contain **columnheader** or **gridcell** or **rowheader** elements.</span></span>

<span data-ttu-id="8ea97-118">Доступное имя должно быть определено для элементов **Grid**, **колумнхеадер**, **гридцелл** и **ровхеадер** с помощью одного из следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8ea97-118">An accessible name should be defined for **grid**, **columnheader**, **gridcell** and **rowheader** elements by using one of the following attributes.</span></span>

-   <span data-ttu-id="8ea97-119">атрибут [**ARIA-лабелледби**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) для ссылки на элемент, содержащий текст.</span><span class="sxs-lookup"><span data-stu-id="8ea97-119">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute for referencing the element containing text.</span></span>
-   <span data-ttu-id="8ea97-120">атрибут [**ARIA-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) для непосредственного задания имени для доступа.</span><span class="sxs-lookup"><span data-stu-id="8ea97-120">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to set the accessible name directly.</span></span>
-   <span data-ttu-id="8ea97-121">[**заголовок**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) для создания подсказки, которая в то же время используется в качестве имени.</span><span class="sxs-lookup"><span data-stu-id="8ea97-121">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) for creating a tooltip which is at the same time used as a name.</span></span>

 

 




