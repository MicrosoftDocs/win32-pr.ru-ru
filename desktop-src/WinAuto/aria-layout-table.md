---
title: Ошибка таблицы представления ARIA
description: Ошибка таблицы представления ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- ариалайауттаблиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797089"
---
# <a name="aria-presentation-table-error"></a><span data-ttu-id="01b44-104">Ошибка таблицы представления ARIA</span><span class="sxs-lookup"><span data-stu-id="01b44-104">ARIA Presentation Table Error</span></span>

## <a name="text"></a><span data-ttu-id="01b44-105">Текст</span><span class="sxs-lookup"><span data-stu-id="01b44-105">Text</span></span>

<span data-ttu-id="01b44-106">Таблица, используемая для макета, не должна иметь заданные заголовок, доступное имя или сводную информацию (**th**, **Summary**, **ARIA-DescribedBy**, **ARIA-лабелледби**, **ARIA-метка**, **заголовок**, атрибуты **заголовка** ).</span><span class="sxs-lookup"><span data-stu-id="01b44-106">Table used for layout must not have header, accessible name or summary information defined (**th**, **summary**, **aria-describedby**, **aria-labelledby**, **aria-label**, **title**, **caption** attributes).</span></span>

## <a name="type"></a><span data-ttu-id="01b44-107">Тип</span><span class="sxs-lookup"><span data-stu-id="01b44-107">Type</span></span>

<span data-ttu-id="01b44-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="01b44-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="01b44-109">Описание</span><span class="sxs-lookup"><span data-stu-id="01b44-109">Description</span></span>

<span data-ttu-id="01b44-110">Эта ошибка относится к тегам таблицы HTML, для которых атрибуту [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) присвоено значение Presentation, или таблице с одной ячейкой (1 × 1 таблица).</span><span class="sxs-lookup"><span data-stu-id="01b44-110">This error applies to HTML table tags that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set to "presentation", or with a table that has a single cell (1×1 table).</span></span>

<span data-ttu-id="01b44-111">Эта ошибка означает, что таблица помечена как только макет (имеет `role="presentation"` ), но она также содержит сведения о специальных возможностях, как если бы это была таблица данных, что может быть запутанным для пользователей средства чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="01b44-111">This error indicates that a table is marked as layout only (has `role="presentation"`), but it also contains accessibility information as if it was a data table, which can be confusing for screen reader users.</span></span>

<span data-ttu-id="01b44-112">Чтобы устранить эту ошибку, определите, действительно ли таблица является только макетной таблицей, и, если это так, удалите доступную разметку:</span><span class="sxs-lookup"><span data-stu-id="01b44-112">To address this error, determine whether the table actually is just a layout table and, if so, remove the accessible markup:</span></span>

-   <span data-ttu-id="01b44-113">[**Заголовок**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**ARIA-лабелледби**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**ARIA-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)или [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .</span><span class="sxs-lookup"><span data-stu-id="01b44-113">[**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span>
-   <span data-ttu-id="01b44-114">[**Сводные данные**](https://www.bing.com/search?q=**summary**) или атрибуты [**ARIA-DescribedBy**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="01b44-114">[**summary**](https://www.bing.com/search?q=**summary**) or [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>
-   <span data-ttu-id="01b44-115">Теги [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .</span><span class="sxs-lookup"><span data-stu-id="01b44-115">[**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags.</span></span>

## <a name="example"></a><span data-ttu-id="01b44-116">Пример</span><span class="sxs-lookup"><span data-stu-id="01b44-116">Example</span></span>

![<span data-ttu-id="01b44-117">HTML для элемента table с такими атрибутами, как Summary, которые активируют ошибку таблицы представления ARIA, показанную в виде HTML-разметки.</span><span class="sxs-lookup"><span data-stu-id="01b44-117">html for a table element, with attributes such as summary that trigger the aria presentation table error shown as struck-out html markup</span></span> ](images/aria-layout-table.png)

## <a name="remarks"></a><span data-ttu-id="01b44-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01b44-118">Remarks</span></span>

<span data-ttu-id="01b44-119">Если определено, что таблица требует специальных сведений, удалите атрибут [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) или задайте для него значение, отличное от Presentation.</span><span class="sxs-lookup"><span data-stu-id="01b44-119">If you determine that a table does need accessibility information, remove the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute or set it to a value other than "presentation".</span></span>

 

 




