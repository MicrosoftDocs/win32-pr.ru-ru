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
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Использование IDirectorySearch и Идиректорйобжект для получения диапазона

Интерфейсы [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) или [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) можно использовать для получения диапазона значений свойств. Для этого укажите атрибут и диапазон для одного из атрибутов, запрошенных в запросе.

## <a name="range-retrieval-with-idirectoryobject"></a>Получение диапазона с помощью Идиректорйобжект

Интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) можно использовать для получения диапазона путем указания атрибута и диапазона для одного из атрибутов в массиве *паттрибутеснаме* при вызове метода [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Дополнительные сведения и пример кода, демонстрирующий использование интерфейса [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) для извлечения диапазона, см. в разделе [пример кода в диапазоне с идиректорйобжект](example-code-for-ranging-with-idirectoryobject.md).

## <a name="range-retrieval-with-idirectorysearch"></a>Получение диапазона с помощью IDirectorySearch

Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) можно использовать для получения диапазона путем указания атрибута и диапазона для одного из полученных атрибутов в массиве *паттрибутеснаме* при вызове метода [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



При использовании интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) для извлечения по диапазону существует одна проблема, которая должна быть специально решена. Если запрошенный диапазон превышает число оставшихся значений, [**IDirectorySearch:: DataColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) вернет **столбец "E ADS" \_ \_ \_ не \_ задан**. Чтобы получить оставшиеся значения, необходимо использовать шаблон диапазона " \* ". Например, если группа содержит 150 членов, значения элементов 0-100 можно получить обычным образом, используя извлечение по диапазону. Если затем запрашивается диапазон 101-200, **IDirectorySearch:: DataColumn** вернет **столбец "E \_ ADSS" \_ \_ не \_ задан**. Эту проблему можно избежать с помощью метода [**IDirectorySearch:: жетнекстколумннаме**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) . Как правило, **жетнекстколумннаме** вернет исходную строку запроса. Однако если запрошенный диапазон превышает количество оставшихся значений, **жетнекстколумннаме** Возвращает измененную версию строки запроса, заменяя значение верхнего диапазона на подстановочный знак " \* ". В приведенном выше примере первый запрос будет выполнен с строкой атрибута "member; Range = 0-100", а **жетнекстколумннаме** вернет "member; Range = 0-100". Во втором запросе строка атрибута будет иметь значение "member; Range = 101-200", но **жетнекстколумннаме** будет возвращать "член; Range = 101- \* ". Этот вариант можно определить, сравнив исходную строку атрибута с результатом **жетнекстколумннаме**. Если строки различаются, последний блок значений должен быть снова запрошен с использованием подстановочного знака диапазона.

Дополнительные сведения и пример кода, демонстрирующий использование интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) для извлечения диапазона, см. в разделе [пример кода в диапазоне с IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).

 

 




