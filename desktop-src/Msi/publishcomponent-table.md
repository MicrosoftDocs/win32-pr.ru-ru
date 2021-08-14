---
description: Таблица Публишкомпонент связывает компоненты, перечисленные в таблице Component, с квалификатором Text-String и ИДЕНТИФИКАТОРом категории GUID.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Таблица Публишкомпонент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0abd7567e8327aa36a120fd5a13115cb191e1660566e9d480446295dca53cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376387"
---
# <a name="publishcomponent-table"></a>Таблица Публишкомпонент

Таблица Публишкомпонент связывает компоненты, перечисленные в [таблице Component](component-table.md) , с квалификатором Text-String и идентификатором категории GUID. Компоненты с параллельной функциональностью, сгруппированной таким образом, называются квалифицированными компонентами. См. раздел [полные компоненты](qualified-components.md). Это предоставляет установщику метод для одноуровневого косвенного обращения при ссылке на компоненты. См. раздел [Использование компонентов с квалификаторами](using-qualified-components.md).

Таблица Публишкомпонент содержит следующие столбцы.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| ComponentId | [GUID](guid.md)             | Д   | Нет        |
| Квалификатор   | [Text](text.md)             | Д   | Нет        |
| Компонент\_ | [Идентификатор](identifier.md) | Д   | Нет        |
| AppData     | [Text](text.md)             | Нет   | Д        |
| Компонент\_   | [Идентификатор](identifier.md) | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

Строковый [идентификатор GUID](guid.md) , представляющий категорию компонентов, которые группируются вместе. Обратите внимание, что заголовок этого столбца является ошибочным. Это идентификатор GUID для категории подходящих компонентов, который не совпадает с идентификатором GUID, отображаемым в столбце ComponentId [таблицы Component](component-table.md). Здесь он относится к серверу, который предоставляет функции компонента внешним клиентам, а не самому компоненту.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Квалификатор
</dt> <dd>

Текстовая строка, которая определяет значение в столбце ComponentId. Квалификатор используется для различения нескольких форм одного и того же компонента, например компонента, реализованного на нескольких языках. Это описательные текстовые строки, возвращаемые функцией [**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в столбце одна из [таблиц Component](component-table.md). Этот идентификатор ссылается на запись полного компонента в таблице Component.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>Папка
</dt> <dd>

Необязательный локализуемый текст, описывающий полный компонент этой записи. Строка обычно анализируется приложением и может отображаться для пользователя. Он должен описывать полный компонент. Это можно получить с помощью [**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_
</dt> <dd>

Внешний ключ в столбце одна из [таблиц Feature](feature-table.md). Это функция, использующая этот компонент.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта таблица упоминается при выполнении [действия публишкомпонентс](publishcomponents-action.md) или [унпублишкомпонентс](unpublishcomponents-action.md) .

Обратите внимание, что имя этой таблицы является ошибочным. Эта таблица не требуется для создания объявления. Сведения о том, как задать состояние установки компонентов для объявления, см. в столбце атрибуты [таблицы Component](component-table.md) и [таблицы функций](feature-table.md) .

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



