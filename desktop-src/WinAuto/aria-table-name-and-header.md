---
title: Ошибка таблицы данных ARIA
description: Ошибка таблицы данных ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- ариадататаблиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 025443ab452ff0103c8808c27dce834a03cb8c96e0d9106a7abb4409b64a0697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133977"
---
# <a name="aria-data-table-error"></a>Ошибка таблицы данных ARIA

## <a name="text"></a>Текст

Таблица содержит данные, но не имеет доступной разметки, определенной, несмотря на то, что в **ARIA-Label**, **ARIA-лабелледби**, **Title**, **Caption** или **th** .

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Эта ошибка применяется к таблицам HTML с более чем одной ячейкой. Эта ошибка не относится к таблицам, `role="presentation"` поскольку они считаются макетными таблицами.

Эта ошибка означает, что таблица данных не содержит доступных сведений о имени или заголовке.

Чтобы устранить эту ошибку, определите доступное имя с помощью тега [**заголовка**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) или атрибутов [**ARIA-лабелледби**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**ARIA-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)или [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) . Если в таблице отсутствуют сведения о заголовке, используйте теги [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) для пометки ячеек заголовка.

## <a name="example"></a>Пример


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



 

 




