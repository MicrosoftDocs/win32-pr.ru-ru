---
description: Установка обработчика протокола включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files, а затем регистрацию обработчика протокола с помощью реестра.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Установка и регистрация обработчиков протоколов (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682530"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a>Установка и регистрация обработчиков протоколов (Поиск Windows)

Установка обработчика протокола включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files, а затем регистрацию обработчика протокола с помощью реестра. Приложение установки может также добавить правила корня и области поиска, чтобы определить область обхода по умолчанию для источника данных оболочки.

Этот раздел организован следующим образом:

-   [Об URL-адресах](#about-urls)
-   [Реализация интерфейсов обработчика протокола](#implementing-protocol-handler-interfaces)
    -   [Исеарчпротокол и ISearchProtocol2](#isearchprotocol-and-isearchprotocol2)
    -   [Иурлакцессор, IUrlAccessor2, IUrlAccessor3 и IUrlAccessor4](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [ипротоколхандлерсите](#iprotocolhandlersite)
-   [Реализация обработчиков фильтров для контейнеров](#implementing-filter-handlers-for-containers)
-   [Установка и регистрация обработчика протокола](#installing-and-registering-a-protocol-handler)
    -   [Рекомендации по регистрации обработчика протокола](#guidelines-for-registering-a-protocol-handler)
    -   [Регистрация обработчика протокола](#installing-and-registering-a-protocol-handler)
    -   [Регистрация обработчика типа файла обработчика протокола](#registering-the-protocol-handlers-file-type-handler)
-   [Проверка индексации элементов](#ensuring-that-your-items-are-indexed)
-   [См. также](#related-topics)

## <a name="about-urls"></a>Об URL-адресах

Поиск Windows использует URL-адреса для уникальной идентификации элементов в иерархии источника данных оболочки. URL-адрес, который является первым узлом в иерархии, называется [корнем поиска](-search-3x-wds-extidx-csm-searchroots.md). Поиск Windows начнет индексироваться в корне поиска, запрашивая, что обработчик протокола перечислит дочерние ссылки для каждого URL-адреса.

Типичная структура URL-адресов:


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



Синтаксис URL-адреса описан в следующей таблице.



| Синтаксис           | Описание                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | Определяет, какой обработчик протокола вызывать для URL-адреса.                                                                                                                                                           |
| {SID пользователя}       | Определяет контекст безопасности пользователя, в котором вызывается обработчик протокола. Если идентификатор безопасности (SID) пользователя не определен, обработчик протокола вызывается в контексте безопасности системной службы. |
| <path>     | Определяет иерархию хранилища, где каждая косая черта ("/") является разделителем между именами папок.                                                                                                            |
| <ItemID>   | Представляет уникальную строку, определяющую дочерний элемент (например, имя файла).                                                                                                                            |



 

Индексатор поиска Windows усекает окончательную косую черту по URL-адресам. В результате нельзя полагаться на существование последней косой черты для определения каталога и элемента. Обработчик протокола должен иметь возможность обрабатывать этот синтаксис URL-адреса. Убедитесь, что имя протокола, выбранное для обнаружения источника данных оболочки, не конфликтует с текущими. Мы рекомендуем использовать такое соглашение об именовании: `companyName.scheme` .

Дополнительные сведения о создании источника данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="implementing-protocol-handler-interfaces"></a>Реализация интерфейсов обработчика протокола

Для создания обработчика протокола требуется реализация следующих трех интерфейсов:

-   [**Исеарчпротокол**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) для управления объектами урлакцессор.
-   [**Иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) , чтобы предоставить свойства и выявить соответствующие фильтры для элементов в источнике данных оболочки.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) для фильтрации собственных файлов или перечисления и фильтрации файлов, хранимых иерархически.

Кроме трех обязательных интерфейсов, другие интерфейсы являются необязательными, и вы в libertyе реализовывать, какие необязательные интерфейсы наиболее подходят для выполнения задачи.

### <a name="isearchprotocol-and-isearchprotocol2"></a>Исеарчпротокол и ISearchProtocol2

Интерфейсы Сеарчпротокол инициализируют и управляют объектами Урлакцессор обработчика протокола. Интерфейс [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) является дополнительным расширением [**исеарчпротокол**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)и включает дополнительный метод для указания дополнительных сведений о пользователе и элементе.

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a>Иурлакцессор, IUrlAccessor2, IUrlAccessor3 и IUrlAccessor4

Интерфейсы [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) описаны в следующей таблице.



| Интерфейс                                                 | Описание                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | Для указанного URL-адреса интерфейс [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) предоставляет доступ к свойствам элемента, предоставляемого в URL-адресе. Он также может привязать эти свойства к фильтру, зависящему от обработчика протокола (т. е. к фильтру, отличному от того, который связан с именем файла). |
| [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (необязательно) | Интерфейс [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) расширяет [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) с помощью методов, которые получают кодовую страницу для свойств элемента и его отображаемого URL-адреса и получают тип элемента в URL-адресе (документ или каталог).                                    |
| [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (необязательно) | Интерфейс [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) расширяет [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) с помощью метода, который получает массив идентификаторов безопасности пользователя, позволяя узлу протокола поиска олицетворять этих пользователей для индексирования элемента.                                                      |
| [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (необязательно) | Интерфейс [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) расширяет функциональные возможности интерфейса [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) с помощью метода, который определяет, следует ли индексировать содержимое элемента.                                                                 |



 

Экземпляр объекта Урлакцессор создается и инициализируется объектом Сеарчпротокол. Интерфейсы [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) предоставляют доступ к важным сведениям с помощью методов, описанных в следующей таблице.



| Метод                                                                                        | Описание                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Иурлакцессор:: Жетластмодифиед**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | Возвращает время последнего изменения URL-адреса. Если это время новее, чем последний раз, когда индексатор обработал этот URL-адрес, вызываются обработчики фильтров (реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) для извлечения (возможно) измененных данных для этого элемента. Изменение времени для каталогов игнорируется. |
| [**Иурлакцессор:: подкаталог**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | Определяет, представляет ли URL-адрес папку, содержащую дочерние URL-адреса.                                                                                                                                                                                                                                                            |
| [**Иурлакцессор:: Биндтостреам**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | Выполняет привязку к [интерфейсу IStream](/windows/win32/api/objidl/nn-objidl-istream) , который представляет данные файла в пользовательском хранилище данных.                                                                                                                                                                           |
| [**Иурлакцессор:: Биндтофилтер**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | Привязывает к интерфейсу [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), зависящему от обработчика протокола, который может предоставлять свойства для элемента.                                                                                                                                                                                                                 |
| [**IUrlAccessor4:: Шаулдиндекситемконтент**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | Определяет, следует ли индексировать содержимое элемента.                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a>ипротоколхандлерсите

Интерфейс [**ипротоколхандлерсите**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) используется для создания экземпляра обработчика фильтра, который размещается в изолированном процессе. Соответствующий обработчик фильтра получается для указанного идентификатора постоянного класса (CLSID), класса хранилища документов или расширения имени файла. Преимущество запроса хост-процесса к [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) заключается в том, что ведущий процесс может управлять процессом поиска соответствующего обработчика фильтра и контролировать безопасность, связанную с вызовом обработчика.

## <a name="implementing-filter-handlers-for-containers"></a>Реализация обработчиков фильтров для контейнеров

При реализации иерархического обработчика протокола необходимо реализовать обработчик фильтра для контейнера, который перечисляет дочерние URL-адреса. Обработчик фильтра является реализацией интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Процесс перечисления — это цикл по методам [**IFilter::-фрагмента**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) и [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) интерфейса **IFilter** . Каждый дочерний URL-адрес предоставляется как значение свойства.

[**IFilter:: "**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) Возвращает свойства контейнера. Чтобы перечислить дочерние URL-адреса, **IFilter::** GetEnumerator возвращает один из следующих элементов:

-   [PKEY \_ Поиск \_ урлтоиндекс](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):

    URL-адрес элемента без времени последнего изменения. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) возвращает пропвариант, содержащий дочерний URL-адрес.

-   [PKEY \_ Поиск \_ урлтоиндексвисмодификатионтиме](../properties/props-system-search-urltoindexwithmodificationtime.md):

    URL-адрес и время последнего изменения. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) возвращает пропвариант, содержащий вектор URL-адреса дочернего элемента и время последнего изменения.

Возвращать [ \_ \_ урлтоиндексвисмодификатионтиме поиска PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) более эффективно, так как индексатор может немедленно определить, нужно ли индексировать элемент, не вызывая методы [**Исеарчпротокол:: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) и [**иурлакцессор:: жетластмодифиед**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .

В следующем примере кода демонстрируется возврат свойства [PKEY \_ Search \_ урлтоиндексвисмодификатионтиме](../properties/props-system-search-urltoindexwithmodificationtime.md) .

> [!IMPORTANT]
>
> (c) Корпорация Майкрософт (Microsoft Corporation). Все права защищены Все права защищены.

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> Компоненту [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) контейнера всегда следует перечислять все дочерние URL-адреса, даже если дочерние URL-адреса не изменялись, так как индексатор обнаруживает удаления с помощью процесса перечисления. Если выходные данные даты в [ \_ \_ урлтоиндексвисмодификатионтиме поиска PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) указывают на то, что данные не изменялись, индексатор не обновляет данные для этого URL-адреса.

 

## <a name="installing-and-registering-a-protocol-handler"></a>Установка и регистрация обработчика протокола

Установка обработчиков протоколов включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files, а затем регистрацию DLL-библиотек. Обработчики протоколов должны реализовать самостоятельную регистрацию для установки. Приложение установки может также добавить корень поиска и правила области, чтобы определить область обхода содержимого по умолчанию для источника данных оболочки, которая рассматривается в разделе [Проверка того, что элементы индексируются](#ensuring-that-your-items-are-indexed) в конце этого раздела.

### <a name="guidelines-for-registering-a-protocol-handler"></a>Рекомендации по регистрации обработчика протокола

При регистрации обработчика протокола следует следовать приведенным ниже рекомендациям.

-   Установщик должен использовать установщик EXE или MSI.
-   Необходимо указать заметки о выпуске.
-   Для каждой установленной надстройки необходимо создать запись «Установка и удаление программ».
-   Установщик должен задействовать все параметры реестра для конкретного типа файлов или хранить данные, распознаваемые текущей надстройкой.
-   Если предыдущая надстройка перезаписывается, установщик должен уведомить пользователя.
-   Если более новая надстройка перезаписала предыдущую надстройку, то должна быть возможность восстановить функциональность предыдущей надстройки и сделать ее надстройкой по умолчанию для этого типа файлов.
-   Установщик должен определить область обхода по умолчанию для индексатора, добавив корень поиска и правила области с помощью диспетчера области сканирования (CSM).

### <a name="registering-a-protocol-handler"></a>Регистрация обработчика протокола

Для регистрации компонента обработчика протокола необходимо внести в реестр записи четырнадцать, где:

-   *Версия \_ Параметр \_* "DIB ProgID" — это независимый от версии идентификатор ProgID реализации обработчика протокола.
-   *Версия \_ DEP \_ ProgID* — это зависимый от версии идентификатор ProgID реализации обработчика протокола.
-   *CLSID \_ 1* — это CLSID реализации обработчика протокола.

**Чтобы зарегистрировать обработчик протокола, выполните следующие действия.**

1.  Зарегистрируйте независимый от версии идентификатор ProgID со следующими ключами и значениями:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  Зарегистрируйте версию ProgID, зависимую от версии, со следующими ключами и значениями:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  Зарегистрируйте CLSID обработчика протокола со следующими ключами и значениями:

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  Зарегистрируйте обработчик протокола в службе поиска Windows. В следующем примере <Protocol Name> — это имя самого протокола, например File, MAPI и т. д.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    До Windows Vista:

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a>Регистрация обработчика типа файла обработчика протокола

Для регистрации обработчика типа файла обработчика протокола (который также называется расширением оболочки) необходимо создать две записи в реестре.

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a>Проверка индексации элементов

После реализации обработчика протокола необходимо указать, какие элементы оболочки должен индексировать обработчик протокола. Для инициации повторного индексирования можно использовать диспетчер каталогов (Дополнительные сведения см. [в разделе Использование диспетчера каталога](-search-3x-wds-mngidx-catalog-manager.md)). Кроме того, можно использовать диспетчер области сканирования (CSM) для настройки правил по умолчанию, указывающих URL-адреса, которые должен обходить индексатор (Дополнительные сведения см. [в разделе Использование диспетчера области сканирования](-search-3x-wds-extidx-csm.md) и [Управление правилами области действия](-search-3x-wds-extidx-csm-scoperules.md)). Вы также можете добавить корень поиска (Дополнительные сведения см. в разделе [Управление корнями поиска](-search-3x-wds-extidx-csm-searchroots.md)). Кроме того, можно выполнить процедуру, описанную в примере переиндексации в разделе [примеры пакета SDK для Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

Интерфейс [**исеарчкравлскопеманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) предоставляет методы, которые уведомляют механизм поиска контейнеров для обхода и (или) просмотра, а также элементы в этих контейнерах для включения или исключения при обходе или просмотре. В Windows 7 и более поздних версиях [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) расширяет **исеарчкравлскопеманажер** с помощью метода [**ISearchCrawlScopeManager2::**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) Method, который получает версию, которая информирует клиентов о том, изменилось ли состояние CSM.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Основные сведения о обработчиках протоколов](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Разработка обработчиков протоколов](-search-3x-wds-phaddins.md)
</dt> <dt>

[Уведомление индекса изменений](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Добавление значков и контекстных меню](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Пример кода: расширения оболочки для обработчиков протоколов](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Создание соединителя поиска для обработчика протокола](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Обработчики протокола отладки](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
