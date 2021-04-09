---
title: Поиск с помощью интерфейса IDirectorySearch
description: Интерфейс IDirectorySearch предоставляет высокоуровневые и недорогие интерфейсы для запроса данных каталога или глобального каталога.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Поиск с помощью интерфейса ADSI в интерфейсе IDirectorySearch
- Запросы к ADSI, интерфейсы запросов, IDirectorySearch
- ADSI ADSI, пример кода C/C++, поиск в каталоге с помощью IDirectorySearch
- IDirectorySearch ADSI, использование для поиска в каталоге
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891093"
---
# <a name="searching-with-the-idirectorysearch-interface"></a>Поиск с помощью интерфейса IDirectorySearch

Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) предоставляет высокоуровневые и недорогие интерфейсы для запроса данных каталога или глобального каталога. COM-интерфейс **IDirectorySearch** может использоваться только с vtable, и поэтому недоступен для сред разработки на основе автоматизации.

**Выполнение поиска**

1.  Привязка к объекту в каталоге.
2.  Вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить указатель [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .
3.  Выполните поиск с помощью указателя [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Вызовите метод [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) и передайте фильтр поиска, запрошенные имена атрибутов и другие параметры.

Дополнительные сведения о синтаксисе фильтра поиска см. в разделе [синтаксис фильтра поиска](search-filter-syntax.md).

Выполнение запроса зависит от поставщика. При использовании некоторых поставщиков фактическое выполнение запроса не происходит до вызова [**IDirectorySearch:: жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) или [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) . Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) работает с фильтрами поиска напрямую. Ни диалект SQL, ни диалект LDAP не требуются.

Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) предоставляет методы для перечисления результирующего набора по строкам. Метод [**IDirectorySearch:: жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) извлекает первую строку, а [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) перемещает вас на следующую строку из текущей строки. Когда вы достигли последней строки, вызов этих методов возвращает \_ код ошибки в ADS \_ \_ . И наоборот, [**IDirectorySearch:: жетпревиаусров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) перемещает вас назад на одну строку за раз. \_ \_ \_ Возвращаемое значение S ADS не показывает, что достигнута первая строка результирующего набора. Эти методы работают с результирующим набором, резидентным в память, на клиенте. Таким образом, при выполнении страничного и асинхронного поиска, а также при отключенном \_ \_ параметре результатов кэширования Обратная прокрутка может привести к непредвиденным последствиям.

После того как вы настроили соответствующую строку, вызовите [**IDirectorySearch:: DataColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) , чтобы получить элементы данных, столбец по столбцу. Для каждого вызова передается имя интересующего столбца. Возвращаемый элемент данных является указателем на структуру [**\_ \_ столбцов поиска баннеров**](/windows/desktop/api/Iads/ns-iads-ads_search_column) . **DataColumn** выделяет эту структуру, но ее необходимо освободить с помощью [**фриколумн**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn). Вызовите [**клосесеарчхандле**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) для завершения операции поиска.

**Выполнение поиска в каталоге**

1.  Привязка к поставщику LDAP. Это может быть контроллер домена или поставщик глобального каталога.
2.  Получение COM-интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) с вызовом [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Эта операция могла быть выполнена на шаге 1 во время начальной привязки.

    При необходимости вызовите [**сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , чтобы выбрать параметры для обработки результатов поиска.

3.  Вызовите [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch). В зависимости от параметров, заданных в [**сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , это может быть, или нет, начать выполнение запроса.
4.  Вызовите [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) , чтобы переместить индекс строки (от внутреннего к [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) в первую строку.
5.  Прочтите данные из строки с помощью метода [**DataColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), а затем вызовите [**фриколумн**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) , чтобы освободить память, выделенную методом **DataColumn**.
6.  Повторяйте шаг 5, пока не будут получены все данные из результата поиска, или пока [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) не вернет \_ строки в ADS \_ \_ .
7.  По завершении вызовите [**абандонсеарч**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) и [**клосесеарчхандле**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) .

Этот сценарий показан в следующем примере кода. Чтобы начать привязку к ADSI, вызовите функцию [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



Это предоставляет указатель на интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

Теперь, когда имеется COM-интерфейс для экземпляра Идиректоринтерфаце, вызовите [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).

Создайте массив имен атрибутов, чтобы подготовиться к вызову функции [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . Имена атрибутов определяются в схеме Active Directory. Дополнительные сведения об определении схемы см. в разделе [модель схемы ADSI](adsi-schema-model.md). Перечисленные имена атрибутов возвращаются, если они поддерживаются объектом в качестве результирующего набора поиска.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



Теперь вызовите функцию [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . Поиск не выполняется до тех пор, пока не будет вызван метод [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Вызовите [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) для итерации строк в результате. Затем каждая строка запрашивается для атрибута "Description". Если атрибут найден, он отображается.


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



Чтобы завершить поиск, вызовите метод [**абандонсеарч**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .

Имейте в виду, что если размер страницы не задан, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) блокируется до тех пор, пока не будет возвращен весь результирующий набор клиенту. Если задан размер страницы, то **GetNextRow** блокируется до тех пор, пока не будет возвращена первая страница (размер страницы = количество строк на странице). Если задан размер страницы и запрос должен быть отсортирован, а поиск по крайней мере одного индексированного атрибута не выполняется, то значение размера страницы игнорируется, а сервер вычисляет весь результирующий набор перед возвратом данных. Это влияет на **GetNextRow** блокировку до завершения запроса.

> [!Note]  
> Чтобы изменить этот запрос в поиске по каталогу на глобальный поиск каталога, вызов [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) изменится.

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 