---
description: В этой статье объясняется, как инициализировать обработчики свойств для работы с системой свойств Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Инициализация обработчиков свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7626f92b3d81a6764e635c10302747f82a383
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406997"
---
# <a name="initializing-property-handlers"></a>Инициализация обработчиков свойств

В этом разделе объясняется, как создавать и регистрировать обработчики свойств для работы с системой свойств Windows.

Этот раздел организован следующим образом:

-   [Обработчики свойств](#property-handlers)
-   [Перед началом](#before-you-begin)
-   [Инициализация обработчиков свойств](#initializing-property-handlers)
-   [Хранилище свойств в памяти](#in-memory-property-store)
-   [Работа с PROPVARIANT-Basedными значениями](#dealing-with-propvariant-based-values)
-   [Поддержка открытых метаданных](#supporting-open-metadata)
-   [Полнотекстовое содержимое](#full-text-contents)
-   [Предоставление значений для свойств](#providing-values-for-properties)
-   [Запись обратных значений](#writing-back-values)
-   [Реализация Ипропертисторекапабилитиес](#implementing-ipropertystorecapabilities)
-   [Регистрация и распространение обработчиков свойств](#registering-and-distributing-property-handlers)
-   [Связанные темы](#related-topics)

## <a name="property-handlers"></a>Обработчики свойств

Обработчики свойств являются ключевой частью системы свойств. Они вызываются внутри процесса индексатором для чтения и индексирования значений свойств, а также вызываются проводником Windows в процессе чтения и записи значений свойств непосредственно в файлах. Эти обработчики необходимо тщательно записать и протестировать, чтобы предотвратить снижение производительности или потери данных в затронутых файлах. Дополнительные сведения о вопросах, связанных с индексатором, которые влияют на реализацию обработчика свойств, см. в разделе [Разработка обработчиков свойств для поиска Windows](../search/-search-3x-wds-extidx-propertyhandlers.md).

В этом разделе рассматривается пример формата файлов на основе XML, описывающий рецепт с расширением имени файла. рецепт. Расширение имени файла с расширением. рецепт регистрируется в собственном отдельном формате, вместо того чтобы полагаться на универсальный формат .xml, обработчик использует вторичный поток для хранения свойств. Для типов файлов рекомендуется зарегистрировать уникальные расширения имен файлов.

## <a name="before-you-begin"></a>Перед началом

Обработчики свойств — это COM-объекты, создающие абстракцию [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) для определенного формата файла. Они считывают (анализируют) и записывают этот формат файла способом, который соответствует его спецификации. Некоторые обработчики свойств выполняют свою работу на основе API-интерфейсов, которые имеют абстрактный доступ к конкретному формату файла. Перед разработкой обработчика свойств для формата файла необходимо понять, как хранятся свойства в формате файла, и как эти свойства (имена и значения) сопоставляются с абстракцией хранилища свойств.

При планировании реализации Помните, что обработчики свойств являются компонентами низкого уровня, загруженными в контексте таких процессов, как проводник, индексатор Windows Search и сторонние приложения, использующие модель программирования элементов оболочки. В результате обработчики свойств не могут быть реализованы в управляемом коде и должны быть реализованы в C++. Если обработчик использует интерфейсы API или службы для выполнения своей работы, необходимо убедиться, что эти службы могут правильно работать в средах, где загружается обработчик свойств.

> [!Note]  
> Обработчики свойств всегда связаны с конкретными типами файлов. Таким же, если формат файла содержит свойства, требующие пользовательского обработчика свойств, всегда следует регистрировать уникальное расширение имени файла для каждого формата файла.

 

## <a name="initializing-property-handlers"></a>Инициализация обработчиков свойств

Прежде чем свойство будет использоваться системой, оно инициализируется путем вызова реализации [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream). Обработчик свойства должен быть инициализирован путем того, что система присваивает ему поток, а не оставит это назначение реализации обработчика. Этот метод инициализации обеспечивает следующие факторы:

-   Обработчик свойств может выполняться в ограниченном процессе (важный компонент безопасности) без прав доступа для непосредственного чтения или записи файлов, а не доступа к их содержимому через поток.
-   Система может быть доверенной, чтобы правильно обрабатывать файл операционные блокировки, что является важной мерой надежности.
-   Система свойств предоставляет автоматически сохраняемую службу без дополнительных функций, необходимых для реализации обработчика свойств. Дополнительные сведения о потоках см. в разделе [запись обратных значений](#writing-back-values) .
-   Использование [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) абстрагирует реализацию из сведений о файловой системе. Это позволяет обработчику поддерживать инициализацию с помощью альтернативных хранилищ, например папки протокол FTP (FTP) или сжатого файла с расширением имени файла .zip.

Бывают случаи, когда инициализация с помощью потоков невозможна. В этих ситуациях существуют два дополнительных интерфейса, которые могут реализовать обработчики свойств: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) и [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Если обработчик свойства не реализует [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), он должен отказаться от выполнения в изолированном процессе, в котором индексатор системы поместит его по умолчанию, если произошло изменение в потоке. Чтобы отказаться от этой функции, задайте следующее значение реестра.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Однако гораздо лучше реализовать [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) и выполнить инициализацию на основе потока. В результате ваш обработчик свойств будет более безопасным и надежным. Отключение изоляции процессов обычно предназначено только для устаревших обработчиков свойств и должно быть стренуауслио без какого-либо нового кода.

Чтобы подробно изучить реализацию обработчика свойств, рассмотрим следующий пример кода, который является реализацией [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize). Обработчик инициализируется путем загрузки документа с рецептом на основе XML посредством указателя на соответствующий экземпляр [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) этого документа. Переменная **\_ спдоцеле** , используемая около конца примера кода, определена ранее в примере как Msxml2:: иксмлдомелементптр.

> [!Note]  
> Следующий код и все последующие примеры кода взяты из примера обработчика рецептов, входящего в состав пакета средств разработки программного обеспечения (SDK) для Windows. .

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



Â 

После загрузки документа свойства, отображаемые в проводнике Windows, загружаются путем вызова защищенного метода **\_ LoadProperties** , как показано в следующем примере кода. Этот процесс подробно рассматривается в следующем разделе.


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



Если поток доступен только для чтения, но параметр *грфмоде* содержит \_ флаг стгм ReadWrite, инициализация должна завершиться ошибкой и вернуть STG \_ E \_ ACCESSDENIED. Без этой проверки проводник Windows отображает значения свойств как доступные для записи, даже если это не так, что приведет к путанице в работе конечных пользователей.

Обработчик свойств инициализируется только один раз в течение своего времени существования. Если запрашивается вторая инициализация, обработчик должен вернуть `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .

## <a name="in-memory-property-store"></a>Хранилище свойств In-Memory

Перед рассмотрением реализации **\_ LoadProperties** необходимо понять, какой массив **PropertyMap** используется в примере, чтобы сопоставлять свойства в XML-документе с существующими свойствами в системе свойств с помощью их значений PKEY.

Не следует предоставлять каждый элемент и атрибут в XML-файле в качестве свойства. Вместо этого следует выбирать только те, которые вы считаете полезными для конечных пользователей в организации их документов (в нашем примере это рецепты). Это важная концепция, которую следует помнить при разработке обработчиков свойств: разница между сведениями, которые действительно удобно использовать для организационных сценариев, и сведениями, которые относятся к сведениям о файле и могут быть просмотрены путем открытия самого файла. Свойства не предназначены для полного дублирования XML-файла.


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



Ниже приведена полная реализация метода **\_ LoadProperties** , вызываемого методом [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



Метод **\_ LoadProperties** вызывает вспомогательную функцию оболочки [**пскреатемеморипропертисторе**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) для создания хранилища свойств в памяти (кэша) для обрабатываемых свойств. С помощью кэша изменения отправляются за вас. Это освобождает от отслеживания изменения значения свойства в кэше, но еще не сохраненного в постоянном хранилище. Он также освобождает вас от ненужных сохраненных значений свойств, которые не были изменены.

Метод **\_ LoadProperties** также вызывает **\_ Свойства LoadProperty** , реализация которого показана в следующем коде, один раз для каждого сопоставленного свойства. **\_ Свойства LoadProperty** получает значение свойства, как указано в элементе **PROPERTYMAP** в потоке XML, и назначает его кэшу в памяти посредством вызова [**ипропертисторекаче:: сетвалуеандстате**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate). \_Стандартный флаг PSC в вызове **ипропертисторекаче:: сетвалуеандстате** указывает, что значение свойства не было изменено со времени, когда оно было введено в кэш.


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a>Работа с PROPVARIANT-Basedными значениями

В реализации **\_ Свойства LoadProperty** значение свойства указывается в виде [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Набор интерфейсов API в пакете средств разработки программного обеспечения (SDK) предоставляется для преобразования из типов **пропвариант** в типы-примитивы, такие как **пвстр** или **int** . Эти API-интерфейсы находятся в Пропварутил. h.

Например, чтобы преобразовать [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) в строку, можно использовать [**пропварианттостринг**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) , как показано здесь.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Чтобы инициализировать ПРОПВАРИАНТ из строки, можно использовать [**инитпропвариантфромстринг**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Как можно увидеть в любом из файлов рецептов, входящих в образец, в каждом файле может быть несколько ключевых слов. Для этого система свойств поддерживает строки с несколькими значениями, представленные в виде вектора строк (например, "VT \_ vector \| VT \_ "). Метод **\_ лоадвекторпроперти** в примере использует векторные значения.


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



Если значение не существует в файле, не возвращайте ошибку. Вместо этого задайте значение VT \_ Empty и возвратите **S \_ ОК**. VT \_ Empty указывает, что значение свойства не существует.

## <a name="supporting-open-metadata"></a>Поддержка открытых метаданных

В этом примере используется формат файла на основе XML. Его схему можно расширить для поддержки свойств, которые не были рассмотрены во время девелопмет, например. Эта система называется открытыми метаданными. Этот пример расширяет систему свойств, создавая узел под элементом **рецепта** с именем **расширенных свойств**, как показано в следующем примере кода.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Чтобы загрузить материализованные расширенные свойства во время инициализации, реализуйте метод **\_ лоадекстендедпропертиес** , как показано в следующем примере кода.


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



Интерфейсы API сериализации, объявленные в Пропсис. h, используются для сериализации и десериализации типов [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) в большие двоичные объекты данных, а затем для сериализации этих больших двоичных объектов в строки, которые могут быть СОХРАНЕНЫ в XML, используются кодировка Base64. Эти строки хранятся в атрибуте **енкодедвалуе** элемента **расширенных свойств** . Следующий служебный метод, реализованный в файле util. cpp в примере, выполняет сериализацию. Он начинается с вызова функции [**стгсериализепропвариант**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) для выполнения двоичной сериализации, как показано в следующем примере кода.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



Затем функция [**криптбинаритостринг**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)в, объявленная в винкрипт. h, выполняет преобразование Base64.


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



Функция **десериализепропвариантфромстринг** , также найденная в файле util. cpp, обращается к операции десериализации значений из XML-файла.

Дополнительные сведения о поддержке открытых метаданных см. в разделе "типы файлов, поддерживающие открытые метаданные" раздела [типы файлов](../shell/fa-file-types.md).

## <a name="full-text-contents"></a>Содержимое Full-Text

Обработчики свойств также могут упростить полнотекстовый поиск содержимого файла, и они являются простым способом предоставления этих функций, если формат файла не слишком сложен. Существует альтернативный, более эффективный способ предоставления полного текста файла с помощью реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

В следующей таблице приведены преимущества каждого из подходов, использующих [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) или [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).



| Функция                                   | IFilter                      | ипропертисторе |
|----------------------------------------------|------------------------------|----------------|
| Разрешает ли обратную запись в файлы?                  | Нет                           | Да            |
| Предоставляет сочетание содержимого и свойств?      | Да                          | Да            |
| Многоязычных?                                | Да                          | Нет             |
| MIME/Embedded?                               | Да                          | Нет             |
| Границы текста?                             | Предложение, абзац, глава | Нет           |
| Реализация, поддерживаемая для SPS/SQL Server? | Да                          | Нет             |
| Реализация                               | Complex                      | Простота         |



 

В образце обработчика рецептов формат файла рецепта не имеет сложных требований, поэтому для поддержки полнотекстового выполнения реализован только [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Полнотекстовый поиск реализуется для XML-узлов, указанных в следующем массиве.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



Система свойств содержит `System.Search.Contents` свойство (содержимое для \_ поиска PKEY \_ ), которое было создано для предоставления полнотекстового содержимого индексатору. Значение этого свойства никогда не отображается непосредственно в пользовательском интерфейсе; текст из всех узлов XML, указанных в приведенном выше массиве, объединяется в одну строку. Затем эта строка предоставляется индексатору в качестве полнотекстового содержимого файла рецепта с помощью вызова [**ипропертисторекаче:: сетвалуеандстате**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) , как показано в следующем примере кода.


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a>Предоставление значений для свойств

При использовании для считывания значений обработчики свойств обычно вызываются по одной из следующих причин:

-   Для перечисления всех значений свойств.
-   Для получения значения определенного свойства.

Для перечисления обработчику свойств предлагается перечислить его свойства либо во время индексирования, либо когда диалоговое окно свойств запрашивает свойства, отображаемые в **другой** группе. Индексирование постоянно выполняется как фоновая операция. При каждом изменении файла индексатор уведомляется, и он повторно индексирует файл, запросив обработчику свойств перечислить его свойства. Поэтому очень важно, чтобы обработчики свойств были эффективно реализованы и возвращали значения свойств как можно быстрее. Перечислите все свойства, для которых имеются значения, точно так же, как и для любой коллекции, но не перечислите свойства, использующие вычисления с интенсивным использованием памяти или сетевые запросы, которые могут затруднить их получение.

При написании обработчика свойств, как правило, необходимо рассмотреть два следующих набора свойств.

-   Основные свойства. свойства, которые поддерживает собственный тип файлов. Например, обработчик свойств Photo для метаданных файла изображения (EXIF), который изначально поддерживает `System.Photo.FNumber` .
-   Расширенные свойства: свойства, которые поддерживаются типом файлов как часть открытых метаданных.

Поскольку в этом примере используется кэш в памяти, реализация методов [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) заключается в делегировании к этому кэшу, как показано в следующем примере кода.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Если вы решили не делегировать кэш в памяти, необходимо реализовать методы, чтобы обеспечить> следующем ожидаемом поведении:

-   [**Ипропертисторе:: NOCOUNT**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): Если нет свойств, этот метод возвращает значение **S \_ ОК**.
-   [**Ипропертисторе:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): Если *ипроп* больше или равно *Кпропс*, этот метод возвращает E \_ INVALIDARG, а структура, на которую указывает параметр *PKEY* , заполняется нулями.
-   [**Ипропертисторе::**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) NOCOUNT и [**Ипропертисторе:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) отражает текущее состояние обработчика свойства. Если [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) добавляется в файл или удаляется из него с помощью [**Ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), эти два метода должны отражать это изменение при следующем вызове.
-   [**Ипропертисторе:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): Если этот метод запрашивает значение, которое не существует, то оно возвращает **\_ ОК** , а значение, сообщаемое как VT \_ Empty.

## <a name="writing-back-values"></a>Запись обратных значений

Когда обработчик свойств записывает значение свойства с помощью [**ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), он не записывает значение в файл до тех пор, пока не будет вызван [**Ипропертисторе:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) . Кэш в памяти может быть полезен при реализации этой схемы. В образце кода реализация **ипропертисторе:: SetValue** просто задает новое значение в кэше в памяти и устанавливает для этого свойства состояние "нет на PSC \_ ".


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



В любой реализации [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) ожидается следующее поведение из [**Ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):

-   Если свойство уже существует, устанавливается значение свойства.
-   Если свойство не существует, добавляется новое свойство и задается его значение.
-   Если значение свойства не может быть сохранено точно так же, как это было задано (например, усечение из-за ограничений размера в формате файла), значение задается как можно больше, и \_ \_ возвращается усечение с усеченным значением.
-   Если свойство не поддерживается обработчиком свойств, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` возвращается значение.
-   Если существует другая причина, по которой невозможно задать значение свойства, например блокировка файла или отсутствие прав на изменение через списки управления доступом (ACL), \_ возвращается STG E \_ ACCESSDENIED.

Одним из основных преимуществ использования потоков в качестве примера является надежность. Обработчики свойств должны всегда учитывать, что они не могут оставить файл в нестабильном состоянии в случае катастрофического сбоя. Из-за повреждения файлов пользователя следует избегать, и лучший способ сделать это — использовать механизм копирования при записи. Если обработчик свойств использует поток для доступа к файлу, это поведение будет получено автоматически. система записывает любые изменения в поток, заменяя файл новой копией только во время операции фиксации.

Чтобы переопределить это поведение и управлять процессом сохранения файлов вручную, можно отказаться от безопасного сохранения, задав значение Мануалсафесаве в записи реестра обработчика, как показано здесь.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Если обработчик задает значение Мануалсафесаве, то поток, с помощью которого он инициализируется, не является транзакционным потоком (СТГМ \_ транзакционным). Сам обработчик должен реализовать функцию безопасного сохранения, чтобы убедиться, что файл не поврежден, если операция сохранения прервана. Если обработчик реализует встроенную запись, он выполняет запись в поток, который ему передан. Если обработчик не поддерживает эту функцию, он должен получить поток для записи обновленной копии файла с помощью [**идестинатионстреамфактори:: жетдестинатионстреам**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream). После того как обработчик закончит запись, он должен вызвать [**ипропертисторе:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) для исходного потока, чтобы завершить операцию, и заменить содержимое исходного потока новой копией файла.

Мануалсафесаве также является ситуацией по умолчанию, если обработчик не инициализируется потоком. Без исходного потока для получения содержимого временного потока необходимо использовать [**реплацефиле**](/windows/win32/api/winbase/nf-winbase-replacefilea) для выполнения атомарной замены исходного файла.

Большие форматы файлов, которые будут использоваться способом создания файлов, превышающих 1 МБ, должны реализовать поддержку записи свойств на месте; в противном случае поведение производительности не соответствует ожиданиям клиентов системы свойств. В этом сценарии время, необходимое для записи свойств, не должно зависеть от размера файла.

Для очень больших файлов, например видеофайла размером 1 ГБ или более, требуется другое решение. Если в файле недостаточно места для выполнения записи на месте, обработчик может завершиться ошибкой, если объем пространства, зарезервированного для записи свойств на месте, был исчерпан. Эта ошибка возникает во избежание низкой производительности от 2 ГБ операций ввода-вывода (1 для чтения, 1 для записи). Из-за такого сбоя эти форматы файлов должны резервировать достаточно места для записи свойств на месте.

Если файл содержит достаточно места в заголовке для записи метаданных, и если запись этих метаданных не приводит к увеличению или уменьшению файла, то может быть полезно писать на месте. В качестве отправной точки рекомендуется использовать 64 КБ. Написание на месте эквивалентно обработчику, запрашивающему Мануалсафесаве и вызывающему метод [**IStream:: Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) в реализации [**Ипропертисторе:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), и имеет гораздо более высокую производительность, чем копирование на запись. Если размер файла изменяется из-за изменения значения свойства, запись на месте не должна быть выполнена из-за возможного повреждения файла в случае аварийного завершения.

> [!Note]  
> Для повышения производительности рекомендуется использовать параметр Мануалсафесаве с обработчиками свойств, которые работают с файлами размером 100 КБ или больше.

 

Как показано в следующем примере реализации [**ипропертисторе:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), обработчик для мануалсафесаве регистрируется, чтобы проиллюстрировать параметр безопасного сохранения вручную. Метод **\_ савекачетодом** записывает значения свойств, хранящиеся в кэше в памяти, в объект XMLdocument.


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



Затем спросите, поддерживает ли занное [**идестинатионстреамфактори**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



Затем зафиксируйте исходный поток, который записывает данные обратно в исходный файл в безопасном режиме.


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



Затем изучите реализацию **\_ савекачетодом** .


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



Затем получите количество свойств, хранящихся в кэше в памяти.


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



Теперь можно выполнить итерацию по свойствам, чтобы определить, изменилось ли значение свойства с момента его загрузки в память.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



Метод [**ипропертисторекаче::**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) WebMethod возвращает состояние свойства в кэше. Флаг PSC \_ Dirty, заданный в реализации [**ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , помечает свойство как измененное.


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



Сопоставьте свойство с XML-узлом, как указано в массиве **\_ ргпропертимап** .


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



Если свойство отсутствует в сопоставлении, это новое свойство, установленное проводником Windows. Так как поддерживаются открытые метаданные, сохраните новое свойство в разделе **РАСШИРЕННЫХ свойств** XML.


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a>Реализация Ипропертисторекапабилитиес

[**Ипропертисторекапабилитиес**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) информирует пользовательский интерфейс оболочки о возможности редактирования определенного свойства в пользовательском интерфейсе оболочки. Важно отметить, что это связано только с возможностью изменения свойства в пользовательском интерфейсе, а также в том, можно ли успешно вызвать метод [**ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) для свойства. Свойство, провокес возвращаемое значение S \_ false из [**ипропертисторекапабилитиес:: испропертивритабле**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) , по-прежнему может быть настроено через приложение.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**Испропертивритабле**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) возвращает **" \_ ОК** ", чтобы указать, что конечным пользователям следует разрешить изменение свойства напрямую; \_Значение false указывает, что они не должны. \_Значение false может означать, что приложения отвечают за написание свойства, а не пользователей. Оболочка отключает редактирование элементов управления в соответствии с результатами вызовов этого метода. Предполагается, что обработчик, не реализующий [**ипропертисторекапабилитиес**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) , поддерживает открытые метаданные посредством поддержки записи любого свойства.

При создании обработчика, который обрабатывает только свойства, доступные только для чтения, следует реализовать метод **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)или [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)), чтобы он возвращал STG \_ E \_ ACCESSDENIED при вызове с \_ флагом стгм ReadWrite.

Для некоторых свойств атрибут [исиннате](./propdesc-schema-typeinfo.md) имеет значение **true**. Свойства присущей имеют следующие характеристики.

-   Свойство обычно вычисляется каким-либо образом. Например, `System.Image.BitDepth` вычисляется на основе самого изображения.
-   Изменение свойства не имеет смысла, не изменяя файл. Например, изменение `System.Image.Dimensions` не приведет к изменению размера изображения, поэтому нет смысла разрешать пользователю изменять его.
-   В некоторых случаях эти свойства предоставляются системой автоматически. Примеры включают в себя `System.DateModified` , предоставляемые файловой системой, и `System.SharedWith` , основанные на том, кому предоставлен доступ к файлу.

Из-за этих характеристик свойства, помеченные как *исиннате* , предоставляются пользователю в пользовательском интерфейсе оболочки только в качестве свойств, доступных только для чтения. Если свойство помечено как *исиннате*, система свойств не сохраняет это свойство в обработчике свойств. Поэтому обработчики свойств не требуют специального кода для учета этих свойств в своих реализациях. Если значение атрибута *исиннате* явно не указано для конкретного свойства, значение по умолчанию — **false**.

## <a name="registering-and-distributing-property-handlers"></a>Регистрация и распространение обработчиков свойств

При реализации обработчика свойств необходимо зарегистрировать его и расширение имени файла, связанное с обработчиком. Дополнительные сведения см. в разделе [Регистрация и распространение обработчиков свойств](./prophand-reg-dist.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Основные сведения о обработчиках свойств](./building-property-handlers-properties.md)
</dt> <dt>

[Использование имен видов](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Использование списков свойств](./building-property-handlers-property-lists.md)
</dt> <dt>

[Регистрация и распространение обработчиков свойств](./prophand-reg-dist.md)
</dt> <dt>

[Рекомендации и вопросы и ответы по обработчикам свойств](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
