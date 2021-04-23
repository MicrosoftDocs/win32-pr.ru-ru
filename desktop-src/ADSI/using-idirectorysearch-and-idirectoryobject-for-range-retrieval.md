---
title: Использование IDirectorySearch и Идиректорйобжект для получения диапазона
description: Интерфейсы Идиректорйобжект или IDirectorySearch можно использовать для получения диапазона значений свойств. Для этого укажите атрибут и диапазон для одного из атрибутов, запрошенных в запросе.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI, использование для получения элементов группы
- Идиректорйобжект ADSI, использование для получения элементов группы
- Получение диапазона ADSI с помощью IDirectorySearch и Идиректорйобжект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654091"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a><span data-ttu-id="6f640-107">Использование IDirectorySearch и Идиректорйобжект для получения диапазона</span><span class="sxs-lookup"><span data-stu-id="6f640-107">Using IDirectorySearch and IDirectoryObject for Range Retrieval</span></span>

<span data-ttu-id="6f640-108">Интерфейсы [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) или [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) можно использовать для получения диапазона значений свойств.</span><span class="sxs-lookup"><span data-stu-id="6f640-108">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) or [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="6f640-109">Для этого укажите атрибут и диапазон для одного из атрибутов, запрошенных в запросе.</span><span class="sxs-lookup"><span data-stu-id="6f640-109">To do this, specify the attribute and range for one of the attributes requested in the query.</span></span>

## <a name="range-retrieval-with-idirectoryobject"></a><span data-ttu-id="6f640-110">Получение диапазона с помощью Идиректорйобжект</span><span class="sxs-lookup"><span data-stu-id="6f640-110">Range Retrieval with IDirectoryObject</span></span>

<span data-ttu-id="6f640-111">Интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) можно использовать для получения диапазона путем указания атрибута и диапазона для одного из атрибутов в массиве *паттрибутеснаме* при вызове метода [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="6f640-111">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface can be used for range retrieval by specifying the attribute and range for one of the attributes in the *pAttributesName* array when calling the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



<span data-ttu-id="6f640-112">Дополнительные сведения и пример кода, демонстрирующий использование интерфейса [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) для извлечения диапазона, см. в разделе [пример кода в диапазоне с идиректорйобжект](example-code-for-ranging-with-idirectoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="6f640-112">For more information and a code example that shows how to use the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for range retrieval, see [Example Code for Ranging with IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span></span>

## <a name="range-retrieval-with-idirectorysearch"></a><span data-ttu-id="6f640-113">Получение диапазона с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="6f640-113">Range Retrieval with IDirectorySearch</span></span>

<span data-ttu-id="6f640-114">Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) можно использовать для получения диапазона путем указания атрибута и диапазона для одного из полученных атрибутов в массиве *паттрибутеснаме* при вызове метода [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="6f640-114">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface can be used for range retrieval by specifying the attribute and range for one of the retrieved attributes in the *pAttributesName* array when calling the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method.</span></span>


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



<span data-ttu-id="6f640-115">При использовании интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) для извлечения по диапазону существует одна проблема, которая должна быть специально решена.</span><span class="sxs-lookup"><span data-stu-id="6f640-115">When using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="6f640-116">Если запрошенный диапазон превышает число оставшихся значений, [**IDirectorySearch:: DataColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) вернет **столбец "E ADS" \_ \_ \_ не \_ задан**.</span><span class="sxs-lookup"><span data-stu-id="6f640-116">When the range requested exceeds the number of remaining values, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="6f640-117">Чтобы получить оставшиеся значения, необходимо использовать шаблон диапазона " \* ".</span><span class="sxs-lookup"><span data-stu-id="6f640-117">To retrieve the remaining values, it is necessary to use the range wildcard '\*'.</span></span> <span data-ttu-id="6f640-118">Например, если группа содержит 150 членов, значения элементов 0-100 можно получить обычным образом, используя извлечение по диапазону.</span><span class="sxs-lookup"><span data-stu-id="6f640-118">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="6f640-119">Если затем запрашивается диапазон 101-200, **IDirectorySearch:: DataColumn** вернет **столбец "E \_ ADSS" \_ \_ не \_ задан**.</span><span class="sxs-lookup"><span data-stu-id="6f640-119">If range 101-200 is then requested, **IDirectorySearch::GetColumn** will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="6f640-120">Эту проблему можно избежать с помощью метода [**IDirectorySearch:: жетнекстколумннаме**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) .</span><span class="sxs-lookup"><span data-stu-id="6f640-120">This problem can be avoided by using the [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) method.</span></span> <span data-ttu-id="6f640-121">Как правило, **жетнекстколумннаме** вернет исходную строку запроса.</span><span class="sxs-lookup"><span data-stu-id="6f640-121">Normally, **GetNextColumnName** will return the original query string.</span></span> <span data-ttu-id="6f640-122">Однако если запрошенный диапазон превышает количество оставшихся значений, **жетнекстколумннаме** Возвращает измененную версию строки запроса, заменяя значение верхнего диапазона на подстановочный знак " \* ".</span><span class="sxs-lookup"><span data-stu-id="6f640-122">However, when the range requested exceeds the number of remaining values, **GetNextColumnName** will return a modified version of the query string by replacing the high range value with the range wildcard '\*'.</span></span> <span data-ttu-id="6f640-123">В приведенном выше примере первый запрос будет выполнен с строкой атрибута "member; Range = 0-100", а **жетнекстколумннаме** вернет "member; Range = 0-100".</span><span class="sxs-lookup"><span data-stu-id="6f640-123">In the example above, the first query would be performed with an attribute string of "member;range=0-100" and **GetNextColumnName** will return "member;range=0-100".</span></span> <span data-ttu-id="6f640-124">Во втором запросе строка атрибута будет иметь значение "member; Range = 101-200", но **жетнекстколумннаме** будет возвращать "член; Range = 101- \* ".</span><span class="sxs-lookup"><span data-stu-id="6f640-124">In the second query, the attribute string would be "member;range=101-200", but **GetNextColumnName** will return "member;range=101-\*".</span></span> <span data-ttu-id="6f640-125">Этот вариант можно определить, сравнив исходную строку атрибута с результатом **жетнекстколумннаме**.</span><span class="sxs-lookup"><span data-stu-id="6f640-125">This case can be determined by comparing the original attribute string to the result of **GetNextColumnName**.</span></span> <span data-ttu-id="6f640-126">Если строки различаются, последний блок значений должен быть снова запрошен с использованием подстановочного знака диапазона.</span><span class="sxs-lookup"><span data-stu-id="6f640-126">If the strings are different, the last block of values should be requested again with the range wildcard.</span></span>

<span data-ttu-id="6f640-127">Дополнительные сведения и пример кода, демонстрирующий использование интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) для извлечения диапазона, см. в разделе [пример кода в диапазоне с IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="6f640-127">For more information and a code example that shows how to use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, see [Example Code for Ranging with IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span></span>

 

 




