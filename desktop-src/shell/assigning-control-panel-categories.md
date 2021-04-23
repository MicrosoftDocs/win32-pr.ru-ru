---
description: Начиная с Windows XP, панель управления поддерживает категоризацию элементов панели управления. Элементы регистрируются для появления в одной или нескольких категориях. Не удается создать новые категории.
title: Назначение категорий панели управления
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984364"
---
# <a name="assigning-control-panel-categories"></a><span data-ttu-id="c6a14-105">Назначение категорий панели управления</span><span class="sxs-lookup"><span data-stu-id="c6a14-105">Assigning Control Panel Categories</span></span>

<span data-ttu-id="c6a14-106">Начиная с Windows XP, панель управления поддерживает категоризацию элементов панели управления.</span><span class="sxs-lookup"><span data-stu-id="c6a14-106">As of Windows XP, Control Panel supports categorization of Control Panel items.</span></span> <span data-ttu-id="c6a14-107">Элементы регистрируются для появления в одной или нескольких категориях.</span><span class="sxs-lookup"><span data-stu-id="c6a14-107">Items are registered to appear in one or more category.</span></span> <span data-ttu-id="c6a14-108">Не удается создать новые категории.</span><span class="sxs-lookup"><span data-stu-id="c6a14-108">New categories cannot be created.</span></span>

