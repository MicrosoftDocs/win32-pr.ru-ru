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
# <a name="aria-presentation-table-error"></a>Ошибка таблицы представления ARIA

## <a name="text"></a>Текст

Таблица, используемая для макета, не должна иметь заданные заголовок, доступное имя или сводную информацию (**th**, **Summary**, **ARIA-DescribedBy**, **ARIA-лабелледби**, **ARIA-метка**, **заголовок**, атрибуты **заголовка** ).

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка относится к тегам таблицы HTML, для которых атрибуту [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) присвоено значение Presentation, или таблице с одной ячейкой (1 × 1 таблица).

Эта ошибка означает, что таблица помечена как только макет (имеет `role="presentation"` ), но она также содержит сведения о специальных возможностях, как если бы это была таблица данных, что может быть запутанным для пользователей средства чтения с экрана.

Чтобы устранить эту ошибку, определите, действительно ли таблица является только макетной таблицей, и, если это так, удалите доступную разметку:

-   [**Заголовок**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**ARIA-лабелледби**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**ARIA-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)или [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .
-   [**Сводные данные**](https://www.bing.com/search?q=**summary**) или атрибуты [**ARIA-DescribedBy**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .
-   Теги [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .

## <a name="example"></a>Пример

![HTML для элемента table с такими атрибутами, как Summary, которые активируют ошибку таблицы представления ARIA, показанную в виде HTML-разметки. ](images/aria-layout-table.png)

## <a name="remarks"></a>Комментарии

Если определено, что таблица требует специальных сведений, удалите атрибут [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) или задайте для него значение, отличное от Presentation.

 

 




