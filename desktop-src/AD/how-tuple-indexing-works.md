---
title: Как работает индексирование кортежей
description: Индексы кортежей используются для оптимизации поиска, которые содержат 0 или более строк срединного-Search и 0 или 1 конечные строки для поиска. Они также могут использоваться для оптимизации поиска исходной строки поиска, если для этого атрибута не доступен обычный индекс.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- Индексация кортежей
- Поиск Active Directory Active Directory, оптимизация
- Active Directory, Active Directory оптимизации поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789516"
---
# <a name="how-tuple-indexing-works"></a><span data-ttu-id="b7739-107">Как работает индексирование кортежей</span><span class="sxs-lookup"><span data-stu-id="b7739-107">How Tuple Indexing Works</span></span>

<span data-ttu-id="b7739-108">Индексы кортежей используются для оптимизации поиска, которые содержат 0 или более [строк срединного-Search](search-string-types.md) и 0 или 1 конечные строки для поиска.</span><span class="sxs-lookup"><span data-stu-id="b7739-108">Tuple indices are used to optimize searches that have 0 or more [medial-search strings](search-string-types.md) and 0 or 1 final-search strings.</span></span> <span data-ttu-id="b7739-109">Они также могут использоваться для оптимизации поиска исходной строки поиска, если для этого атрибута не доступен обычный индекс.</span><span class="sxs-lookup"><span data-stu-id="b7739-109">They can also be used to optimize searches for an initial search string if no ordinary index is available over that attribute.</span></span>

<span data-ttu-id="b7739-110">Можно включить индексирование кортежей для атрибута, установив бит 5, который соответствует значению 32 в атрибуте [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .</span><span class="sxs-lookup"><span data-stu-id="b7739-110">You can turn on tuple indexing for an attribute by setting bit 5, which corresponds to the value 32, in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute.</span></span> <span data-ttu-id="b7739-111">Этот атрибут задается в объекте схемы, который представляет атрибут, которому требуется индекс кортежа.</span><span class="sxs-lookup"><span data-stu-id="b7739-111">This attribute is set in the schema object that represents the attribute that needs the tuple index.</span></span> <span data-ttu-id="b7739-112">Снижение производительности при включении индексирования кортежей заключается в том, что любое строковое значение, заданное для этого атрибута, будет развернуто в большое количество фрагментов в индексе кортежа.</span><span class="sxs-lookup"><span data-stu-id="b7739-112">The performance impact of turning on tuple indexing is that any string value that is set for that attribute will be expanded into a large number of fragments in the tuple index.</span></span> <span data-ttu-id="b7739-113">При расширении атрибута он потребляет больше места на диске в файле дерева сведений о каталоге, а также более медленно обновляется.</span><span class="sxs-lookup"><span data-stu-id="b7739-113">When an attribute expands, it consumes a larger amount of disk space in the Directory Information Tree file, and also gets updated more slowly.</span></span>

<span data-ttu-id="b7739-114">Индексы кортежей предназначены для ускорения поиска в форме `*string*` .</span><span class="sxs-lookup"><span data-stu-id="b7739-114">Tuple indices are designed to accelerate searches of the form `*string*`.</span></span> <span data-ttu-id="b7739-115">Ускорение может быть значительным, поскольку такая форма поиска не может быть оптимизирована каким-либо другим способом, а в неоптимизированной форме она заставляет сервер Active Directory проанализировать каждый объект в области поиска, чтобы выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="b7739-115">The acceleration can be considerable because this form of search cannot be optimized in any other way, and in its un-optimized form, it forces the Active Directory server to walk every object in the scope of the search to perform the query.</span></span> <span data-ttu-id="b7739-116">Таким образом, базовый поиск будет искать только один объект, при этом непосредственный дочерний Поиск будет искать только дочерний объект объекта (который может использовать меньше ресурсов или больше ресурсов в зависимости от размера контейнера), и поиск поддерева будет проходить по всему поддереву базового объекта, которое обычно требует большого количества ресурсов и будет очень медленным из-за размера поддерева.</span><span class="sxs-lookup"><span data-stu-id="b7739-116">Thus, a base search would just search one object, which would use fewer resources, an immediate children search would search just the children of an object (which could use fewer resources or more resources depending on the container size), and a subtree search will walk the entire subtree under the base object, which would usually require a lot of resources and be very slow because of the subtree size.</span></span>

<span data-ttu-id="b7739-117">Индексы кортежей работают путем разбиения строки на *кортежи*.</span><span class="sxs-lookup"><span data-stu-id="b7739-117">Tuple indices work by breaking a string into *tuples*.</span></span> <span data-ttu-id="b7739-118">Например, строка "Active Directory" будет разбиваться на следующие кортежи:</span><span class="sxs-lookup"><span data-stu-id="b7739-118">For example, the string "Active Directory" would be broken into the following tuples:</span></span>

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> <span data-ttu-id="b7739-119">Каталог будет останавливаться на 32767 символов при расширении строки для индексирования кортежей.</span><span class="sxs-lookup"><span data-stu-id="b7739-119">The directory will stop at 32767 characters when expanding a string for tuple indexing.</span></span>

 

<span data-ttu-id="b7739-120">Индекс кортежа будет содержать запись для каждого из этих кортежей.</span><span class="sxs-lookup"><span data-stu-id="b7739-120">A tuple index would contain an entry for each one of these tuples.</span></span> <span data-ttu-id="b7739-121">Таким образом, если пользователь выполняет поиск `*cto*` , Active Directory сервер будет искать все совпадения для "CTO" в индексе и, в данном случае, найти указатель обратно к записи с атрибутом (с индексом кортежа) со значением "Directory".</span><span class="sxs-lookup"><span data-stu-id="b7739-121">So, if a user searches for `*cto*`, then the Active Directory server will look up all the matches for "cto" in the index and, in this case, find a pointer back to the record that had a (tuple indexed) attribute with a value of "Directory".</span></span>

<span data-ttu-id="b7739-122">Если строка поиска срединного ( `*cto*` в предыдущем примере) является достаточной, поиск будет выполняться достаточно эффективно, поскольку это значительно сокращает количество объектов, которые сервер Active Directory должен проверить для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="b7739-122">If the medial search string (`*cto*` in the previous example) is specific enough, then the search will be quite efficient because it greatly reduces the number of objects that the Active Directory server must inspect to perform the query.</span></span>

 

 