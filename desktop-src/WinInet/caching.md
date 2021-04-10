---
title: Кэширование (Windows Internet)
description: Функции WinINet имеют простую, но гибкую встроенную поддержку кэширования.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134914"
---
# <a name="caching-windows-internet"></a>Кэширование (Windows Internet)

Функции WinINet имеют простую, но гибкую встроенную поддержку кэширования. Все данные, полученные из сети, кэшируются на жестком диске и извлекаются для последующих запросов. Приложение может управлять кэшированием каждого запроса. Для HTTP-запросов с сервера большинство полученных заголовков также кэшируются. Когда HTTP-запрос выполняется из кэша, кэшированные заголовки также возвращаются вызывающему объекту. Это позволяет легко загружать данные независимо от того, поступают ли они из кэша или из сети.

Приложения должны правильно выделить буфер для получения нужных результатов при использовании постоянных функций кэширования URL-адресов. Дополнительные сведения см. [в разделе использование буферов](appendix-b-using-buffers.md).

## <a name="cache-behavior-during-response-processing"></a>Поведение кэша во время обработки ответа

Кэш WinINet совместим с директивами управления кэшем HTTP, описанными в RFC 2616. Директивы управления кэшем и флаги набора приложений определяют, что может быть кэшировано; Однако WinINet определяет, что на самом деле кэшируется на основе следующего критерия:

