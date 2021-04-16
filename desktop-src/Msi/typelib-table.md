---
description: Таблица TypeLib содержит сведения, которые должны быть помещены в реестр для регистрации библиотек типов.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Таблица TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650474"
---
# <a name="typelib-table"></a><span data-ttu-id="cc2cf-103">Таблица TypeLib</span><span class="sxs-lookup"><span data-stu-id="cc2cf-103">TypeLib Table</span></span>

<span data-ttu-id="cc2cf-104">Таблица TypeLib содержит сведения, которые должны быть помещены в реестр для регистрации библиотек типов.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-104">The TypeLib table contains the information that needs to be placed in the registry registration of type libraries.</span></span>

<span data-ttu-id="cc2cf-105">Таблица TypeLib содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-105">The TypeLib table has the following columns.</span></span>



| <span data-ttu-id="cc2cf-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="cc2cf-106">Column</span></span>      | <span data-ttu-id="cc2cf-107">Type</span><span class="sxs-lookup"><span data-stu-id="cc2cf-107">Type</span></span>                               | <span data-ttu-id="cc2cf-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="cc2cf-108">Key</span></span> | <span data-ttu-id="cc2cf-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="cc2cf-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="cc2cf-110">ID</span><span class="sxs-lookup"><span data-stu-id="cc2cf-110">LibID</span></span>       | [<span data-ttu-id="cc2cf-111">GUID</span><span class="sxs-lookup"><span data-stu-id="cc2cf-111">GUID</span></span>](guid.md)                   | <span data-ttu-id="cc2cf-112">Да</span><span class="sxs-lookup"><span data-stu-id="cc2cf-112">Y</span></span>   | <span data-ttu-id="cc2cf-113">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-113">N</span></span>        |
| <span data-ttu-id="cc2cf-114">Язык</span><span class="sxs-lookup"><span data-stu-id="cc2cf-114">Language</span></span>    | [<span data-ttu-id="cc2cf-115">Integer</span><span class="sxs-lookup"><span data-stu-id="cc2cf-115">Integer</span></span>](integer.md)             | <span data-ttu-id="cc2cf-116">Да</span><span class="sxs-lookup"><span data-stu-id="cc2cf-116">Y</span></span>   | <span data-ttu-id="cc2cf-117">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-117">N</span></span>        |
| <span data-ttu-id="cc2cf-118">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="cc2cf-118">Component\_</span></span> | [<span data-ttu-id="cc2cf-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="cc2cf-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="cc2cf-120">Да</span><span class="sxs-lookup"><span data-stu-id="cc2cf-120">Y</span></span>   | <span data-ttu-id="cc2cf-121">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-121">N</span></span>        |
| <span data-ttu-id="cc2cf-122">Версия</span><span class="sxs-lookup"><span data-stu-id="cc2cf-122">Version</span></span>     | [<span data-ttu-id="cc2cf-123">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="cc2cf-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="cc2cf-124">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-124">N</span></span>   | <span data-ttu-id="cc2cf-125">Да</span><span class="sxs-lookup"><span data-stu-id="cc2cf-125">Y</span></span>        |
| <span data-ttu-id="cc2cf-126">Описание</span><span class="sxs-lookup"><span data-stu-id="cc2cf-126">Description</span></span> | [<span data-ttu-id="cc2cf-127">Text</span><span class="sxs-lookup"><span data-stu-id="cc2cf-127">Text</span></span>](text.md)                   | <span data-ttu-id="cc2cf-128">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-128">N</span></span>   | <span data-ttu-id="cc2cf-129">Да</span><span class="sxs-lookup"><span data-stu-id="cc2cf-129">Y</span></span>        |
| <span data-ttu-id="cc2cf-130">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="cc2cf-130">Directory\_</span></span> | [<span data-ttu-id="cc2cf-131">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="cc2cf-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="cc2cf-132">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-132">N</span></span>   | <span data-ttu-id="cc2cf-133">Да</span><span class="sxs-lookup"><span data-stu-id="cc2cf-133">Y</span></span>        |
| <span data-ttu-id="cc2cf-134">Функция\_</span><span class="sxs-lookup"><span data-stu-id="cc2cf-134">Feature\_</span></span>   | [<span data-ttu-id="cc2cf-135">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="cc2cf-135">Identifier</span></span>](identifier.md)       | <span data-ttu-id="cc2cf-136">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-136">N</span></span>   | <span data-ttu-id="cc2cf-137">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-137">N</span></span>        |
| <span data-ttu-id="cc2cf-138">Стоимость</span><span class="sxs-lookup"><span data-stu-id="cc2cf-138">Cost</span></span>        | [<span data-ttu-id="cc2cf-139">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="cc2cf-139">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="cc2cf-140">Нет</span><span class="sxs-lookup"><span data-stu-id="cc2cf-140">N</span></span>   | <span data-ttu-id="cc2cf-141">Да</span><span class="sxs-lookup"><span data-stu-id="cc2cf-141">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cc2cf-142">Столбцы</span><span class="sxs-lookup"><span data-stu-id="cc2cf-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cc2cf-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>ID</span><span class="sxs-lookup"><span data-stu-id="cc2cf-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span></span>
</dt> <dd>

<span data-ttu-id="cc2cf-144">Идентификатор GUID, определяющий библиотеку.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-144">The GUID that identifies the library.</span></span>

</dd> <dt>

<span data-ttu-id="cc2cf-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Языке</span><span class="sxs-lookup"><span data-stu-id="cc2cf-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="cc2cf-146">Язык библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-146">The language of the type library.</span></span> <span data-ttu-id="cc2cf-147">Это значение должно быть неотрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-147">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="cc2cf-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="cc2cf-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="cc2cf-149">Внешний ключ в первый столбец [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc2cf-149">External key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="cc2cf-150">В этом столбце указывается компонент, принадлежащий компоненту \_ , чей файл ключа является регистрируемой библиотекой типов.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-150">This column identifies the component belonging to Feature\_ whose key file is the type library being registered.</span></span>

</dd> <dt>

<span data-ttu-id="cc2cf-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Версия</span><span class="sxs-lookup"><span data-stu-id="cc2cf-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="cc2cf-152">Это версия библиотеки.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-152">This is the version of the library.</span></span> <span data-ttu-id="cc2cf-153">Основная и дополнительная версии кодируются в 4 байтовое целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-153">The major and minor versions are encoded in the four byte integer value.</span></span> <span data-ttu-id="cc2cf-154">Дополнительная версия находится в младших восьми битах.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-154">The minor version is in the lower eight bits.</span></span> <span data-ttu-id="cc2cf-155">Основная версия находится в среднем шестнадцати бит.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-155">The major version is in the middle sixteen bits.</span></span>

</dd> <dt>

<span data-ttu-id="cc2cf-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="cc2cf-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="cc2cf-157">Локализуемое описание библиотеки.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-157">A localizable description of the library.</span></span>

</dd> <dt>

<span data-ttu-id="cc2cf-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Каталоги\_</span><span class="sxs-lookup"><span data-stu-id="cc2cf-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="cc2cf-159">Внешний ключ в первом столбце [таблицы Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc2cf-159">External key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="cc2cf-160">В этом столбце указывается путь справки для библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-160">This column identifies the Help path for the type library.</span></span> <span data-ttu-id="cc2cf-161">Во время объявления этот столбец не учитывается.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-161">This column is ignored during advertising.</span></span>

</dd> <dt>

<span data-ttu-id="cc2cf-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_</span><span class="sxs-lookup"><span data-stu-id="cc2cf-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="cc2cf-163">Внешний ключ в первый столбец [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc2cf-163">External key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="cc2cf-164">В этом столбце указывается компонент, который должен быть установлен, чтобы библиотека типов была работоспособной.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-164">This column specifies the feature that must be installed for the type library to be operational.</span></span>

</dd> <dt>

<span data-ttu-id="cc2cf-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Маршрут</span><span class="sxs-lookup"><span data-stu-id="cc2cf-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="cc2cf-166">Стоимость, связанная с регистрацией библиотеки типов в байтах.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-166">The cost associated with the registration of the type library in bytes.</span></span> <span data-ttu-id="cc2cf-167">Это должно быть неотрицательное число или значение null.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-167">This must be a non-negative number or null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc2cf-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc2cf-168">Remarks</span></span>

<span data-ttu-id="cc2cf-169">Эта таблица упоминается при выполнении [действия регистертипелибрариес](registertypelibraries-action.md) или [унрегистертипелибрариес](unregistertypelibraries-action.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2cf-169">This table is referred to when the [RegisterTypeLibraries action](registertypelibraries-action.md) or the [UnregisterTypeLibraries action](unregistertypelibraries-action.md) is executed.</span></span>

<span data-ttu-id="cc2cf-170">Установщик записывает все сведения о регистрации библиотеки типов в \_ \_ расположение реестра для ЛОКАЛЬНОГО компьютера hKey (HKLM).</span><span class="sxs-lookup"><span data-stu-id="cc2cf-170">The installer writes all type library registration information into the HKEY\_LOCAL\_MACHINE (HKLM) registry location.</span></span> <span data-ttu-id="cc2cf-171">Это происходит даже при установке отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-171">This is the case even for per-user installations.</span></span> <span data-ttu-id="cc2cf-172">Библиотеки типов не могут быть зарегистрированы в расположениях для отдельных пользователей (HKCU).</span><span class="sxs-lookup"><span data-stu-id="cc2cf-172">Type libraries cannot be registered in per-user locations (HKCU).</span></span>

<span data-ttu-id="cc2cf-173">Авторы пакета установки настоятельно рекомендуем использовать таблицу TypeLib.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-173">Installation package authors are strongly advised against using the TypeLib table.</span></span> <span data-ttu-id="cc2cf-174">Вместо этого они должны регистрировать библиотеки типов с помощью таблицы [реестра](registry-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2cf-174">Instead, they should register type libraries by using the [Registry](registry-table.md) table.</span></span> <span data-ttu-id="cc2cf-175">Причины для предотвращения самостоятельной регистрации:</span><span class="sxs-lookup"><span data-stu-id="cc2cf-175">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="cc2cf-176">Если установка, использующая таблицу TypeLib, завершается ошибкой и должна быть выполнена откат, то откат может не восстановить состояние компьютера, существовавшего до отката.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-176">If an installation using the TypeLib table fails and must be rolled back, the rollback may not restore the computer to the same state that existed prior to the rollback.</span></span> <span data-ttu-id="cc2cf-177">Библиотеки типов, зарегистрированные до отката, могут быть не зарегистрированы после отката.</span><span class="sxs-lookup"><span data-stu-id="cc2cf-177">Type libraries registered prior to rollback may not be registered after rollback.</span></span>

## <a name="validation"></a><span data-ttu-id="cc2cf-178">Проверка</span><span class="sxs-lookup"><span data-stu-id="cc2cf-178">Validation</span></span>

<dl>

[<span data-ttu-id="cc2cf-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="cc2cf-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cc2cf-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="cc2cf-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cc2cf-181">ICE19</span><span class="sxs-lookup"><span data-stu-id="cc2cf-181">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="cc2cf-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="cc2cf-182">ICE32</span></span>](ice32.md)  
</dl>

 

 



