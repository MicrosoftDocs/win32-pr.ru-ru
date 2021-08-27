---
title: Предупреждение таблицы данных ARIA
description: Предупреждение таблицы данных ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- ариадататаблеварнингид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fb9e8e97336199b5b133dc59ef7c5f0900f7bdeb0c7a8d8098a51707b107f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122394"
---
# <a name="aria-data-table-warning"></a>Предупреждение таблицы данных ARIA

## <a name="text"></a>Текст

Таблица содержит данные, но не имеет ни сводки, ни допустимого атрибута **ARIA-DescribedBy** .

## <a name="type"></a>Тип

Предупреждение

## <a name="description"></a>Описание

Это предупреждение относится к таблицам HTML с более чем одной ячейкой. Он не применяется к таблицам, `role="presentation"` поскольку они считаются макетными таблицами.

Это предупреждение означает, что таблица идентифицирована как таблица данных, но для нее не определено доступное описание.

> [!Note]  
> Не все таблицы данных должны иметь доступное описание. Необходимо определить доступное описание, если пользователям требуются дополнительные сведения для понимания структуры и содержимого таблицы данных.

 

Чтобы устранить это предупреждение, определите доступное для таблицы описание с помощью атрибута Summary или **ARIA-DescribedBy** .

## <a name="example"></a>Пример


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




