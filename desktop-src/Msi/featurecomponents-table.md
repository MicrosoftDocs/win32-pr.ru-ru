---
description: В таблице Феатурекомпонентс определяется связь между компонентами и компонентами. Для каждого компонента в этой таблице перечислены все компоненты, составляющие эту функцию.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Таблица Феатурекомпонентс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7635a43784ee7e8fbb71c7161bb07d39ffe5238177ea2a7cdaabdeb18dc41e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430874"
---
# <a name="featurecomponents-table"></a>Таблица Феатурекомпонентс

В таблице Феатурекомпонентс определяется связь между компонентами и компонентами. Для каждого компонента в этой таблице перечислены все компоненты, составляющие эту функцию.

Таблица Феатурекомпонентс содержит следующие столбцы.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| Компонент\_   | [Идентификатор](identifier.md) | Д   | Нет        |
| Компонент\_ | [Идентификатор](identifier.md) | Д   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_
</dt> <dd>

Внешний ключ в первом столбце [таблицы](feature-table.md)Feature.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в первом столбце [таблицы Component](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Максимальное число компонентов для каждого компонента — 1600.

Компоненты могут совместно использоваться двумя или более компонентами, то есть один и тот же компонент может ссылаться более чем на одну функцию.

Эта таблица упоминается при выполнении [действия публишфеатурес](publishfeatures-action.md) или [унпублишфеатурес](unpublishfeatures-action.md) .

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE21](ice21.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE47](ice47.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE69](ice69.md)  
</dl>

 

 