-   WinINet кэширует только ответы HTTP и FTP.
-   Только хорошо обрабатываемые ответы могут храниться в кэше и использоваться в ответ на последующий запрос. Правильно настроенные ответы определяются как ответы, которые успешно возвращают данные.
-   По умолчанию WinINet кэширует успешные ответы, если только директива Cache-Control не используется с сервера, или определенный приложением флаг, не Заказывающий, что ответ может не кэшироваться.
-   Как правило, ответы на команду GET кэшируются, если выполняются указанные выше требования. Ответы на команды размещения и POST не кэшируются при каких обстоятельствах.
-   Элементы будут кэшироваться даже при заполнении кэша. Если добавленный элемент помещает кэш на предельный размер, то запланирована очистка кэша. По умолчанию в кэше не гарантируется, что элементы остаются более чем 10 минут. Дополнительные сведения см. в разделе [Очистка кэша](#cache-scavenger) ниже.
-   По умолчанию протокол HTTPS кэшируется. Это управляется глобальным параметром, который не может быть переопределен директивами кэша, определяемыми приложением. Чтобы переопределить глобальный параметр, выберите приложение "Свойства обозревателя" на панели управления и перейдите на вкладку "Дополнительно". Установите флажок "не сохранять зашифрованные страницы на диск" в разделе "безопасность".

## <a name="cache-scavenger"></a>Очистка кэша

Очистка кэша периодически удаляет элементы из кэша. Если элемент добавляется в кэш, а кэш полон, элемент добавляется в кэш и планируется очистка кэша. Если очистка кэша завершает очистку, а кэш не достигает предела кэша, то для очистки планируется еще один цикл, когда в кэш добавляется другой элемент. Как правило, очистка планируется, когда добавленный элемент помещает кэш на предельный размер. По умолчанию минимальное время жизни в кэше составляет 10 минут, если иное не указано в директиве Cache-Control. При инициации очистки кэша не гарантируется, что самые старые элементы первыми будут удалены из кэша.

Кэш является общим для всех приложений WinINet на компьютере для одного и того же пользователя. Начиная с Windows Vista и Windows Server 2008 размер кэша задается равным 1 или 32-го размер диска, минимальный размер 8 МБ и максимальный размер 50 МБ.

## <a name="using-flags-to-control-caching"></a>Использование флагов для управления кэшированием

Флаги кэширования позволяют приложению управлять тем, когда и как оно использует кэш. Эти флаги можно использовать отдельно или в сочетании с параметром *dwFlags* в функциях, обращающихся к информации или ресурсам в Интернете. По умолчанию функции хранят все данные, загруженные из Интернета.

Для управления кэшированием можно использовать следующие флаги.



| Значение                                                                                                                                                  | Значение                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_кэш флагов Интернета \_ \_ Async**](api-flags.md)                                                                            | Этот флаг ни на что не влияет.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_кэш флагов Интернета в \_ \_ случае \_ \_ сбоя NET**](api-flags.md)                                                              | Возвращает ресурс из кэша в случае сбоя сетевого запроса ресурса из-за [ошибки \_ \_ \_ сброса подключения к Интернету](wininet-errors.md) или [ошибки подключения \_ \_ \_ к Интернету](wininet-errors.md) . Этот флаг используется [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                                                                              |
| [**\_ \_ кэш не Internet \_ Flag**](api-flags.md)                                                                              | Не кэширует данные локально или в любых шлюзах. Аналогично предпочтительному значению [**, \_ флаг Интернета \_ без \_ кэширования \_ записи**](api-flags.md).                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Указывает, что это отправка форм.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Интернет \_ Отправка флагов \_ из \_ кэша**](api-flags.md)[**\_ формы флагов Интернета \_ \_ Отправить**](api-flags.md) | Не выполняет сетевые запросы. Все сущности возвращаются из кэша. Если запрошенный элемент отсутствует в кэше, возвращается подходящая ошибка, например \_ файл ошибок \_ не \_ найден. Этот флаг используется только в функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .                                                                                                                                                                                                       |
| [**\_флаг Интернета \_ ФВД \_ назад**](api-flags.md)                                                                                  | Указывает, что функция должна использовать копию ресурса, который в данный момент находится в кэше Интернета. Дата окончания срока действия и другие сведения о ресурсе не проверяются. Если запрошенный элемент не найден в кэше Интернета, система пытается найти ресурс в сети. Это значение было представлено в Microsoft Internet Explorer 5 и связано с операциями « **вперед** » и « **назад** » обозревателя Internet Explorer. |
| [**\_Гиперссылка для Internet Flag \_**](api-flags.md)                                                                                 | Заставляет приложение перезагружать ресурс, если срок действия не истек и время последнего изменения не возвращалось, когда ресурс был сохранен в кэше.                                                                                                                                                                                                                                                                                                                  |
| [**\_флаг Интернета \_ сделать \_ постоянным**](api-flags.md)                                                                    | Больше не поддерживается.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_флаг Интернета \_ должен \_ кэшировать \_ запрос**](api-flags.md)                                                             | Вызывает создание временного файла, если файл не может быть кэширован. Это аналогично предпочтительному значению, параметру [**Internet \_ Flag \_ требуется \_ файл**](api-flags.md).                                                                                                                                                                                                                                                                            |
| [**для \_ флага Интернета \_ требуется \_ файл**](api-flags.md)                                                                                | Вызывает создание временного файла, если файл не может быть кэширован.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_флаг Интернета \_ без \_ записи в кэш \_**](api-flags.md)                                                                     | Отклоняет все попытки функции для хранения данных, загруженных из Интернета в кэш. Этот флаг необходим, если приложению не требуется хранить загруженные ресурсы локально.                                                                                                                                                                                                                                                               |
| [**\_флаг Интернета \_ нет \_ пользовательского интерфейса**](api-flags.md)                                                                                        | Отключает диалоговое окно "файл cookie". Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только HTTP-запросы).                                                                                                                                                                                                                                                                                          |
| [**\_отключить флаг \_ Интернета**](api-flags.md)                                                                                     | Предотвращает отправку запросов в сеть приложением. Все запросы разрешаются с помощью ресурсов, хранящихся в кэше. Если ресурс отсутствует в кэше, возвращается подходящая ошибка, например \_ файл ошибок \_ не \_ найден.                                                                                                                                                                                                                            |
| [**параметр INTERNET \_ Flag \_ pragma \ \_ Cache**](api-flags.md)                                                                      | Вызывает принудительное разрешение запроса сервером-источником, даже если кэшированная копия существует на прокси-сервере. Функция [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только для запросов HTTP и HTTPS) и функция [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) используют этот флаг.                                                                                                                                                                                               |
| [**\_Перезагрузка флага Интернета \_**](api-flags.md)                                                                                       | Заставляет функцию получить запрошенный ресурс непосредственно из Интернета. Загружаемые сведения хранятся в кэше.                                                                                                                                                                                                                                                                                                                     |
| [**\_ \_ Повторная синхронизация ФЛАГа Интернета**](api-flags.md)                                                                         | Заставляет приложение выполнять условную загрузку ресурса из Интернета. Если версия, хранящаяся в кэше, является актуальной, сведения загружаются из кэша. В противном случае сведения перегружаются с сервера.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Функции постоянного кэширования

