---
description: Изменения сортировки NLS
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Изменения сортировки NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57cfaf2a9891c2d952637429786729670fc103c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088062"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="b9b72-103">Изменения сортировки NLS</span><span class="sxs-lookup"><span data-stu-id="b9b72-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="b9b72-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="b9b72-104">Affected Platforms</span></span>

 <span data-ttu-id="b9b72-105">**Клиенты** — Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9b72-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="b9b72-106">**Серверы** — windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9b72-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="b9b72-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="b9b72-107">Feature Impact</span></span>

 <span data-ttu-id="b9b72-108">**Серьезность** — высокая</span><span class="sxs-lookup"><span data-stu-id="b9b72-108">**Severity** - High</span></span>  
<span data-ttu-id="b9b72-109">**Частота** — низкая (несколько приложений затронули, но если они затронуты, всегда нарушены)</span><span class="sxs-lookup"><span data-stu-id="b9b72-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="b9b72-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b9b72-110">Description</span></span>

<span data-ttu-id="b9b72-111">Функции поддержки национальных языков (NLS) помогают приложениям поддерживать различные потребности пользователей в разных языковых и национальных настройках.</span><span class="sxs-lookup"><span data-stu-id="b9b72-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="b9b72-112">Новые версии Windows почти неизменно включают изменения NLS.</span><span class="sxs-lookup"><span data-stu-id="b9b72-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="b9b72-113">Это изменение влияет на параметры сортировки и сортировки, поэтому приложения с постоянными индексами.</span><span class="sxs-lookup"><span data-stu-id="b9b72-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="b9b72-114">Таблица параметров сортировки имеет два числа, которые определяют версию (редакция): определенную версию и версию NLS.</span><span class="sxs-lookup"><span data-stu-id="b9b72-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="b9b72-115">Обе версии имеют значения DWORD, состоящие из основной версии и дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="b9b72-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="b9b72-116">Первый байт значения зарезервирован, два следующих байта представляют основной номер версии, а последний байт представляет дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="b9b72-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="b9b72-117">В шестнадцатеричных терминах используется шаблон 0xRRMMMMmm, где R равно reserved, M равно Major, а m равно Minor.</span><span class="sxs-lookup"><span data-stu-id="b9b72-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="b9b72-118">Например, основная версия 3 с дополнительной версией 4 представлена как 0x304.</span><span class="sxs-lookup"><span data-stu-id="b9b72-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="b9b72-119">Для основной версии одна или несколько кодовых точек меняются, поэтому приложению необходимо повторно индексировать все данные, чтобы они были допустимыми.</span><span class="sxs-lookup"><span data-stu-id="b9b72-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="b9b72-120">Для дополнительной версии ничего не перемещается, но добавляются кодовые точки.</span><span class="sxs-lookup"><span data-stu-id="b9b72-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="b9b72-121">Для этого типа версии приложению необходимо только повторно индексировать строки с ранее несортированными значениями.</span><span class="sxs-lookup"><span data-stu-id="b9b72-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="b9b72-122">Ниже приведены сведения о том, что означают номера версий в связи с изменением данных в таблицах исключений, зависящих от языкового стандарта, и в таблицах по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="b9b72-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="b9b72-123">**Нлсверсион Major** — измененные кодовые точки в "Exception" или таблицах, зависящих от локали</span><span class="sxs-lookup"><span data-stu-id="b9b72-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="b9b72-124">**Нлсверсион Minor** — добавлены новые позиции кода в таблицах "Exception" или "зависящие от языкового стандарта".</span><span class="sxs-lookup"><span data-stu-id="b9b72-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="b9b72-125">**Дефинедверсион основной** — измененные кодовые точки в таблице по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b9b72-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="b9b72-126">**Дефинедверсион Minor** — добавлены новые кодовые точки в таблицу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9b72-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="b9b72-127">**Сортировка номеров версий для выпущенных версий:**</span><span class="sxs-lookup"><span data-stu-id="b9b72-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="b9b72-128">Операционная система</span><span class="sxs-lookup"><span data-stu-id="b9b72-128">Operating System</span></span>    | <span data-ttu-id="b9b72-129">Release</span><span class="sxs-lookup"><span data-stu-id="b9b72-129">Release</span></span>           | <span data-ttu-id="b9b72-130">Версия (0xRRMMMMmm)</span><span class="sxs-lookup"><span data-stu-id="b9b72-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="b9b72-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b9b72-131">Windows XP</span></span>          | <span data-ttu-id="b9b72-132">RTM/SP1/SP2/SP3/...</span><span class="sxs-lookup"><span data-stu-id="b9b72-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="b9b72-133">Н/д — нет API Жетнлсверсион ()</span><span class="sxs-lookup"><span data-stu-id="b9b72-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="b9b72-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9b72-134">Windows Server 2003</span></span> | <span data-ttu-id="b9b72-135">RTM И SP1</span><span class="sxs-lookup"><span data-stu-id="b9b72-135">RTM/SP1</span></span>           | <span data-ttu-id="b9b72-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="b9b72-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="b9b72-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9b72-137">Windows Vista</span></span>       | <span data-ttu-id="b9b72-138">RTM И SP1</span><span class="sxs-lookup"><span data-stu-id="b9b72-138">RTM/SP1</span></span>           | <span data-ttu-id="b9b72-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="b9b72-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="b9b72-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9b72-140">Windows Server 2008</span></span> | <span data-ttu-id="b9b72-141">RTM</span><span class="sxs-lookup"><span data-stu-id="b9b72-141">RTM</span></span>               | <span data-ttu-id="b9b72-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="b9b72-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="b9b72-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9b72-143">Windows 7</span></span>           | <span data-ttu-id="b9b72-144">RTM</span><span class="sxs-lookup"><span data-stu-id="b9b72-144">RTM</span></span>               | <span data-ttu-id="b9b72-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="b9b72-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="b9b72-146">Проявление</span><span class="sxs-lookup"><span data-stu-id="b9b72-146">Manifestation</span></span>

