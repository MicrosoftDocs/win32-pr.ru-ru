---
description: Таблица Публишкомпонент связывает компоненты, перечисленные в таблице Component, с квалификатором Text-String и ИДЕНТИФИКАТОРом категории GUID.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Таблица Публишкомпонент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673680"
---
# <a name="publishcomponent-table"></a><span data-ttu-id="c75ea-103">Таблица Публишкомпонент</span><span class="sxs-lookup"><span data-stu-id="c75ea-103">PublishComponent Table</span></span>

<span data-ttu-id="c75ea-104">Таблица Публишкомпонент связывает компоненты, перечисленные в [таблице Component](component-table.md) , с квалификатором Text-String и идентификатором категории GUID.</span><span class="sxs-lookup"><span data-stu-id="c75ea-104">The PublishComponent table associates components listed in the [Component table](component-table.md) with a qualifier text-string and a category ID GUID.</span></span> <span data-ttu-id="c75ea-105">Компоненты с параллельной функциональностью, сгруппированной таким образом, называются квалифицированными компонентами.</span><span class="sxs-lookup"><span data-stu-id="c75ea-105">Components with parallel functionality that have been grouped together in this way are referred to as qualified components.</span></span> <span data-ttu-id="c75ea-106">См. раздел [полные компоненты](qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="c75ea-106">See [Qualified Components](qualified-components.md).</span></span> <span data-ttu-id="c75ea-107">Это предоставляет установщику метод для одноуровневого косвенного обращения при ссылке на компоненты.</span><span class="sxs-lookup"><span data-stu-id="c75ea-107">This provides the installer with a method for single-level indirection when referring to components.</span></span> <span data-ttu-id="c75ea-108">См. раздел [Использование компонентов с квалификаторами](using-qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="c75ea-108">See [Using Qualified Components](using-qualified-components.md).</span></span>

<span data-ttu-id="c75ea-109">Таблица Публишкомпонент содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="c75ea-109">The PublishComponent table has the following columns.</span></span>



| <span data-ttu-id="c75ea-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="c75ea-110">Column</span></span>      | <span data-ttu-id="c75ea-111">Type</span><span class="sxs-lookup"><span data-stu-id="c75ea-111">Type</span></span>                         | <span data-ttu-id="c75ea-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="c75ea-112">Key</span></span> | <span data-ttu-id="c75ea-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="c75ea-113">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="c75ea-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="c75ea-114">ComponentId</span></span> | [<span data-ttu-id="c75ea-115">GUID</span><span class="sxs-lookup"><span data-stu-id="c75ea-115">GUID</span></span>](guid.md)             | <span data-ttu-id="c75ea-116">Да</span><span class="sxs-lookup"><span data-stu-id="c75ea-116">Y</span></span>   | <span data-ttu-id="c75ea-117">Нет</span><span class="sxs-lookup"><span data-stu-id="c75ea-117">N</span></span>        |
| <span data-ttu-id="c75ea-118">Квалификатор</span><span class="sxs-lookup"><span data-stu-id="c75ea-118">Qualifier</span></span>   | [<span data-ttu-id="c75ea-119">Text</span><span class="sxs-lookup"><span data-stu-id="c75ea-119">Text</span></span>](text.md)             | <span data-ttu-id="c75ea-120">Да</span><span class="sxs-lookup"><span data-stu-id="c75ea-120">Y</span></span>   | <span data-ttu-id="c75ea-121">Нет</span><span class="sxs-lookup"><span data-stu-id="c75ea-121">N</span></span>        |
| <span data-ttu-id="c75ea-122">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="c75ea-122">Component\_</span></span> | [<span data-ttu-id="c75ea-123">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c75ea-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="c75ea-124">Да</span><span class="sxs-lookup"><span data-stu-id="c75ea-124">Y</span></span>   | <span data-ttu-id="c75ea-125">Нет</span><span class="sxs-lookup"><span data-stu-id="c75ea-125">N</span></span>        |
| <span data-ttu-id="c75ea-126">AppData</span><span class="sxs-lookup"><span data-stu-id="c75ea-126">AppData</span></span>     | [<span data-ttu-id="c75ea-127">Text</span><span class="sxs-lookup"><span data-stu-id="c75ea-127">Text</span></span>](text.md)             | <span data-ttu-id="c75ea-128">Нет</span><span class="sxs-lookup"><span data-stu-id="c75ea-128">N</span></span>   | <span data-ttu-id="c75ea-129">Да</span><span class="sxs-lookup"><span data-stu-id="c75ea-129">Y</span></span>        |
| <span data-ttu-id="c75ea-130">Функция\_</span><span class="sxs-lookup"><span data-stu-id="c75ea-130">Feature\_</span></span>   | [<span data-ttu-id="c75ea-131">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c75ea-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="c75ea-132">Нет</span><span class="sxs-lookup"><span data-stu-id="c75ea-132">N</span></span>   | <span data-ttu-id="c75ea-133">Нет</span><span class="sxs-lookup"><span data-stu-id="c75ea-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c75ea-134">Столбцы</span><span class="sxs-lookup"><span data-stu-id="c75ea-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c75ea-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="c75ea-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="c75ea-136">Строковый [идентификатор GUID](guid.md) , представляющий категорию компонентов, которые группируются вместе.</span><span class="sxs-lookup"><span data-stu-id="c75ea-136">A string [GUID](guid.md) that represents the category of components being grouped together.</span></span> <span data-ttu-id="c75ea-137">Обратите внимание, что заголовок этого столбца является ошибочным.</span><span class="sxs-lookup"><span data-stu-id="c75ea-137">Note that this column's title is misleading.</span></span> <span data-ttu-id="c75ea-138">Это идентификатор GUID для категории подходящих компонентов, который не совпадает с идентификатором GUID, отображаемым в столбце ComponentId [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c75ea-138">This is the GUID for the category of qualified components and is not the same GUID appearing in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="c75ea-139">Здесь он относится к серверу, который предоставляет функции компонента внешним клиентам, а не самому компоненту.</span><span class="sxs-lookup"><span data-stu-id="c75ea-139">Here it refers to a server that provides the functionality of a component to external clients rather than the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="c75ea-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Квалификатор</span><span class="sxs-lookup"><span data-stu-id="c75ea-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualifier</span></span>
</dt> <dd>

<span data-ttu-id="c75ea-141">Текстовая строка, которая определяет значение в столбце ComponentId.</span><span class="sxs-lookup"><span data-stu-id="c75ea-141">A text string that qualifies the value in the ComponentId column.</span></span> <span data-ttu-id="c75ea-142">Квалификатор используется для различения нескольких форм одного и того же компонента, например компонента, реализованного на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="c75ea-142">A qualifier is used to distinguish multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span> <span data-ttu-id="c75ea-143">Это описательные текстовые строки, возвращаемые функцией [**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="c75ea-143">These are the qualifier text-strings returned by [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="c75ea-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="c75ea-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="c75ea-145">Внешний ключ в столбце одна из [таблиц Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c75ea-145">External key into column one of the [Component table](component-table.md).</span></span> <span data-ttu-id="c75ea-146">Этот идентификатор ссылается на запись полного компонента в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="c75ea-146">This identifier refers to the qualified component's record in the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="c75ea-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>Папка</span><span class="sxs-lookup"><span data-stu-id="c75ea-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span></span>
</dt> <dd>

<span data-ttu-id="c75ea-148">Необязательный локализуемый текст, описывающий полный компонент этой записи.</span><span class="sxs-lookup"><span data-stu-id="c75ea-148">An optional localizable text describing the qualified component of this record.</span></span> <span data-ttu-id="c75ea-149">Строка обычно анализируется приложением и может отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c75ea-149">The string is commonly parsed by the application and can be displayed to the user.</span></span> <span data-ttu-id="c75ea-150">Он должен описывать полный компонент.</span><span class="sxs-lookup"><span data-stu-id="c75ea-150">It should describe the qualified component.</span></span> <span data-ttu-id="c75ea-151">Это можно получить с помощью [**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="c75ea-151">This can be retrieved with [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="c75ea-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_</span><span class="sxs-lookup"><span data-stu-id="c75ea-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="c75ea-153">Внешний ключ в столбце одна из [таблиц Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c75ea-153">External key into column one of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="c75ea-154">Это функция, использующая этот компонент.</span><span class="sxs-lookup"><span data-stu-id="c75ea-154">This is the feature using this qualified component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c75ea-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c75ea-155">Remarks</span></span>

<span data-ttu-id="c75ea-156">Эта таблица упоминается при выполнении [действия публишкомпонентс](publishcomponents-action.md) или [унпублишкомпонентс](unpublishcomponents-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c75ea-156">This table is referred to when the [PublishComponents action](publishcomponents-action.md) or the [UnpublishComponents action](unpublishcomponents-action.md) is executed.</span></span>

<span data-ttu-id="c75ea-157">Обратите внимание, что имя этой таблицы является ошибочным.</span><span class="sxs-lookup"><span data-stu-id="c75ea-157">Note that the name of this table is misleading.</span></span> <span data-ttu-id="c75ea-158">Эта таблица не требуется для создания объявления.</span><span class="sxs-lookup"><span data-stu-id="c75ea-158">This table is not required in order to author advertisement.</span></span> <span data-ttu-id="c75ea-159">Сведения о том, как задать состояние установки компонентов для объявления, см. в столбце атрибуты [таблицы Component](component-table.md) и [таблицы функций](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c75ea-159">See the Attributes column of the [Component table](component-table.md) and [Feature table](feature-table.md) for information on how to set the installation state of components to advertise.</span></span>

## <a name="validation"></a><span data-ttu-id="c75ea-160">Проверка</span><span class="sxs-lookup"><span data-stu-id="c75ea-160">Validation</span></span>

<dl>

[<span data-ttu-id="c75ea-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="c75ea-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c75ea-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="c75ea-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c75ea-163">ICE19</span><span class="sxs-lookup"><span data-stu-id="c75ea-163">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="c75ea-164">ICE22</span><span class="sxs-lookup"><span data-stu-id="c75ea-164">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="c75ea-165">ICE32</span><span class="sxs-lookup"><span data-stu-id="c75ea-165">ICE32</span></span>](ice32.md)  
</dl>

 

 



