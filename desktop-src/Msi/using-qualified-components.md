---
description: Квалифицированные компоненты — это метод косвенного обращения, который можно использовать для группирования компонентов с параллельными функциями в категории.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Использование полных компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145313"
---
# <a name="using-qualified-components"></a><span data-ttu-id="546b1-103">Использование полных компонентов</span><span class="sxs-lookup"><span data-stu-id="546b1-103">Using Qualified Components</span></span>

<span data-ttu-id="546b1-104">Квалифицированные компоненты — это метод косвенного обращения, который можно использовать для группирования компонентов с параллельными функциями в категории.</span><span class="sxs-lookup"><span data-stu-id="546b1-104">Qualified components are a method of indirection and can be used to group components with parallel functionality into categories.</span></span>

<span data-ttu-id="546b1-105">Чтобы получить полный путь и установить [полный компонент](qualified-components.md), вызовите [**мсипровидекуалифиедкомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) или [**мсипровидекуалифиедкомпонентекс**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span><span class="sxs-lookup"><span data-stu-id="546b1-105">To return the full path and install a [qualified component](qualified-components.md), call [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span></span>

<span data-ttu-id="546b1-106">Чтобы перечислить все полные квалификаторы компонентов и описательные строки, вызовите [**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="546b1-106">To enumerate all of the qualified component qualifiers and descriptive strings, call [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

<span data-ttu-id="546b1-107">**Группирование компонентов в категорию полных компонентов**</span><span class="sxs-lookup"><span data-stu-id="546b1-107">**To group components together into a qualified-component category**</span></span>

1.  <span data-ttu-id="546b1-108">В [таблице Component](component-table.md) должна быть запись для каждого компонента, включенного в новую категорию подходящих компонентов.</span><span class="sxs-lookup"><span data-stu-id="546b1-108">There must be a record in the [Component table](component-table.md) for each component that is included in the new category of qualified components.</span></span> <span data-ttu-id="546b1-109">Создайте поля в таблице компонентов так же, как и для обычных компонентов.</span><span class="sxs-lookup"><span data-stu-id="546b1-109">Author the fields in the Component table the same as for ordinary components.</span></span> <span data-ttu-id="546b1-110">Обратите внимание, что каждый квалифицированный компонент должен иметь уникальный идентификатор GUID компонента, введенный в столбец ComponentId таблицы Component.</span><span class="sxs-lookup"><span data-stu-id="546b1-110">Note that each qualified component must have a unique component ID GUID entered in the ComponentId column of the Component table.</span></span>
2.  <span data-ttu-id="546b1-111">Создайте текстовую строку квалификатора для каждого квалифицированного компонента.</span><span class="sxs-lookup"><span data-stu-id="546b1-111">Generate a qualifier text string for each qualified component.</span></span> <span data-ttu-id="546b1-112">Квалификатор должен быть уникальной текстовой строкой, которая может быть легко создана при поиске квалифицированного компонента.</span><span class="sxs-lookup"><span data-stu-id="546b1-112">The qualifier must be unique text string that can be easily generated when searching for a qualified component.</span></span> <span data-ttu-id="546b1-113">Например, если компоненты в категории квалифицированы по языку, числовой идентификатор локали (LCID) является разумной строкой квалификатора.</span><span class="sxs-lookup"><span data-stu-id="546b1-113">For example, if the components in the category are being qualified by language, the numeric locale identifier (LCID) is a reasonable qualifier string.</span></span>
3.  <span data-ttu-id="546b1-114">Добавьте запись в [таблицу публишкомпонент](publishcomponent-table.md) для каждого квалифицированного компонента.</span><span class="sxs-lookup"><span data-stu-id="546b1-114">Add a record in the [PublishComponent table](publishcomponent-table.md) for each qualified component.</span></span> <span data-ttu-id="546b1-115">Введите идентификаторы компонентов из столбца Component Таблицы Component в \_ столбец Component Таблицы публишкомпонент.</span><span class="sxs-lookup"><span data-stu-id="546b1-115">Enter the qualified-component identifiers from the Component column of the Component table into the Component\_ column of the PublishComponent table.</span></span> <span data-ttu-id="546b1-116">Введите строки квалификатора для каждого квалифицированного компонента в столбец квалификатора.</span><span class="sxs-lookup"><span data-stu-id="546b1-116">Enter the qualifier strings for each qualified component into the Qualifier column.</span></span> <span data-ttu-id="546b1-117">Введите локализованную строку, которая будет отображаться пользователю, и опишите полный компонент в необязательном столбце AppData.</span><span class="sxs-lookup"><span data-stu-id="546b1-117">Enter a localized string to be displayed to the user and describing the qualified component into the optional AppData column.</span></span> <span data-ttu-id="546b1-118">Пояснительная строка должна быть размещена в поле AppData, например "французский словарь", а не только с числовым кодом LCID.</span><span class="sxs-lookup"><span data-stu-id="546b1-118">An explanatory string should be put in the AppData field, such as "French Dictionary," rather than just the numeric LCID.</span></span> <span data-ttu-id="546b1-119">Введите имя компонента, использующего этот компонент, в \_ столбец Feature.</span><span class="sxs-lookup"><span data-stu-id="546b1-119">Enter the name of the feature that uses this component into the Feature\_ column.</span></span> <span data-ttu-id="546b1-120">Идентификатор компонента в этом поле также должен быть указан в столбце Feature [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="546b1-120">The feature identifier in this field must also be listed in the Feature column of the [Feature table](feature-table.md).</span></span>
4.  <span data-ttu-id="546b1-121">Создать GUID категории для этой категории компонентов с квалификаторами.</span><span class="sxs-lookup"><span data-stu-id="546b1-121">Generate a category GUID for this category of qualified components.</span></span> <span data-ttu-id="546b1-122">Это должен быть допустимый [GUID](guid.md).</span><span class="sxs-lookup"><span data-stu-id="546b1-122">This must be a valid [GUID](guid.md).</span></span> <span data-ttu-id="546b1-123">Если вы используете служебную программу, например GUIDGEN для создания идентификатора GUID, убедитесь, что она содержит только прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="546b1-123">If you use a utility such as GUIDGEN to generate the GUID be sure that it contains only uppercase letters.</span></span> <span data-ttu-id="546b1-124">Для каждого квалифицированного компонента в этой категории введите GUID категории в поле ComponentId [таблицы публишкомпонент](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="546b1-124">For every qualified component in this category, enter the category GUID into the ComponentId field of the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="546b1-125">В следующем примере показано, как в таблице Components, Feature и Публишкомпонент были созданы Категория "шаблоны факсов" для компонентов с квалификаторами.</span><span class="sxs-lookup"><span data-stu-id="546b1-125">The following example illustrates how the "FAX Templates" category of qualified components are authored into the Component, Feature, and PublishComponent tables.</span></span>

[<span data-ttu-id="546b1-126">Таблица Публишкомпонент</span><span class="sxs-lookup"><span data-stu-id="546b1-126">PublishComponent table</span></span>](publishcomponent-table.md)



| <span data-ttu-id="546b1-127">ComponentId</span><span class="sxs-lookup"><span data-stu-id="546b1-127">ComponentId</span></span>                  | <span data-ttu-id="546b1-128">Квалификатор</span><span class="sxs-lookup"><span data-stu-id="546b1-128">Qualifier</span></span> | <span data-ttu-id="546b1-129">AppData</span><span class="sxs-lookup"><span data-stu-id="546b1-129">AppData</span></span>             | <span data-ttu-id="546b1-130">Функция\_</span><span class="sxs-lookup"><span data-stu-id="546b1-130">Feature\_</span></span>   | <span data-ttu-id="546b1-131">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="546b1-131">Component\_</span></span>    |
|------------------------------|-----------|---------------------|-------------|----------------|
| <span data-ttu-id="546b1-132">{GUID категории шаблона ФАКСа}</span><span class="sxs-lookup"><span data-stu-id="546b1-132">{FAX Template Category GUID}</span></span> | <span data-ttu-id="546b1-133">1033</span><span class="sxs-lookup"><span data-stu-id="546b1-133">1033</span></span>      | <span data-ttu-id="546b1-134">Шаблон для английского языка (США)</span><span class="sxs-lookup"><span data-stu-id="546b1-134">US English template</span></span> | <span data-ttu-id="546b1-135">факстемплате</span><span class="sxs-lookup"><span data-stu-id="546b1-135">FAXTemplate</span></span> | <span data-ttu-id="546b1-136">факстемплатину</span><span class="sxs-lookup"><span data-stu-id="546b1-136">FAXTemplateENU</span></span> |
|                              | <span data-ttu-id="546b1-137">1041</span><span class="sxs-lookup"><span data-stu-id="546b1-137">1041</span></span>      | <span data-ttu-id="546b1-138">Японский шаблон</span><span class="sxs-lookup"><span data-stu-id="546b1-138">Japanese template</span></span>   | <span data-ttu-id="546b1-139">факстемплате</span><span class="sxs-lookup"><span data-stu-id="546b1-139">FAXTemplate</span></span> | <span data-ttu-id="546b1-140">факстемплатежпн</span><span class="sxs-lookup"><span data-stu-id="546b1-140">FAXTemplateJPN</span></span> |
|                              | <span data-ttu-id="546b1-141">1054</span><span class="sxs-lookup"><span data-stu-id="546b1-141">1054</span></span>      | <span data-ttu-id="546b1-142">Шаблон для тайского языка</span><span class="sxs-lookup"><span data-stu-id="546b1-142">Thai template</span></span>       | <span data-ttu-id="546b1-143">факстемплате</span><span class="sxs-lookup"><span data-stu-id="546b1-143">FAXTemplate</span></span> | <span data-ttu-id="546b1-144">факстемплатеса</span><span class="sxs-lookup"><span data-stu-id="546b1-144">FAXTemplateTHA</span></span> |
|                              | <span data-ttu-id="546b1-145">1031</span><span class="sxs-lookup"><span data-stu-id="546b1-145">1031</span></span>      | <span data-ttu-id="546b1-146">Шаблон для немецкого языка</span><span class="sxs-lookup"><span data-stu-id="546b1-146">German template</span></span>     | <span data-ttu-id="546b1-147">факстемплате</span><span class="sxs-lookup"><span data-stu-id="546b1-147">FAXTemplate</span></span> | <span data-ttu-id="546b1-148">факстемплатедеу</span><span class="sxs-lookup"><span data-stu-id="546b1-148">FAXTemplateDEU</span></span> |



 

<span data-ttu-id="546b1-149">[Таблица Component](component-table.md) (частичная таблица)</span><span class="sxs-lookup"><span data-stu-id="546b1-149">[Component table](component-table.md) (partial table)</span></span>



| <span data-ttu-id="546b1-150">Компонент</span><span class="sxs-lookup"><span data-stu-id="546b1-150">Component</span></span>      | <span data-ttu-id="546b1-151">ComponentId</span><span class="sxs-lookup"><span data-stu-id="546b1-151">ComponentId</span></span>                                  |
|----------------|----------------------------------------------|
| <span data-ttu-id="546b1-152">факстемплатину</span><span class="sxs-lookup"><span data-stu-id="546b1-152">FAXTemplateENU</span></span> | <span data-ttu-id="546b1-153">{*GUID компонента шаблона факса (Английский (США))*</span><span class="sxs-lookup"><span data-stu-id="546b1-153">{*FAX Template (US English) component GUID*}</span></span> |
| <span data-ttu-id="546b1-154">факстемплатежпн</span><span class="sxs-lookup"><span data-stu-id="546b1-154">FAXTemplateJPN</span></span> | <span data-ttu-id="546b1-155">{*GUID компонента шаблона факса (японский)*}</span><span class="sxs-lookup"><span data-stu-id="546b1-155">{*FAX Template (Japanese) component GUID*}</span></span>   |
| <span data-ttu-id="546b1-156">факстемплатеса</span><span class="sxs-lookup"><span data-stu-id="546b1-156">FAXTemplateTHA</span></span> | <span data-ttu-id="546b1-157">{*GUID компонента шаблона факса (тайский)*}</span><span class="sxs-lookup"><span data-stu-id="546b1-157">{*FAX Template (Thai) component GUID*}</span></span>       |
| <span data-ttu-id="546b1-158">факстемплатедеу</span><span class="sxs-lookup"><span data-stu-id="546b1-158">FAXTemplateDEU</span></span> | <span data-ttu-id="546b1-159">{*GUID компонента шаблона факса (немецкий)*}</span><span class="sxs-lookup"><span data-stu-id="546b1-159">{*FAX Template (German) component GUID*}</span></span>     |



 

<span data-ttu-id="546b1-160">[Таблица компонентов](feature-table.md) (частичная таблица)</span><span class="sxs-lookup"><span data-stu-id="546b1-160">[Feature table](feature-table.md) (partial table)</span></span>



| <span data-ttu-id="546b1-161">Функция</span><span class="sxs-lookup"><span data-stu-id="546b1-161">Feature</span></span>     |
|-------------|
| <span data-ttu-id="546b1-162">факстемплате</span><span class="sxs-lookup"><span data-stu-id="546b1-162">FAXTemplate</span></span> |
| <span data-ttu-id="546b1-163">факстемплате</span><span class="sxs-lookup"><span data-stu-id="546b1-163">FAXTemplate</span></span> |
| <span data-ttu-id="546b1-164">факстемплате</span><span class="sxs-lookup"><span data-stu-id="546b1-164">FAXTemplate</span></span> |
| <span data-ttu-id="546b1-165">факстемплате</span><span class="sxs-lookup"><span data-stu-id="546b1-165">FAXTemplate</span></span> |



 

 

 