Клиенты, которым требуются постоянные службы кэширования, используют функции постоянного кэширования, чтобы позволить приложениям сохранять данные в локальной файловой системе для последующего использования, например в ситуациях, когда канал с низкой пропускной способностью ограничивает доступ к данным, или доступ вообще недоступен.

Функции кэширования обеспечивают постоянное кэширование и просмотр в автономном режиме. Если флаг [**Internet \_ флаг \_ \_ \_ записи кэша явно не**](api-flags.md) указывает кэширование, функции кэшируют все данные, загруженные из сети. Ответы на POST данные не кэшируются.

## <a name="using-the-persistent-url-cache-functions"></a>Использование функций кэша постоянного URL-адреса

Следующие функции кэша постоянных URL-адресов позволяют приложению получать доступ к информации, хранящейся в кэше, и управлять ею.



| Функция                                                           | Описание                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**коммитурлкачинтря**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Кэширует данные в указанном файле в хранилище кэша и связывает их с заданным URL-адресом.                                                                  |
| [**коммитурлкачинтрив**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Кэширует данные в указанном файле в хранилище кэша и связывает их с заданным URL-адресом.                                                                  |
| [**креатеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Выделяет запрошенное хранилище кэша и создает локальное имя файла для сохранения записи кэша, соответствующей имени источника.                           |
| [**креатеурлкачеграуп**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Создает идентификатор группы кэша.                                                                                                                       |
| [**делетеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Удаляет файл, связанный с именем источника из кэша, если файл существует.                                                                          |
| [**делетеурлкачеграуп**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Освобождает объект **GROUPID** и любое связанное состояние в файле индекса кэша.                                                                                      |
| [**финдклосеурлкаче**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Закрывает указанный маркер перечисления.                                                                                                                      |
| [**финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Начинает перечисление кэша.                                                                                                                          |
| [**финдфирстурлкачинтрекс**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Начинает фильтрованное перечисление кэша.                                                                                                                   |
| [**финднекстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Извлекает следующую запись в кэше.                                                                                                                        |
| [**финднекстурлкачинтрекс**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Извлекает следующую запись в отфильтрованном перечислении кэша.                                                                                                     |
| [**жетурлкачинтринфо**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Извлекает сведения о записи кэша.                                                                                                                    |
| [**жетурлкачинтринфоекс**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Выполняет поиск URL-адреса после преобразования любых кэшированных перенаправлений, которые будут применены в автономном режиме с помощью [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).           |
| [**реадурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Считывает кэшированные данные из потока, открытого с помощью [**ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                            |
| [**ретриевеурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Извлекает запись кэша из кэша в виде файла.                                                                                                 |
| [**ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Предоставляет наиболее эффективный и независимый от реализации способ доступа к данным кэша.                                                                   |
| [**сетурлкачинтриграуп**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Добавляет или удаляет записи из группы кэша.                                                                                                                   |
| [**сетурлкачинтринфо**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Задает указанные элементы структуры [**\_ \_ \_ сведений об элементе кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .                                                |
| [**унлоккурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Разблокирует запись кэша, которая была заблокирована, когда файл был извлечен для использования из кэша [**ретриевеурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea). |
| [**унлоккурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Закрывает поток, полученный с помощью [**ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                                           |



 

### <a name="enumerating-the-cache"></a>Перечисление кэша

Функции [**финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) и [**финднекстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) перечисляют сведения, хранящиеся в кэше. [**Финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) запускает перечисление, используя шаблон поиска, буфер и размер буфера для создания маркера и возврата первой записи кэша. [**Финднекстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) принимает маркер, созданный [**финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), буфер и размер буфера, чтобы вернуть следующую запись кэша.

Обе функции хранят информационную структуру [**\_ \_ записи \_ в кэше Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) в буфере. Размер этой структуры различается для каждой записи. Если размер буфера, передаваемый любой из функций, недостаточен, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную для \_ буфера. Переменная размера буфера содержит размер буфера, который был необходим для получения этой записи кэша. Буфер, размер которого определяется переменной размера буфера, должен быть выделен, а функция должна вызываться повторно с новым буфером.

Структура [**\_ \_ \_ сведений о записи кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) содержит размер структуры, URL-адрес кэшированной информации, имя локального файла, тип записи кэша, число использований, скорость попаданий, размер, время последнего изменения, срок действия, Последний доступ, время последней синхронизации, сведения о заголовке, размер сведений о заголовке и расширение имени файла.

Функция [**финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) принимает шаблон поиска, буфер, в котором хранится структура [**\_ \_ \_ сведений об элементе кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) , и размер буфера. В настоящее время реализован только шаблон поиска по умолчанию, который возвращает все записи кэша.

После перечисления кэша приложение должно вызвать [**финдклосеурлкаче**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) , чтобы закрыть обработчик перечисления кэша.

В следующем примере отображается URL-адрес каждой записи кэша в поле со списком, **IDC \_ качелист**. Он использует максимальный \_ \_ Размер записи \_ кэша \_ для первоначального выделения буфера, поскольку ранние версии API WinInet не перечисляют кэш должным образом. Более поздние версии выполняют перечисление кэша в правильном объеме и не имеют ограничения на размер кэша. Все приложения, работающие на компьютерах с версией API WinINet из Internet Explorer 4,0, должны выделить буфер требуемого размера. Дополнительные сведения см. [в разделе использование буферов](appendix-b-using-buffers.md).


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a>Получение сведений о записи кэша

Функция [**жетурлкачинтринфо**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) позволяет получить структуру [**\_ \_ \_ сведений об элементе кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) для указанного URL-адреса. Эта структура содержит размер структуры, URL-адрес кэшированной информации, имя локального файла, тип записи кэша, число использований, коэффициент попаданий, размер, время последнего изменения, срок действия, Последний доступ, время последней синхронизации, сведения о заголовке, размер сведений о заголовке и расширение имени файла.

[**Жетурлкачинтринфо**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) принимает URL-адрес, буфер для структуры [**\_ \_ \_ сведений об элементе кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) и размер буфера. Если URL-адрес найден, сведения копируются в буфер. В противном случае происходит сбой функции, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ВОЗВРАЩАЕТ \_ файл ошибки \_ не \_ найден. Если размер буфера недостаточен для хранения данных записи кэша, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную для \_ буфера. Размер, необходимый для получения сведений, хранится в переменной размера буфера.

[**Жетурлкачинтринфо**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) не выполняет синтаксический анализ URL-адреса, поэтому URL-адрес, содержащий привязку ( \# ), не будет найден в кэше, даже если ресурс кэшируется. Например, если передается URL-адрес " https://example.com/example.htm\#sample ", функция возвращает \_ файл ошибки \_ не \_ найден, даже если https://example.com/example.htm в кэше находится "".

В следующем примере извлекается информация о записи кэша для указанного URL-адреса. Затем функция отображает сведения о заголовке в поле ввода **\_ качедумп IDC** .


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a>Создание записи кэша

Приложение использует функции [**креатеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) и [**коммитурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) для создания записи кэша.

[**Креатеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) принимает URL-адрес, ожидаемый размер файла и расширение имени файла. Затем функция создает локальное имя файла для сохранения записи кэша, которая соответствует URL-адресу и расширению имени файла.

С помощью имени локального файла запишите данные в локальный файл. После того как данные записаны в локальный файл, приложение должно вызвать [**коммитурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).

[**Коммитурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) принимает URL-адрес, имя локального файла, срок действия, время последнего изменения, тип записи кэша, сведения о заголовке, размер сведений о заголовке и расширение имени файла. Затем функция кэширует данные в файле, указанном в хранилище кэша, и связывает его с заданным URL-адресом.

В следующем примере используется локальное имя файла, созданное предыдущим вызовом [**креатеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), которое хранится в текстовом поле **IDC \_ локальный_файл**, чтобы сохранить текст из текстового поля, **IDC \_ качедумп**, в записи кэша. После записи данных в файл с помощью **fopen**, **fprintf** и **фклосе** запись фиксируется с помощью [**коммитурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a>Удаление записи кэша

Функция [**делетеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) принимает URL-адрес и удаляет связанный с ним файл кэша. Если файл кэша не существует, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ВОЗВРАЩАЕТ \_ файл ошибки \_ не \_ найден. Если файл кэша в настоящий момент заблокирован или используется, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает \_ отказ в доступе \_ . Файл удаляется после снятия блокировки.

### <a name="retrieving-cache-entry-files"></a>Получение файлов записей кэша

Для приложений, которым требуется имя файла ресурса, используйте функции [**ретриевеурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) и [**унлоккурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) . Приложения, которым не требуется имя файла, должны использовать функции [**ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**реадурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)и [**унлоккурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) для получения информации в кэше.

[**Ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) не выполняет синтаксический анализ URL-адреса, поэтому URL-адрес, содержащий привязку ( \# ), не будет найден в кэше, даже если ресурс кэшируется. Например, если передается URL-адрес " https://example.com/example.htm\#sample ", функция возвращает \_ файл ошибки \_ не \_ найден, даже если https://example.com/example.htm в кэше находится "".

[**Ретриевеурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) принимает URL-адрес, буфер, в котором хранится структура [**\_ \_ \_ сведений о записи кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) , и размер буфера. Функция извлекается и блокируется для вызывающего объекта.

После того как данные в файле будут использованы, приложение должно вызвать [**унлоккурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) для разблокировки файла.

### <a name="cache-groups"></a>Группы кэша

Чтобы создать группу кэша, необходимо вызвать функцию [**креатеурлкачеграуп**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) , чтобы создать объект **GROUPID** для группы кэша. Записи можно добавить в группу кэша, предоставив URL-адрес записи кэша и \_ флаг добавления группы кэша Интернета в \_ \_ функцию [**сетурлкачинтриграуп**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) . Чтобы удалить запись кэша из группы, передайте ее URL-адрес и параметр \_ удаления группы кэша Интернета \_ \_ в [**сетурлкачинтриграуп**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).

Функции [**финдфирстурлкачинтрекс**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) и [**финднекстурлкачинтрекс**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) можно использовать для перечисления записей в указанной группе кэша. После завершения перечисления функция должна вызвать [**финдклосеурлкаче**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).

## <a name="handling-structures-with-variable-size-information"></a>Обработка структур со сведениями о размере переменных

Кэш может содержать сведения о размере переменных для каждого хранимого URL-адреса. Это отражено в структуре [**\_ сведений в \_ записи \_ кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) . Когда функции кэша возвращают эту структуру, они создают буфер, который всегда имеет размер данных [**\_ \_ записи \_ кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) плюс любые сведения о размере переменной. Если элемент указателя не **равен null**, он указывает на область памяти сразу после структуры. При копировании буфера, возвращенного функцией, в другой буфер, необходимо исправить элементы указателя, чтобы они указывали на соответствующее место в новом буфере, как показано в следующем примере.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Некоторые функции кэша завершаются ошибкой, \_ недостаточным \_ сообщение об ошибке буфера, если указать буфер, который слишком мал для хранения данных записи кэша, полученных функцией. В этом случае функция также возвращает необходимый размер буфера. Затем можно выделить буфер соответствующего размера и вызвать функцию снова.

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