<span data-ttu-id="b9b72-147">Приложения (например, базы данных) с постоянными индексами, которые не проверяют версию NLS и повторно индексируются при изменении версии, не смогут правильно выполнить сортировку или выдать запрошенные результаты.</span><span class="sxs-lookup"><span data-stu-id="b9b72-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="b9b72-148">В случае пользовательских интерфейсов списки (например, буквы, цифры, буквы, символы и т. д.) могут быть неправильно отсортированы.</span><span class="sxs-lookup"><span data-stu-id="b9b72-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="b9b72-149">Решение</span><span class="sxs-lookup"><span data-stu-id="b9b72-149">Solution</span></span>

<span data-ttu-id="b9b72-150">Приложение может вызывать либо **жетнлсверсионекс** (Windows Vista, либо более поздней версии), либо **Жетнлсверсион** (до Windows Vista), чтобы получить определенную версию и версию NLS для таблицы параметров сортировки.</span><span class="sxs-lookup"><span data-stu-id="b9b72-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="b9b72-151">Жетнлсверсионекс:</span><span class="sxs-lookup"><span data-stu-id="b9b72-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="b9b72-152">*Извлекает сведения о текущей версии указанной возможности NLS для языкового стандарта, указанного по имени*</span><span class="sxs-lookup"><span data-stu-id="b9b72-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="b9b72-153">Эта функция позволяет приложению, например Active Directory, определить, влияет ли изменение NLS на языковой стандарт, используемый для конкретной таблицы индексов.</span><span class="sxs-lookup"><span data-stu-id="b9b72-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="b9b72-154">В противном случае нет необходимости повторно индексировать таблицу.</span><span class="sxs-lookup"><span data-stu-id="b9b72-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="b9b72-155">Дополнительные сведения см. в разделе Обработка языковых стандартов и сведений о языке.</span><span class="sxs-lookup"><span data-stu-id="b9b72-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="b9b72-156">Эта функция поддерживает пользовательские языковые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b9b72-156">This function supports custom locales.</span></span> <span data-ttu-id="b9b72-157">Если *лплокаленаме* указывает дополнительный языковой стандарт, полученные данные представляют собой правильные данные для порядка сортировки, связанного с дополнительным языковым стандартом.</span><span class="sxs-lookup"><span data-stu-id="b9b72-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="b9b72-158">**Примечание.** Версии Windows до Windows Vista не поддерживают **жетнлсверсионекс**.</span><span class="sxs-lookup"><span data-stu-id="b9b72-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="b9b72-159">Жетнлсверсион (используется для приложений, работающих в версиях Windows, предшествовавших Windows Vista):</span><span class="sxs-lookup"><span data-stu-id="b9b72-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="b9b72-160">*Извлекает сведения о текущей версии указанной возможности NLS для языкового стандарта, заданного идентификатором*</span><span class="sxs-lookup"><span data-stu-id="b9b72-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="b9b72-161">Эта функция позволяет приложению, например Active Directory, определить, влияет ли изменение NLS на идентификатор локали, используемый для конкретной таблицы индексов.</span><span class="sxs-lookup"><span data-stu-id="b9b72-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="b9b72-162">В противном случае нет необходимости повторно индексировать таблицу.</span><span class="sxs-lookup"><span data-stu-id="b9b72-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="b9b72-163">Дополнительные сведения см. в разделе Обработка языковых стандартов и сведений о языке.</span><span class="sxs-lookup"><span data-stu-id="b9b72-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="b9b72-164">**Примечание.** Эта функция получает сведения только о языковом стандарте, заданном идентификатором.</span><span class="sxs-lookup"><span data-stu-id="b9b72-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="b9b72-165">Функция **жетнлсверсионекс** поддерживает дополнительные языковые стандарты, функции и имена RFC 4646.</span><span class="sxs-lookup"><span data-stu-id="b9b72-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="b9b72-166">Однако версии Windows до Windows Vista не поддерживают **жетнлсверсионекс**.</span><span class="sxs-lookup"><span data-stu-id="b9b72-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="b9b72-167">Приложения, предназначенные для работы только в Windows Vista и более поздних версиях, должны использовать **жетнлсверсионекс** в качестве предпочтений этой функции.</span><span class="sxs-lookup"><span data-stu-id="b9b72-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="b9b72-168">**Жетнлсверсионекс** обеспечивает хорошую поддержку дополнительных языковых стандартов.</span><span class="sxs-lookup"><span data-stu-id="b9b72-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="b9b72-169">Тест совместимости</span><span class="sxs-lookup"><span data-stu-id="b9b72-169">Compatibility Test</span></span>

