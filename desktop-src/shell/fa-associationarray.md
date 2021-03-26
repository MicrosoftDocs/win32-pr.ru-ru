---
description: Массив ассоциаций — это упорядоченный список расположений в реестре, который используется для хранения сведений о типе элемента, включая обработчики, глаголы и другие атрибуты, такие как значок и отображаемое имя типа.
title: Массивы ассоциаций
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144608"
---
# <a name="association-arrays"></a><span data-ttu-id="c64e0-103">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="c64e0-103">Association Arrays</span></span>

<span data-ttu-id="c64e0-104">Массив ассоциаций — это упорядоченный список расположений в реестре, который используется для хранения сведений о типе элемента, включая обработчики, глаголы и другие атрибуты, такие как значок и отображаемое имя типа.</span><span class="sxs-lookup"><span data-stu-id="c64e0-104">An association array is an ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="c64e0-105">Оболочка использует массивы ассоциаций для запроса предопределенного набора расположений реестра, которые могут содержать сведения об элементе оболочки.</span><span class="sxs-lookup"><span data-stu-id="c64e0-105">The Shell uses association arrays to query a predefined set of registry locations that might contain information about a Shell item.</span></span>

<span data-ttu-id="c64e0-106">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c64e0-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c64e0-107">Сведения о массивах ассоциаций</span><span class="sxs-lookup"><span data-stu-id="c64e0-107">About Association Arrays</span></span>](#about-association-arrays)
-   [<span data-ttu-id="c64e0-108">Запрос массивов ассоциаций</span><span class="sxs-lookup"><span data-stu-id="c64e0-108">Querying Association Arrays</span></span>](#querying-association-arrays)
-   [<span data-ttu-id="c64e0-109">Работа с массивами ассоциаций для конкретного источника данных оболочки</span><span class="sxs-lookup"><span data-stu-id="c64e0-109">Working with Association Arrays for a Particular Shell Data Source</span></span>](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [<span data-ttu-id="c64e0-110">Массивы ассоциаций источников данных оболочки</span><span class="sxs-lookup"><span data-stu-id="c64e0-110">Shell Data Source Association Arrays</span></span>](#shell-data-source-association-arrays)
-   [<span data-ttu-id="c64e0-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c64e0-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="c64e0-112">См. также</span><span class="sxs-lookup"><span data-stu-id="c64e0-112">Related topics</span></span>](#related-topics)

## <a name="about-association-arrays"></a><span data-ttu-id="c64e0-113">Сведения о массивах ассоциаций</span><span class="sxs-lookup"><span data-stu-id="c64e0-113">About Association Arrays</span></span>

<span data-ttu-id="c64e0-114">Массив ассоциаций — это упорядоченный список расположений реестра, содержащих сведения о типе элемента, включая обработчики, команды и другие атрибуты, такие как значок и отображаемое имя типа.</span><span class="sxs-lookup"><span data-stu-id="c64e0-114">An association array is an ordered list of registry locations that contain information about an item type, including handlers, verbs, and other attributes such as the icon and display name of the type.</span></span> <span data-ttu-id="c64e0-115">Эти сведения о типе элемента могут быть зарегистрированы на различных уровнях квалификации.</span><span class="sxs-lookup"><span data-stu-id="c64e0-115">This information about the item type can be registered at varying levels of specificity.</span></span> <span data-ttu-id="c64e0-116">Например, можно зарегистрировать команду, которая будет отображаться только для определенного типа файлов (например, JPG) или для всех элементов с одинаковой системой. Kind (например, System. Kind = Picture) или для всех элементов.</span><span class="sxs-lookup"><span data-stu-id="c64e0-116">For example, you can register a verb that will show up only for a specific file type (such as .jpg), or for all items with the same System.Kind (for example, System.kind = picture), or for all items.</span></span>

<span data-ttu-id="c64e0-117">Оболочка использует массивы ассоциаций для запроса предопределенного набора расположений реестра, которые потенциально могут содержать сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="c64e0-117">The Shell uses association arrays to query a predefined set of registry locations that might potentially contain information about the item.</span></span> <span data-ttu-id="c64e0-118">Интерфейсы API массива взаимосвязей можно использовать для извлечения из подраздела реестра одного значения, которое содержит запрашиваемую информацию, с этим значением, которое поступает из первой записи в массиве, который его предоставляет.</span><span class="sxs-lookup"><span data-stu-id="c64e0-118">The association array APIs can be used to retrieve from the registry subkey a single value that contains the requested information, with that value coming from the first entry in the array that provides it.</span></span> <span data-ttu-id="c64e0-119">Например, значение значка по умолчанию извлекается таким образом.</span><span class="sxs-lookup"><span data-stu-id="c64e0-119">For example, the default icon value is retrieved this way.</span></span> <span data-ttu-id="c64e0-120">Массив ассоциаций можно также использовать для получения набора значений, которые хранятся в подразделах реестра.</span><span class="sxs-lookup"><span data-stu-id="c64e0-120">The association array can also be used to retrieve a set of values that are stored in the registry subkeys.</span></span> <span data-ttu-id="c64e0-121">Например, список команд строится на основе этих команд, зарегистрированных во всех подразделах.</span><span class="sxs-lookup"><span data-stu-id="c64e0-121">For example, the list of verbs is built from those verbs that are registered under all the subkeys.</span></span>

<span data-ttu-id="c64e0-122">После того как оболочка запрашивает для сведений об элементе оболочки предопределенный набор расположений реестра, он помещает их в массив в порядке от наиболее конкретного расположения к наиболее общему.</span><span class="sxs-lookup"><span data-stu-id="c64e0-122">After the Shell queries a predefined set of registry locations for information about a Shell item, it puts the registry locations into an array in order from the most specific location to the most general.</span></span>

<span data-ttu-id="c64e0-123">Поскольку массивы ассоциаций являются упорядоченными списками, они предоставляют разработчикам приложений механизм для добавления в реестр сведений, которые будут возвращаться для определенного типа элемента.</span><span class="sxs-lookup"><span data-stu-id="c64e0-123">Because association arrays are ordered lists, they provide application developers with a mechanism for adding information to the registry that will be returned for a specific type of item.</span></span> <span data-ttu-id="c64e0-124">Аналогичным образом, массивы ассоциаций позволяют разработчикам приложений добавлять сведения в реестр для определенной группы элементов, когда эти элементы регистрируются в более общем расположении.</span><span class="sxs-lookup"><span data-stu-id="c64e0-124">Likewise, association arrays permit application developers to add information to the registry for a specific group of items when those items are registered at a more general location.</span></span> <span data-ttu-id="c64e0-125">Эта логика информирует ваше решение о наиболее подходящем расположении в реестре для хранения сведений об элементах оболочки.</span><span class="sxs-lookup"><span data-stu-id="c64e0-125">This logic informs your decision about the most appropriate location in the registry to store information about Shell items.</span></span>

<span data-ttu-id="c64e0-126">В системе Windows по умолчанию JPG-файл имеет следующий массив ассоциаций:</span><span class="sxs-lookup"><span data-stu-id="c64e0-126">On a default Windows system a .jpg file has the following association array:</span></span>

-   <span data-ttu-id="c64e0-127">**HKey \_ \_Корневые** \\ **жпгфиле** классов</span><span class="sxs-lookup"><span data-stu-id="c64e0-127">**HKEY\_CLASSES\_ROOT**\\**jpgfile**</span></span>
-   <span data-ttu-id="c64e0-128">**HKey \_ \_Корневые классы** \\ **системфилеассоЦиатионс** \\ **. jpg**</span><span class="sxs-lookup"><span data-stu-id="c64e0-128">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.jpg**</span></span>
-   <span data-ttu-id="c64e0-129">**HKey \_ \_Корневой** \\ **образ** классов</span><span class="sxs-lookup"><span data-stu-id="c64e0-129">**HKEY\_CLASSES\_ROOT**\\**image**</span></span>
-   <span data-ttu-id="c64e0-130">**HKey \_ \_корневой класс классов** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="c64e0-130">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="c64e0-131">_ *\_ Классы hKey \_ root **\\** аллфилесистемобжектс*\*</span><span class="sxs-lookup"><span data-stu-id="c64e0-131">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>

<span data-ttu-id="c64e0-132">Сведения о регистрации массивов ассоциаций см. в разделе [Регистрация приложения](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="c64e0-132">For information on registering association arrays, see [Application Registration](app-registration.md).</span></span>

## <a name="querying-association-arrays"></a><span data-ttu-id="c64e0-133">Запрос массивов ассоциаций</span><span class="sxs-lookup"><span data-stu-id="c64e0-133">Querying Association Arrays</span></span>

<span data-ttu-id="c64e0-134">Существуют API-интерфейсы оболочки для получения сведений из диапазона подразделов реестра, от самого конкретного подраздела реестра до надмножество данных во всех подразделах реестра.</span><span class="sxs-lookup"><span data-stu-id="c64e0-134">There are Shell APIs to retrieve information from a range of registry subkeys, from the most specific registry subkey to a superset of the information across all registry subkeys.</span></span>

<span data-ttu-id="c64e0-135">Чаще всего массив ассоциаций используется для запроса одного значения, которое оболочка возвращает из наиболее конкретного элемента в массиве, имеющего запрашиваемую информацию.</span><span class="sxs-lookup"><span data-stu-id="c64e0-135">The most common use of an association array is to query for a single value that the Shell returns from the most specific element in the array that has the requested information.</span></span> <span data-ttu-id="c64e0-136">В следующем примере кода показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="c64e0-136">The following code example shows how to do that.</span></span>


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



<span data-ttu-id="c64e0-137">Следующие API можно использовать для запроса массива ассоциаций или для создания объекта [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) Array, к которому можно выполнить запрос:</span><span class="sxs-lookup"><span data-stu-id="c64e0-137">The following APIs can be used to query an association array or to construct an association array [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) object that can be queried:</span></span>

-   <span data-ttu-id="c64e0-138">[**Ассоккреате**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (до Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="c64e0-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prior to Windows Vista)</span></span>
-   [<span data-ttu-id="c64e0-139">**ассоккреатефорклассес**</span><span class="sxs-lookup"><span data-stu-id="c64e0-139">**AssocCreateForClasses**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [<span data-ttu-id="c64e0-140">**ассоккуеристринг**</span><span class="sxs-lookup"><span data-stu-id="c64e0-140">**AssocQueryString**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a><span data-ttu-id="c64e0-141">Работа с массивами ассоциаций для конкретного источника данных оболочки</span><span class="sxs-lookup"><span data-stu-id="c64e0-141">Working with Association Arrays for a Particular Shell Data Source</span></span>

<span data-ttu-id="c64e0-142">Каждый источник данных оболочки определяет массив ассоциаций для своих элементов.</span><span class="sxs-lookup"><span data-stu-id="c64e0-142">Each Shell data source defines the association array for its items.</span></span> <span data-ttu-id="c64e0-143">Определение массива ассоциаций обычно является функцией типа Item.</span><span class="sxs-lookup"><span data-stu-id="c64e0-143">Defining an association array is usually a function of the type of item.</span></span> <span data-ttu-id="c64e0-144">Разработчики источников данных оболочки должны определять и документировать массивы взаимосвязей, чтобы позволить приложениям расширять поведение этих типов, например для регистрации команд или другой информации.</span><span class="sxs-lookup"><span data-stu-id="c64e0-144">Shell data source implementers should define and document the association arrays to enable applications to extend the behavior of those types, such as for registering verbs or other information.</span></span> <span data-ttu-id="c64e0-145">Приложения могут расширять поведение элементов на основе добавления данных в подразделы массива взаимосвязей, например добавление глаголов для элементов.</span><span class="sxs-lookup"><span data-stu-id="c64e0-145">Applications can extend the behavior of items based on adding data to the association array subkeys, such as adding verbs for items.</span></span>

<span data-ttu-id="c64e0-146">Источник данных файловой системы создает массив ассоциаций для файлов на основе следующих подразделов реестра и специальных идентификаторов ProgID:</span><span class="sxs-lookup"><span data-stu-id="c64e0-146">The file system data source builds an association array for files based on the following registry subkeys and special ProgIDs:</span></span>

-   <span data-ttu-id="c64e0-147">Если файл имеет зарегистрированный ProgID, используется **\_ \_ корневой** \\ *идентификатор ProgID* для классов hKey.</span><span class="sxs-lookup"><span data-stu-id="c64e0-147">If the file has a registered ProgID, **HKEY\_CLASSES\_ROOT**\\*ProgID* is used.</span></span> <span data-ttu-id="c64e0-148">В противном случае используется **\_ \_ корень классов hKey** \\ **Unknown** .</span><span class="sxs-lookup"><span data-stu-id="c64e0-148">Otherwise **HKEY\_CLASSES\_ROOT**\\**Unknown** is used.</span></span>
-   <span data-ttu-id="c64e0-149">Расширение имени файла регистрируется в подразделе " **\_ классы hKey \_ root** \\ **системфилеассоЦиатионс** \\ *. fileExtension* ".</span><span class="sxs-lookup"><span data-stu-id="c64e0-149">The file name extension is registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ *.fileExtension* subkey.</span></span>
-   <span data-ttu-id="c64e0-150">В следующей таблице показаны специальные идентификаторы ProgID.</span><span class="sxs-lookup"><span data-stu-id="c64e0-150">Special ProgIDs are shown in the following table.</span></span> 

    | <span data-ttu-id="c64e0-151">Специальный идентификатор progID</span><span class="sxs-lookup"><span data-stu-id="c64e0-151">Special progID</span></span>                                    | <span data-ttu-id="c64e0-152">Описание</span><span class="sxs-lookup"><span data-stu-id="c64e0-152">Description</span></span>                   |
    |---------------------------------------------------|-------------------------------|
    | <span data-ttu-id="c64e0-153">**HKey \_ \_корневой класс классов** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="c64e0-153">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>                   | <span data-ttu-id="c64e0-154">Все файлы (не папки)</span><span class="sxs-lookup"><span data-stu-id="c64e0-154">All files (non-folders)</span></span>       |
    | <span data-ttu-id="c64e0-155">_ *\_ Классы hKey \_ root **\\** аллфилесистемобжектс*\*</span><span class="sxs-lookup"><span data-stu-id="c64e0-155">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span> | <span data-ttu-id="c64e0-156">Файлы и папки файловой системы</span><span class="sxs-lookup"><span data-stu-id="c64e0-156">Files and file system folders</span></span> |
    | <span data-ttu-id="c64e0-157">**HKey \_ \_Корневой** \\ **Каталог** классов</span><span class="sxs-lookup"><span data-stu-id="c64e0-157">**HKEY\_CLASSES\_ROOT**\\**Directory**</span></span>            | <span data-ttu-id="c64e0-158">Папки файловой системы</span><span class="sxs-lookup"><span data-stu-id="c64e0-158">File system folders</span></span>           |
    | <span data-ttu-id="c64e0-159">**HKey \_ \_Корневая** \\ **Папка** классов</span><span class="sxs-lookup"><span data-stu-id="c64e0-159">**HKEY\_CLASSES\_ROOT**\\**Folder**</span></span>               | <span data-ttu-id="c64e0-160">Контейнеры оболочки</span><span class="sxs-lookup"><span data-stu-id="c64e0-160">Shell containers</span></span>              |

    

     

### <a name="shell-data-source-association-arrays"></a><span data-ttu-id="c64e0-161">Массивы ассоциаций источников данных оболочки</span><span class="sxs-lookup"><span data-stu-id="c64e0-161">Shell Data Source Association Arrays</span></span>

<span data-ttu-id="c64e0-162">В следующем списке представлены некоторые массивы ассоциаций хранилища данных оболочки, которые можно использовать в целях, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="c64e0-162">The following list represents some of the Shell data store association arrays that can be used for the purposes described in this topic:</span></span>

-   <span data-ttu-id="c64e0-163">**HKey \_ \_корневой класс классов** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="c64e0-163">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="c64e0-164">_ *\_ Классы hKey \_ root **\\** аллфилесистемобжектс*\*</span><span class="sxs-lookup"><span data-stu-id="c64e0-164">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>
-   <span data-ttu-id="c64e0-165">**HKey \_ \_Корневые классы** \\ **Kind.Docумент**</span><span class="sxs-lookup"><span data-stu-id="c64e0-165">**HKEY\_CLASSES\_ROOT**\\**Kind.Document**</span></span>
-   <span data-ttu-id="c64e0-166">**HKey \_ \_Корневые** \\ **результаты** классов</span><span class="sxs-lookup"><span data-stu-id="c64e0-166">**HKEY\_CLASSES\_ROOT**\\**Results**</span></span>
-   <span data-ttu-id="c64e0-167">**HKey \_ \_Корневые классы** \\ **системфилеассоЦиатионс** \\ **. docx**</span><span class="sxs-lookup"><span data-stu-id="c64e0-167">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.docx**</span></span>
-   <span data-ttu-id="c64e0-168">**HKey \_ \_Корневые классы** \\ **Word.Docумент. 12**</span><span class="sxs-lookup"><span data-stu-id="c64e0-168">**HKEY\_CLASSES\_ROOT**\\**Word.Document.12**</span></span>

<span data-ttu-id="c64e0-169">Массивы ассоциаций источников данных оболочки, которые можно использовать для Дбфолдер (хранилище данных оболочки, представляющее элементы в результатах поиска и представлениях, основанных на запросах), приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="c64e0-169">Shell data source association arrays that can be used for DBFolder (a Shell data store that represents items in search results and query-based views) are as follows:</span></span>

-   <span data-ttu-id="c64e0-170">Диски</span><span class="sxs-lookup"><span data-stu-id="c64e0-170">Drives</span></span>
-   <span data-ttu-id="c64e0-171">Сеть</span><span class="sxs-lookup"><span data-stu-id="c64e0-171">Network</span></span>
-   <span data-ttu-id="c64e0-172">регитемс</span><span class="sxs-lookup"><span data-stu-id="c64e0-172">RegItems</span></span>
-   <span data-ttu-id="c64e0-173">Примеры:</span><span class="sxs-lookup"><span data-stu-id="c64e0-173">Examples:</span></span>
    -   <span data-ttu-id="c64e0-174">ContentView</span><span class="sxs-lookup"><span data-stu-id="c64e0-174">ContentView</span></span>
    -   <span data-ttu-id="c64e0-175">Команды</span><span class="sxs-lookup"><span data-stu-id="c64e0-175">Verbs</span></span>

<span data-ttu-id="c64e0-176">Другие распространенные массивы взаимосвязей включают папки и принтеры.</span><span class="sxs-lookup"><span data-stu-id="c64e0-176">Other common association arrays include Folder and Printers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c64e0-177">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c64e0-177">Additional Resources</span></span>

-   <span data-ttu-id="c64e0-178">Сведения о создании хранилища данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="c64e0-178">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c64e0-179">См. также</span><span class="sxs-lookup"><span data-stu-id="c64e0-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c64e0-180">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="c64e0-180">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="c64e0-181">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="c64e0-181">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="c64e0-182">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="c64e0-182">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="c64e0-183">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="c64e0-183">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="c64e0-184">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="c64e0-184">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="c64e0-185">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="c64e0-185">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="c64e0-186">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="c64e0-186">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="c64e0-187">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="c64e0-187">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> </dl>

 

 
