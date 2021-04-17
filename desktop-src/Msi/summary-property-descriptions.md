---
description: Сводные свойства для пакетов установки, преобразований и исправлений описаны в следующих таблицах.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Описания свойств сводки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674305"
---
# <a name="summary-property-descriptions"></a><span data-ttu-id="7da40-103">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="7da40-103">Summary Property Descriptions</span></span>

<span data-ttu-id="7da40-104">Сводные свойства для пакетов установки, преобразований и исправлений описаны в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="7da40-104">Summary properties for installation packages, transforms, and patches are described in the following tables.</span></span> <span data-ttu-id="7da40-105">Обратите внимание, что значение конкретного свойства сводки может отличаться в зависимости от того, принадлежит ли база данных к пакету установки, преобразованию или пакету исправлений.</span><span class="sxs-lookup"><span data-stu-id="7da40-105">Note that the meaning of a particular summary property can be different depending on whether the database belongs to an installation package, transform, or patch package.</span></span> <span data-ttu-id="7da40-106">Дополнительные сведения о кодах свойств, идентификаторах PID и типах см. в разделе [набор свойств потока сводных данных](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="7da40-106">For more information about the property IDs, PIDs, and types, see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

## <a name="installation-packages"></a><span data-ttu-id="7da40-107">Пакеты установки</span><span class="sxs-lookup"><span data-stu-id="7da40-107">Installation Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7da40-108">Свойство сводки</span><span class="sxs-lookup"><span data-stu-id="7da40-108">Summary property</span></span></th>
<th><span data-ttu-id="7da40-109">Значение этого свойства в базе данных установки</span><span class="sxs-lookup"><span data-stu-id="7da40-109">Meaning of this property in an Installation database</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7da40-110"><a href="title-summary.md"><strong>Заголовок</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-110"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="7da40-111">Описание этого файла в качестве установочного пакета.</span><span class="sxs-lookup"><span data-stu-id="7da40-111">A description of this file as an installation package.</span></span> <span data-ttu-id="7da40-112">Описание должно включать &quot; <a href="about-the-installer-database.md">базу данных установки</a>фразы.&quot;</span><span class="sxs-lookup"><span data-stu-id="7da40-112">The description should include the phrase &quot;<a href="about-the-installer-database.md">Installation Database</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-113"><a href="subject-summary.md"><strong>Субъект</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-113"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="7da40-114">Имя продукта, установленного этим пакетом.</span><span class="sxs-lookup"><span data-stu-id="7da40-114">The name of the product installed by this package.</span></span> <span data-ttu-id="7da40-115">Это должно быть то же имя, что и в свойстве <a href="productname.md"><strong>ProductName</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7da40-115">This should be the same name as in the <a href="productname.md"><strong>ProductName</strong></a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-116"><a href="author-summary.md"><strong>Автор</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-116"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="7da40-117">Название производителя этого продукта.</span><span class="sxs-lookup"><span data-stu-id="7da40-117">The name of the manufacturer of this product.</span></span> <span data-ttu-id="7da40-118">Это имя должно совпадать с именем в свойстве <a href="manufacturer.md"><strong>Manufacturer</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7da40-118">This should be the same name as in the <a href="manufacturer.md"><strong>Manufacturer</strong></a> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="7da40-120">Список ключевых слов, которые могут использоваться браузерами файлов для выполнения поиска по ключевым словам для файла.</span><span class="sxs-lookup"><span data-stu-id="7da40-120">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="7da40-121">Ключевые слова должны включать &quot; установщик &quot; , а также ключевые слова для конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="7da40-121">The keywords should include &quot;Installer&quot; as well as product-specific keywords.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-122"><a href="comments-summary.md"><strong>Комментарии</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-122"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="7da40-123">Содержит фразу: &quot; Эта база данных установщика содержит логику и данные, необходимые для установки <<em>Название продукта</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="7da40-123">Contains the phrase: &quot;This installer database contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-124"><a href="template-summary.md"><strong>Шаблон</strong></a> (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-124"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7da40-125">Платформа и языки, совместимые с этим пакетом установки.</span><span class="sxs-lookup"><span data-stu-id="7da40-125">The platform and languages compatible with this installation package.</span></span> <span data-ttu-id="7da40-126">Синтаксис см. в разделе <a href="template-summary.md"><strong>шаблон</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7da40-126">See <a href="template-summary.md"><strong>Template</strong></a> for syntax.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-127"><a href="last-saved-by-summary.md"><strong>Автор последнего сохранения</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-127"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="7da40-128">Разработчики средств редактирования баз данных могут использовать это свойство в процессе разработки, чтобы отслеживанию последнего пользователя для изменения базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="7da40-128">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="7da40-129">Это свойство должно иметь значение NULL в конечной базе данных доставки.</span><span class="sxs-lookup"><span data-stu-id="7da40-129">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="7da40-130">Установщик задает для этого свойства значение свойства <a href="logonuser.md"><strong>LogonUser</strong></a> во время <a href="administrative-installation.md"><strong>административной установки</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7da40-130">The installer sets this property to the value of the <a href="logonuser.md"><strong>LogonUser</strong></a> property during an <a href="administrative-installation.md"><strong>administrative installation</strong></a>.</span></span> <span data-ttu-id="7da40-131">Установщик никогда не использует это свойство, и пользователь не должен изменять его.</span><span class="sxs-lookup"><span data-stu-id="7da40-131">The installer never uses this property and a user never needs to modify it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-132"><a href="revision-number-summary.md"><strong>Номер редакции</strong></a> (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-132"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7da40-133">Содержит <a href="package-codes.md">код пакета</a> для пакета установщика.</span><span class="sxs-lookup"><span data-stu-id="7da40-133">Contains the <a href="package-codes.md">package code</a> for the installer package.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-134"><a href="last-printed-summary.md"><strong>Последняя печать</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-134"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="7da40-135">Может быть задана дата и время, когда <a href="administrative-installation.md">Административная установка</a> записывается при создании административного образа.</span><span class="sxs-lookup"><span data-stu-id="7da40-135">May be set to the date and time during an <a href="administrative-installation.md">administrative installation</a> to record when the administrative image was created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-136"><a href="create-time-date-summary.md"><strong>Создать дату и время</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-136"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="7da40-137">Дата и время создания базы данных установщика.</span><span class="sxs-lookup"><span data-stu-id="7da40-137">The time and date when this installer database was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-138"><a href="last-saved-time-date-summary.md"><strong>Время и Дата последнего сохранения</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-138"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="7da40-139">Текущее системное время и дата на момент последнего сохранения базы данных установщика.</span><span class="sxs-lookup"><span data-stu-id="7da40-139">The current system time and date at the time the installer database was last saved.</span></span> <span data-ttu-id="7da40-140">Изначально имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="7da40-140">Initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-141"><a href="page-count-summary.md"><strong>Число страниц</strong></a> (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-141"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7da40-142">Содержит значение, используемое для задания минимальной версии установщика, необходимой для данного пакета установки.</span><span class="sxs-lookup"><span data-stu-id="7da40-142">Contains a value used to identify the minimum installer version required by this installation package.</span></span> <span data-ttu-id="7da40-143">Например, если для пакета требуется по крайней мере версия 2,0 установщика, для этого свойства необходимо задать целое число 200.</span><span class="sxs-lookup"><span data-stu-id="7da40-143">For example, if the package requires at minimum the 2.0 version of the installer, this property should be set to an integer of 200.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7da40-144">Значение этого свойства должно быть 200 или выше с <a href="64-bit-windows-installer-packages.md">64-разрядными установщик Windows пакетами</a>.</span><span class="sxs-lookup"><span data-stu-id="7da40-144">The value of this property must be 200 or greater with <a href="64-bit-windows-installer-packages.md">64-bit Windows Installer Packages</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-145"><a href="word-count-summary.md"><strong>Число слов</strong></a> (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-145"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7da40-146">Тип образа исходного файла.</span><span class="sxs-lookup"><span data-stu-id="7da40-146">The type of the source file image.</span></span> <span data-ttu-id="7da40-147">Сохраняется вместо свойства стандартного счетчика.</span><span class="sxs-lookup"><span data-stu-id="7da40-147">Stored in place of the standard Count property.</span></span> <span data-ttu-id="7da40-148">Это свойство является битовым полем.</span><span class="sxs-lookup"><span data-stu-id="7da40-148">This property is a bit field.</span></span> <span data-ttu-id="7da40-149">Значения см. в разделе " <a href="word-count-summary.md"><strong>подсчет слов</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="7da40-149">See the <a href="word-count-summary.md"><strong>Word Count</strong></a> topic for the values.</span></span><br/> <span data-ttu-id="7da40-150">Начиная с версии установщик Windows 4,0 в Windows Vista, это свойство содержит биты, указывающие, требуются ли повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="7da40-150">Starting with Windows Installer version 4.0 on Windows Vista, this property includes bits to specify whether elevated privileges are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-151"><a href="character-count-summary.md"><strong>Число символов</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-151"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="7da40-152">NULL</span><span class="sxs-lookup"><span data-stu-id="7da40-152">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-153"><a href="creating-application-summary.md"><strong>Создание приложения</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-153"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="7da40-154">Содержит имя программного обеспечения, используемого для создания этой базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="7da40-154">Contains the name of the software used to author this installation database.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-155"><a href="security-summary.md"><strong>Безопасность</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-155"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="7da40-156">Значение этого свойства должно быть 2-рекомендуемым только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7da40-156">The value of this property should be 2 - Recommended read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-157"><a href="codepage-summary.md"><strong>Страница</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-157"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="7da40-158">Числовое значение кодовой страницы ANSI, используемой для вывода сводных данных.</span><span class="sxs-lookup"><span data-stu-id="7da40-158">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="7da40-159">Это свойство должно быть установлено до того, как в сводных данных будут заданы все свойства строк.</span><span class="sxs-lookup"><span data-stu-id="7da40-159">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a><span data-ttu-id="7da40-160">Преобразования</span><span class="sxs-lookup"><span data-stu-id="7da40-160">Transforms</span></span>



| <span data-ttu-id="7da40-161">Свойство сводки</span><span class="sxs-lookup"><span data-stu-id="7da40-161">Summary property</span></span>                                              | <span data-ttu-id="7da40-162">Значение этого свойства в преобразовании</span><span class="sxs-lookup"><span data-stu-id="7da40-162">Meaning of this property in a Transform</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7da40-163">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7da40-163">**Title**</span></span>](title-summary.md)                                | <span data-ttu-id="7da40-164">Описание этого файла в виде преобразования.</span><span class="sxs-lookup"><span data-stu-id="7da40-164">A description of this file as a transform.</span></span> <span data-ttu-id="7da40-165">Описание должно включать фразу "[Преобразование](database-transforms.md)".</span><span class="sxs-lookup"><span data-stu-id="7da40-165">The description should include the phrase: "[Transform](database-transforms.md)."</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="7da40-166">**Субъект**</span><span class="sxs-lookup"><span data-stu-id="7da40-166">**Subject**</span></span>](subject-summary.md)                            | <span data-ttu-id="7da40-167">Имя продукта, установленного исходным пакетом установки.</span><span class="sxs-lookup"><span data-stu-id="7da40-167">The name of the product installed by the original installation package.</span></span> <span data-ttu-id="7da40-168">Это должно быть то же значение, что и свойство [**сводки субъекта**](subject-summary.md) в исходном пакете установки.</span><span class="sxs-lookup"><span data-stu-id="7da40-168">This should be the same value as the [**Subject Summary**](subject-summary.md) property in the original installation package.</span></span>                                                                                            |
| [<span data-ttu-id="7da40-169">**Автор**</span><span class="sxs-lookup"><span data-stu-id="7da40-169">**Author**</span></span>](author-summary.md)                              | <span data-ttu-id="7da40-170">Имя производителя для этого преобразования.</span><span class="sxs-lookup"><span data-stu-id="7da40-170">The name of the manufacturer of this transform.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="7da40-171">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="7da40-171">**Keywords**</span></span>](keywords-summary.md)                          | <span data-ttu-id="7da40-172">Список ключевых слов, которые могут использоваться браузерами файлов для выполнения поиска по ключевым словам для файла.</span><span class="sxs-lookup"><span data-stu-id="7da40-172">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="7da40-173">Ключевые слова должны включать «Installer», а также ключевые слова для конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="7da40-173">The keywords should include "Installer" as well as product-specific keywords.</span></span>                                                                                                                             |
| [<span data-ttu-id="7da40-174">**Комментарии**</span><span class="sxs-lookup"><span data-stu-id="7da40-174">**Comments**</span></span>](comments-summary.md)                          | <span data-ttu-id="7da40-175">Содержит фразу: "это преобразование содержит логику и данные, необходимые для установки <*Название продукта*>".</span><span class="sxs-lookup"><span data-stu-id="7da40-175">Contains the phrase: "This transform contains the logic and data required to install <*product name*>."</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="7da40-176">[**Шаблон**](template-summary.md) (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-176">[**Template**](template-summary.md) (REQUIRED)</span></span>               | <span data-ttu-id="7da40-177">Версии платформы и языка, совместимые с этим преобразованием.</span><span class="sxs-lookup"><span data-stu-id="7da40-177">The platform and language versions compatible with this transform.</span></span> <span data-ttu-id="7da40-178">Если ограничений нет, это значение можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="7da40-178">This value may be left blank if there are no restrictions.</span></span> <span data-ttu-id="7da40-179">Для преобразования можно указать только один язык.</span><span class="sxs-lookup"><span data-stu-id="7da40-179">Only one language can be specified for a transform.</span></span> <span data-ttu-id="7da40-180">Дополнительные сведения о синтаксисе см. в разделе [**шаблон**](template-summary.md).</span><span class="sxs-lookup"><span data-stu-id="7da40-180">For more information about the syntax, see [**Template**](template-summary.md).</span></span>                                |
| [<span data-ttu-id="7da40-181">**Автор последнего сохранения**</span><span class="sxs-lookup"><span data-stu-id="7da40-181">**Last Saved By**</span></span>](last-saved-by-summary.md)                | <span data-ttu-id="7da40-182">ИДЕНТИФИКАТОРы платформы и языка, которые база данных имеет после преобразования.</span><span class="sxs-lookup"><span data-stu-id="7da40-182">The platform and language ID(s) that the database has after it has been transformed.</span></span> <span data-ttu-id="7da40-183">Свойству " [**Сводка" шаблона**](template-summary.md) в новой базе данных следует присвоить одинаковые значения.</span><span class="sxs-lookup"><span data-stu-id="7da40-183">The [**Template Summary**](template-summary.md) property in the new database should be set to the same values.</span></span>                                                                                              |
| <span data-ttu-id="7da40-184">[**Номер редакции**](revision-number-summary.md) (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-184">[**Revision Number**](revision-number-summary.md) (REQUIRED)</span></span> | <span data-ttu-id="7da40-185">Список идентификаторов GUID кода продукта и версию новых и исходных продуктов, а также идентификатор GUID кода обновления.</span><span class="sxs-lookup"><span data-stu-id="7da40-185">A list of the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="7da40-186">Список разделен точками с запятой, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7da40-186">The list is separated by semicolons as follows.</span></span> <span data-ttu-id="7da40-187">Исходный *продукт исходного кода — версия продукта*; *Новый код продукта новый — Product — Version*; *Обновление — код*</span><span class="sxs-lookup"><span data-stu-id="7da40-187">*Original-Product-Code Original-Product-Version*;*New-Product Code New-Product-Version*; *Upgrade-Code*</span></span><br/>                       |
| [<span data-ttu-id="7da40-188">**Последняя печать**</span><span class="sxs-lookup"><span data-stu-id="7da40-188">**Last Printed**</span></span>](last-printed-summary.md)                  | <span data-ttu-id="7da40-189">NULL</span><span class="sxs-lookup"><span data-stu-id="7da40-189">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7da40-190">**Создать дату и время**</span><span class="sxs-lookup"><span data-stu-id="7da40-190">**Create Time/Date**</span></span>](create-time-date-summary.md)          | <span data-ttu-id="7da40-191">Дата и время создания преобразования.</span><span class="sxs-lookup"><span data-stu-id="7da40-191">The time and date when the transform was created.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="7da40-192">**Время и Дата последнего сохранения**</span><span class="sxs-lookup"><span data-stu-id="7da40-192">**Last Saved Time/Date**</span></span>](last-saved-time-date-summary.md)  | <span data-ttu-id="7da40-193">Текущее системное время и дата на момент сохранения преобразования.</span><span class="sxs-lookup"><span data-stu-id="7da40-193">The current system time and date at the time the transform was saved.</span></span> <span data-ttu-id="7da40-194">Изначально имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="7da40-194">Initially null.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="7da40-195">[**Число страниц**](page-count-summary.md) (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-195">[**Page Count**](page-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="7da40-196">Значение, используемое для указания минимальной версии установщика, необходимой для обработки преобразования.</span><span class="sxs-lookup"><span data-stu-id="7da40-196">A value used to indicate the minimum installer version required to process the transform.</span></span> <span data-ttu-id="7da40-197">В качестве значения должно быть задано большее из двух значений свойств [**счетчика страниц**](page-count-summary.md) , принадлежащих базам данных, используемым для создания преобразования.</span><span class="sxs-lookup"><span data-stu-id="7da40-197">The value should be set to the greater of the two [**Page Count**](page-count-summary.md) property values that belong to the databases used to generate the transform.</span></span>                                 |
| <span data-ttu-id="7da40-198">[**Число слов**](word-count-summary.md) (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-198">[**Word Count**](word-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="7da40-199">NULL</span><span class="sxs-lookup"><span data-stu-id="7da40-199">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7da40-200">**Число символов**</span><span class="sxs-lookup"><span data-stu-id="7da40-200">**Character Count**</span></span>](character-count-summary.md)            | <span data-ttu-id="7da40-201">Эта часть информационного потока сводки делится на 2 16-разрядные слова.</span><span class="sxs-lookup"><span data-stu-id="7da40-201">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="7da40-202">Верхнее слово содержит [*Флаги проверки преобразования*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7da40-202">The upper word contains [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="7da40-203">В нижнем слове содержатся [*флаги состояния ошибки преобразования*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7da40-203">Lower word contains [*transform error condition flags*](t-gly.md).</span></span> |
| [<span data-ttu-id="7da40-204">**Создание приложения**</span><span class="sxs-lookup"><span data-stu-id="7da40-204">**Creating Application**</span></span>](creating-application-summary.md)  | <span data-ttu-id="7da40-205">Содержит имя программного обеспечения, используемого для создания этого преобразования.</span><span class="sxs-lookup"><span data-stu-id="7da40-205">Contains the name of the software used to create this transform.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7da40-206">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="7da40-206">**Security**</span></span>](security-summary.md)                          | <span data-ttu-id="7da40-207">Значение этого свойства должно быть 4-принудительно применено только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7da40-207">The value of this property should be 4 - Enforced read-only.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7da40-208">**Страница**</span><span class="sxs-lookup"><span data-stu-id="7da40-208">**Codepage**</span></span>](codepage-summary.md)                          | <span data-ttu-id="7da40-209">Числовое значение кодовой страницы ANSI, используемой для вывода сводных данных.</span><span class="sxs-lookup"><span data-stu-id="7da40-209">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="7da40-210">Это свойство должно быть установлено до того, как в сводных данных можно задать любые свойства строки.</span><span class="sxs-lookup"><span data-stu-id="7da40-210">This property must be set before any string properties can be set in the summary information.</span></span>                                                                                                                    |



 

## <a name="patch-packages"></a><span data-ttu-id="7da40-211">Пакеты исправлений</span><span class="sxs-lookup"><span data-stu-id="7da40-211">Patch Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7da40-212">Свойство сводки</span><span class="sxs-lookup"><span data-stu-id="7da40-212">Summary property</span></span></th>
<th><span data-ttu-id="7da40-213">Значение этого свойства в пакете исправлений</span><span class="sxs-lookup"><span data-stu-id="7da40-213">Meaning of this property in a Patch package</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7da40-214"><a href="title-summary.md"><strong>Заголовок</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-214"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="7da40-215">Описание этого файла в виде пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="7da40-215">A description of this file as a patch package.</span></span> <span data-ttu-id="7da40-216">Описание должно включать фразу: &quot; <a href="patch-packages.md">Patch</a>.&quot;</span><span class="sxs-lookup"><span data-stu-id="7da40-216">The description should include the phrase: &quot;<a href="patch-packages.md">Patch</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-217"><a href="subject-summary.md"><strong>Субъект</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-217"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="7da40-218">Описание исправления, которое содержит имя продукта.</span><span class="sxs-lookup"><span data-stu-id="7da40-218">A description of the patch that includes the name of the product.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-219"><a href="author-summary.md"><strong>Автор</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-219"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="7da40-220">Имя производителя пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="7da40-220">The name of the manufacturer of the patch package.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="7da40-222">Разделенный точками с запятой список источников исправления.</span><span class="sxs-lookup"><span data-stu-id="7da40-222">A semicolon delimited list of sources of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-223"><a href="comments-summary.md"><strong>Комментарии</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-223"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="7da40-224">Содержит фразу: &quot; это исправление содержит логику и данные, необходимые для установки <<em>Название продукта</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="7da40-224">Contains the phrase: &quot;This patch contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-225"><a href="template-summary.md"><strong>Шаблон</strong></a> (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-225"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7da40-226">Разделенный точками с запятой список кодов продуктов, которые могут принять это исправление.</span><span class="sxs-lookup"><span data-stu-id="7da40-226">A semicolon delimited list of the product codes that can accept this patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-227"><a href="last-saved-by-summary.md"><strong>Автор последнего сохранения</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-227"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="7da40-228">Разделенный точками с запятой список преобразований имен подхранилищ в том порядке, в котором они применяются этим исправлением.</span><span class="sxs-lookup"><span data-stu-id="7da40-228">A semicolon delimited list of transform substorage names in the order they are applied by this patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-229"><a href="revision-number-summary.md"><strong>Номер редакции</strong></a> (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-229"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7da40-230">Содержит код исправления GUID для исправления.</span><span class="sxs-lookup"><span data-stu-id="7da40-230">Contains the GUID patch code for the patch.</span></span> <span data-ttu-id="7da40-231">За этим может следовать список идентификаторов GUID кода исправления для исправлений, которые удаляются при применении этого исправления.</span><span class="sxs-lookup"><span data-stu-id="7da40-231">This may be followed by a list of patch code GUIDs for patches that are removed when this patch is applied.</span></span> <span data-ttu-id="7da40-232">Коды исправлений объединяются без разделителей, разделяющих идентификаторы GUID в списке.</span><span class="sxs-lookup"><span data-stu-id="7da40-232">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7da40-233">Если пакет исправлений содержит таблицу <a href="msipatchsequence-table.md"><strong>мсипатчсекуенце</strong></a> , это исправление не удаляет исправления, перечисленные после идентификатора GUID текущего исправления.</span><span class="sxs-lookup"><span data-stu-id="7da40-233">If the patch package contains a <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> table, the patch does not remove patches listed after the current patch's GUID.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-234"><a href="last-printed-summary.md"><strong>Последняя печать</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-234"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="7da40-235">NULL</span><span class="sxs-lookup"><span data-stu-id="7da40-235">Null</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-236"><a href="create-time-date-summary.md"><strong>Создать дату и время</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-236"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="7da40-237">Дата и время создания файла исправления.</span><span class="sxs-lookup"><span data-stu-id="7da40-237">The time and date when patch file was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-238"><a href="last-saved-time-date-summary.md"><strong>Время и Дата последнего сохранения</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-238"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="7da40-239">Текущее системное время и дата на момент сохранения пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="7da40-239">The current system time and date at the time the patch package was saved.</span></span> <span data-ttu-id="7da40-240">Это значение изначально равно null.</span><span class="sxs-lookup"><span data-stu-id="7da40-240">This value is initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-241"><a href="page-count-summary.md"><strong>Число страниц</strong></a> (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-241"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7da40-242">NULL</span><span class="sxs-lookup"><span data-stu-id="7da40-242">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-243"><a href="word-count-summary.md"><strong>Число слов</strong></a> (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7da40-243"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7da40-244">Содержит значение, указывающее минимальную версию установщик Windows, необходимую для установки исправления.</span><span class="sxs-lookup"><span data-stu-id="7da40-244">Contains a value that indicates the minimum Windows Installer version that is required to install the patch.</span></span> <span data-ttu-id="7da40-245">Для установки исправления с числом слов, равным 4, требуется установщик Windows версии 3,0 или выше.</span><span class="sxs-lookup"><span data-stu-id="7da40-245">A patch with a word count value of 4 requires Windows Installer version 3.0 or higher for the patch to be applied.</span></span> <span data-ttu-id="7da40-246">Значение 3 указывает, что требуется установщик Windows версии 2,0 или выше.</span><span class="sxs-lookup"><span data-stu-id="7da40-246">A value of 3 indicates that Windows Installer version 2.0 or higher is required.</span></span> <span data-ttu-id="7da40-247">Значение 2 указывает, что требуется установщик Windows версии 1,2 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7da40-247">A value of 2 indicates that Windows Installer version 1.2 or higher is required.</span></span> <span data-ttu-id="7da40-248">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="7da40-248">The default value is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-249"><a href="character-count-summary.md"><strong>Число символов</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-249"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="7da40-250">NULL</span><span class="sxs-lookup"><span data-stu-id="7da40-250">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-251"><a href="creating-application-summary.md"><strong>Создание приложения</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-251"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="7da40-252">Имя программного обеспечения, используемого для создания исправления.</span><span class="sxs-lookup"><span data-stu-id="7da40-252">The name of the software used to create the patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7da40-253"><a href="security-summary.md"><strong>Безопасность</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-253"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="7da40-254">Значение этого свойства должно быть 4-принудительно применено только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7da40-254">The value of this property should be 4 - Enforced read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7da40-255"><a href="codepage-summary.md"><strong>Страница</strong></a></span><span class="sxs-lookup"><span data-stu-id="7da40-255"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="7da40-256">Числовое значение кодовой страницы ANSI, используемой для вывода сводных данных.</span><span class="sxs-lookup"><span data-stu-id="7da40-256">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="7da40-257">Это свойство должно быть установлено до того, как в сводных данных будут заданы все свойства строк.</span><span class="sxs-lookup"><span data-stu-id="7da40-257">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