<span data-ttu-id="b9b72-170">**Пошаговые инструкции по изменению версии параметров сортировки (то есть необходимости повторного индексирования):**</span><span class="sxs-lookup"><span data-stu-id="b9b72-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="b9b72-171">**Используйте жетнлсверсионекс ()** для получения структуры **нлсверсионинфоекс** при выполнении исходной индексации данных.</span><span class="sxs-lookup"><span data-stu-id="b9b72-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="b9b72-172">Сохраните следующие свойства с индексом, чтобы определить версию:  **нлсверсионинфоекс. двнлсверсион** и **нлсверсионинфоекс. двдефинедверсион** — эти два свойства вместе указывают версию таблицы сортировки, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="b9b72-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="b9b72-173">**Нлсверсионинфоекс. двеффективеид** — указывает действующий языковой стандарт для сортировки.</span><span class="sxs-lookup"><span data-stu-id="b9b72-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="b9b72-174">Пользовательский языковой стандарт будет указывать на сортировку в встроенном языковом стандарте.</span><span class="sxs-lookup"><span data-stu-id="b9b72-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="b9b72-175">При использовании индекса используйте **жетнлсверсионекс ()** для обнаружения версии данных.</span><span class="sxs-lookup"><span data-stu-id="b9b72-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="b9b72-176">Если какое-либо из трех свойств было изменено, то используемые данные сортировки могут возвращать разные результаты, а любое индексирование может не найти записи.</span><span class="sxs-lookup"><span data-stu-id="b9b72-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="b9b72-177">Если известно, что данные не содержат недопустимые кодовые точки Юникода (т. е. все строки возвращали **значение true** из вызова **иснлсдефинедстринг ()**), вы можете считать их одинаковыми, если изменился только младший байт **двнлсверсион** и **двдефинедверсион** (дополнительные версии, описанные выше).</span><span class="sxs-lookup"><span data-stu-id="b9b72-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="b9b72-178">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="b9b72-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="b9b72-179">Интернационализация для приложений Windows</span><span class="sxs-lookup"><span data-stu-id="b9b72-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="b9b72-180">Функция Жетнлсверсионекс</span><span class="sxs-lookup"><span data-stu-id="b9b72-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="b9b72-181">Функция Жетнлсверсион</span><span class="sxs-lookup"><span data-stu-id="b9b72-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="b9b72-182">Как определить, изменилась ли версия параметров сортировки</span><span class="sxs-lookup"><span data-stu-id="b9b72-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 
