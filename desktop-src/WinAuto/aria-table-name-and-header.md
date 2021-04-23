---
title: Ошибка таблицы данных ARIA
description: Ошибка таблицы данных ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- ариадататаблиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104413973"
---
# <a name="aria-data-table-error"></a><span data-ttu-id="4953a-104">Ошибка таблицы данных ARIA</span><span class="sxs-lookup"><span data-stu-id="4953a-104">ARIA Data Table Error</span></span>

## <a name="text"></a><span data-ttu-id="4953a-105">Текст</span><span class="sxs-lookup"><span data-stu-id="4953a-105">Text</span></span>

<span data-ttu-id="4953a-106">Таблица содержит данные, но не имеет доступной разметки, определенной, несмотря на то, что в **ARIA-Label**, **ARIA-лабелледби**, **Title**, **Caption** или **th** .</span><span class="sxs-lookup"><span data-stu-id="4953a-106">Table contains data but doesn't have accessible markup defined though **aria-label**, **aria-labelledby**, **title**, **caption** or **th** elements.</span></span>

## <a name="type"></a><span data-ttu-id="4953a-107">Тип</span><span class="sxs-lookup"><span data-stu-id="4953a-107">Type</span></span>

<span data-ttu-id="4953a-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="4953a-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="4953a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4953a-109">Description</span></span>

<span data-ttu-id="4953a-110">Эта ошибка применяется к таблицам HTML с более чем одной ячейкой.</span><span class="sxs-lookup"><span data-stu-id="4953a-110">This error applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="4953a-111">Эта ошибка не относится к таблицам, `role="presentation"` поскольку они считаются макетными таблицами.</span><span class="sxs-lookup"><span data-stu-id="4953a-111">This error does not apply to tables with `role="presentation"` because these are considered to be layout tables.</span></span>

<span data-ttu-id="4953a-112">Эта ошибка означает, что таблица данных не содержит доступных сведений о имени или заголовке.</span><span class="sxs-lookup"><span data-stu-id="4953a-112">This error indicates that a data table doesn’t have an accessible name or header information.</span></span>

<span data-ttu-id="4953a-113">Чтобы устранить эту ошибку, определите доступное имя с помощью тега [**заголовка**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) или атрибутов [**ARIA-лабелледби**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**ARIA-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)или [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .</span><span class="sxs-lookup"><span data-stu-id="4953a-113">To fix this error, define an accessible name by using the [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) tag, or the [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span> <span data-ttu-id="4953a-114">Если в таблице отсутствуют сведения о заголовке, используйте теги [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) для пометки ячеек заголовка.</span><span class="sxs-lookup"><span data-stu-id="4953a-114">If the table is missing header information, use [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags to mark header cells.</span></span>

## <a name="example"></a><span data-ttu-id="4953a-115">Пример</span><span class="sxs-lookup"><span data-stu-id="4953a-115">Example</span></span>


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