<span data-ttu-id="c6a14-109">Чтобы зарегистрировать элемент панели управления в одной или нескольких категориях, добавьте значения, как описано в разделе Регистрация элемента панели управления [исполняемый файл](registering-control-panel-items.md) или [регистрация элемента панели управления DLL](registering-control-panel-items.md) на странице Регистрация [элементов панели управления](registering-control-panel-items.md)в соответствии с соответствующими задачами.</span><span class="sxs-lookup"><span data-stu-id="c6a14-109">To register a Control Panel item in one or more categories, add values as explained in the [Executable Control Panel Item Registration](registering-control-panel-items.md) or [DLL Control Panel Item Registration](registering-control-panel-items.md) section of [Registering Control Panel Items](registering-control-panel-items.md), as appropriate.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6a14-110">Идентификатор категории</span><span class="sxs-lookup"><span data-stu-id="c6a14-110">Category ID</span></span></th>
<th><span data-ttu-id="c6a14-111">Имя категории (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="c6a14-111">Category Name (Windows 7)</span></span></th>
<th><span data-ttu-id="c6a14-112">Имя категории (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="c6a14-112">Category Name (Windows Vista)</span></span></th>
<th><span data-ttu-id="c6a14-113">Имя категории (Windows XP)</span><span class="sxs-lookup"><span data-stu-id="c6a14-113">Category Name (Windows XP)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6a14-114">0</span><span class="sxs-lookup"><span data-stu-id="c6a14-114">0</span></span></td>
<td><span data-ttu-id="c6a14-115">&quot;Все элементы панели управления&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-115">&quot;All Control Panel Items&quot;</span></span></td>
<td><span data-ttu-id="c6a14-116">&quot;Дополнительные параметры&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-116">&quot;Additional Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6a14-117">В этой категории отображается любой элемент панели управления, не указывающий идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="c6a14-117">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c6a14-118">&quot;Другие параметры панели управления&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-118">&quot;Other Control Panel Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6a14-119">В этой категории отображается любой элемент панели управления, не указывающий идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="c6a14-119">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a14-120">1</span><span class="sxs-lookup"><span data-stu-id="c6a14-120">1</span></span></td>
<td><span data-ttu-id="c6a14-121">&quot;"Оформление и персонализация"&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-121">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="c6a14-122">&quot;"Оформление и персонализация"&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-122">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="c6a14-123">&quot;Внешний вид и темы&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-123">&quot;Appearance and Themes&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6a14-124">2</span><span class="sxs-lookup"><span data-stu-id="c6a14-124">2</span></span></td>
<td><span data-ttu-id="c6a14-125">&quot;Оборудование и звук&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-125">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="c6a14-126">&quot;Оборудование и звук&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-126">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="c6a14-127">&quot;Принтеры и другое оборудование&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-127">&quot;Printers and Other Hardware&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a14-128">3</span><span class="sxs-lookup"><span data-stu-id="c6a14-128">3</span></span></td>
<td><span data-ttu-id="c6a14-129">&quot;"Сеть и Интернет"&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-129">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="c6a14-130">&quot;"Сеть и Интернет"&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-130">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="c6a14-131">&quot;Подключение к сети и Интернету&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-131">&quot;Network and Internet Connections&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6a14-132">4</span><span class="sxs-lookup"><span data-stu-id="c6a14-132">4</span></span></td>
<td><span data-ttu-id="c6a14-133">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="c6a14-133">No longer used.</span></span> <span data-ttu-id="c6a14-134">Любой элемент, который добавляет себя только в категорию 4, отображается в категории 2 (оборудование и звук).</span><span class="sxs-lookup"><span data-stu-id="c6a14-134">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="c6a14-135">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="c6a14-135">No longer used.</span></span> <span data-ttu-id="c6a14-136">Любой элемент, который добавляет себя только в категорию 4, отображается в категории 2 (оборудование и звук).</span><span class="sxs-lookup"><span data-stu-id="c6a14-136">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="c6a14-137">&quot;Звуки, речь и звуковые устройства&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-137">&quot;Sounds, Speech, and Audio Devices&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a14-138">5</span><span class="sxs-lookup"><span data-stu-id="c6a14-138">5</span></span></td>
<td><span data-ttu-id="c6a14-139">&quot;Система и безопасность&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-139">&quot;System and Security&quot;</span></span></td>
<td><span data-ttu-id="c6a14-140">&quot;Система и обслуживание&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-140">&quot;System and Maintenance&quot;</span></span></td>
<td><span data-ttu-id="c6a14-141">&quot;Производительность и обслуживание&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-141">&quot;Performance and Maintenance&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6a14-142">6</span><span class="sxs-lookup"><span data-stu-id="c6a14-142">6</span></span></td>
<td><span data-ttu-id="c6a14-143">&quot;Часы, язык и регион&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-143">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="c6a14-144">&quot;Часы, язык и регион&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-144">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="c6a14-145">&quot;Параметры даты, времени, языка и региональных параметров&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-145">&quot;Date, Time, Language, and Regional Options&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a14-146">7</span><span class="sxs-lookup"><span data-stu-id="c6a14-146">7</span></span></td>
<td><span data-ttu-id="c6a14-147">&quot;Простота доступа&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-147">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="c6a14-148">&quot;Простота доступа&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-148">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="c6a14-149">&quot;Специальные возможности&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-149">&quot;Accessibility Options&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6a14-150">8</span><span class="sxs-lookup"><span data-stu-id="c6a14-150">8</span></span></td>
<td><span data-ttu-id="c6a14-151">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-151">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="c6a14-152">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-152">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="c6a14-153">&quot;Установка и удаление программ&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-153">&quot;Add or Remove Programs&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a14-154">9</span><span class="sxs-lookup"><span data-stu-id="c6a14-154">9</span></span></td>
<td><span data-ttu-id="c6a14-155">&quot;Учетные записи пользователей&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-155">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6a14-156">При отсутствии подключения к домену это называется &quot; учетными записями пользователей и семейной безопасностью &quot; .</span><span class="sxs-lookup"><span data-stu-id="c6a14-156">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c6a14-157">&quot;Учетные записи пользователей&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-157">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6a14-158">При отсутствии подключения к домену это называется &quot; учетными записями пользователей и семейной безопасностью &quot; .</span><span class="sxs-lookup"><span data-stu-id="c6a14-158">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c6a14-159">&quot;Учетные записи пользователей&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-159">&quot;User Accounts&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6a14-160">10</span><span class="sxs-lookup"><span data-stu-id="c6a14-160">10</span></span></td>
<td><span data-ttu-id="c6a14-161">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="c6a14-161">No longer used.</span></span> <span data-ttu-id="c6a14-162">Элементы, зарегистрированные в этой категории, отображаются в категории 5 (система и безопасность).</span><span class="sxs-lookup"><span data-stu-id="c6a14-162">Items registered in this category appear in category 5 (System and Security).</span></span></td>
<td><span data-ttu-id="c6a14-163">&quot;Безопасность&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-163">&quot;Security&quot;</span></span></td>
<td><span data-ttu-id="c6a14-164">&quot;Центр безопасности&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-164">&quot;Security Center&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6a14-165">Доступно только в Windows XP с пакетом обновления 2 (SP2) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c6a14-165">Available only in Windows XP Service Pack 2 (SP2) or later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a14-166">11</span><span class="sxs-lookup"><span data-stu-id="c6a14-166">11</span></span></td>
<td><span data-ttu-id="c6a14-167">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="c6a14-167">No longer used.</span></span> <span data-ttu-id="c6a14-168">Элементы, зарегистрированные в этой категории, отображаются в категории 0 (все элементы панели управления).</span><span class="sxs-lookup"><span data-stu-id="c6a14-168">Items registered in this category appear in category 0 (All Control Panel Items).</span></span></td>
<td><span data-ttu-id="c6a14-169">&quot;Мобильный ПК&quot;</span><span class="sxs-lookup"><span data-stu-id="c6a14-169">&quot;Mobile PC&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6a14-170">Эта категория отображается только на мобильных ПК.</span><span class="sxs-lookup"><span data-stu-id="c6a14-170">This category is only visible on mobile PCs.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c6a14-171">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c6a14-171">Not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c6a14-172">В Windows XP категории " **Установка и удаление программ** " и " **учетные записи пользователей** " работают несколько иначе из других категорий на панели управления.</span><span class="sxs-lookup"><span data-stu-id="c6a14-172">In Windows XP, the categories **Add or Remove Programs** and **User Accounts** work somewhat differently from other categories in Control Panel.</span></span> <span data-ttu-id="c6a14-173">Когда один или несколько элементов добавляются к одной из этих двух категорий, связанная ссылка в панели управления открывает страницу категории.</span><span class="sxs-lookup"><span data-stu-id="c6a14-173">When one or more items are added to one of these two categories, the associated link in Control Panel opens a category page.</span></span> <span data-ttu-id="c6a14-174">Зарегистрированные элементы отображаются в нижней части страницы под заголовком или выберите значок панели управления.</span><span class="sxs-lookup"><span data-stu-id="c6a14-174">The registered items appear in the lower portion of the page under the heading "or Pick a Control Panel icon".</span></span> <span data-ttu-id="c6a14-175">Если для одной из этих категорий не зарегистрирован ни один элемент, связанная ссылка в панели управления напрямую вызывает стандартный элемент Windows для этой категории.</span><span class="sxs-lookup"><span data-stu-id="c6a14-175">When no items are registered for one of these categories, the associated link in Control Panel directly invokes the standard Windows item for that category.</span></span> <span data-ttu-id="c6a14-176">В Windows Vista и более поздних версиях категории " **программы** " и " **учетные записи пользователей** " не имеют этого свойства.</span><span class="sxs-lookup"><span data-stu-id="c6a14-176">In Windows Vista and later, the **Programs** category and the **User Accounts** category do not have this property.</span></span>

<span data-ttu-id="c6a14-177">Категория **Центр безопасности** , доступная только в Windows XP с пакетом обновления 2 (SP2), также является довольно нестандартной.</span><span class="sxs-lookup"><span data-stu-id="c6a14-177">The **Security Center** category, available only in Windows XP SP2, is also somewhat non-standard.</span></span> <span data-ttu-id="c6a14-178">Если щелкнуть эту категорию, страница **центра безопасности** откроется в новом окне.</span><span class="sxs-lookup"><span data-stu-id="c6a14-178">Clicking this category opens the **Security Center** page in a new window.</span></span> <span data-ttu-id="c6a14-179">Элементы, зарегистрированные для **центра безопасности** , отображаются в нижней части этой страницы под заголовком **Управление параметрами безопасности для:**.</span><span class="sxs-lookup"><span data-stu-id="c6a14-179">Items registered for **Security Center** appear in the lower portion of that page under the heading **Manage security settings for:**.</span></span> <span data-ttu-id="c6a14-180">При щелчке значка открывается элемент панели управления.</span><span class="sxs-lookup"><span data-stu-id="c6a14-180">Clicking an icon opens the Control Panel item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6a14-181">См. также</span><span class="sxs-lookup"><span data-stu-id="c6a14-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a14-182">Элементы панели управления</span><span class="sxs-lookup"><span data-stu-id="c6a14-182">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="c6a14-183">Руководство по работе пользователей</span><span class="sxs-lookup"><span data-stu-id="c6a14-183">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="c6a14-184">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="c6a14-184">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c6a14-185">Использование Кплапплет</span><span class="sxs-lookup"><span data-stu-id="c6a14-185">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="c6a14-186">Обработка сообщений в панели управления</span><span class="sxs-lookup"><span data-stu-id="c6a14-186">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="c6a14-187">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="c6a14-187">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c6a14-188">Расширение элементов панели управления "система"</span><span class="sxs-lookup"><span data-stu-id="c6a14-188">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c6a14-189">Создание ссылок на задачи с возможностью поиска для элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="c6a14-189">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="c6a14-190">Доступ к панели управления в защищенном режиме в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6a14-190">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




