---
description: В следующей таблице описаны изменения между Microsoft Internet Explorer 6 и Windows Internet Explorer 8.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Изменения браузера IE 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7abf978d2211a03b59a78847a66efc21f3213c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909975"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Приложение 1. изменения браузера Internet Explorer 6 для Internet Explorer 8

В следующей таблице описаны изменения между Microsoft Internet Explorer 6 и Windows Internet Explorer 8.



Проектирование изменений из Internet Explorer 6 в Internet Explorer 7

Проектирование изменений из Internet Explorer 7 в Internet Explorer 8

$ {ROWSPAN2} $Internet обозреватель версий $ {Remove} $  

Проверьте код на наличие неверно определенных случаев для Internet Explorer 6, Windows Internet Explorer 7 или Internet Explorer 8 с помощью [сканирования строки агента пользователя, векторов версий или условных комментариев](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85)).

-   Когда строка агента пользователя (UA) обнаруживает сервер, принимающий более короткие строки UA, пользователи видят [страницу ошибки](https://www.enhanceie.com/ua.aspx).

<!-- -->

-   Представление совместимости Internet Explorer 8, включенное по умолчанию для сайтов интрасети, отправляет строку агента пользователя Internet Explorer 7. Чтобы отличить Internet Explorer 7 от представления совместимости, найдите новый [токен Trident](/archive/blogs/ie/).

$ {ROWSPAN3} $ обновления соответствия стандартам

-   Применяется к [указанным режимам документов](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)).
-   [Режим просмотра совместимости Internet Explorer 8](/archive/blogs/ie/), который по умолчанию включен для сайтов интрасети, обычно [возвращает обновления стандартов из Internet Explorer 7 в Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).
-   Используйте заголовок HTTP [EmulateIE7 X-UA-Compatible](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) или элемент **meta** , чтобы включить представление совместимости на веб-сайтах или в конкретных веб-страницах.

$ {REMOVE} $  

Исключение режима совместимости. не требуется вносить изменения в соответствие стандартам для веб-страниц, которые задают режим "несовместимость" (путем установки для параметра DOCTYPE "соответствие стандартам" значение "OFF").

Применяется к стандартам Internet Explorer 7 или "ограниченному" режиму и выше:

-   [Журналы XML](/previous-versions/windows/internet-explorer/ie-developer/) в первой строке исходного кода больше не вызывают ошибок в объявлениях DOCTYPE.
-   Блочная [модель](/previous-versions/windows/internet-explorer/ie-developer/) область пересечения содержимого переполнена и больше не автоматически расширяет рамку DIV в соответствии с содержимым.
-   [Некоторые фильтры CSS](/previous-versions/windows/internet-explorer/ie-developer/) (например, \* HTML, \_ символы подчеркивания и/ \* \* /) не поддерживаются.
-   Создается [только элемент самого внешнего объекта во вложенных объектах](/previous-versions/windows/internet-explorer/ie-developer/) .
-   [Приложения, которые используют элемент SELECT](/previous-versions/windows/internet-explorer/ie-developer/) для получения HWND для использования с интерфейсами API Microsoft Win32, могут нарушить работу, так как [элемент SELECT](/archive/blogs/ie/) теперь является безоконным элементом управления.
-   [Формат определения канала (CDF)](/previous-versions/aa740486(v=msdn.10)) не поддерживается в пользу RSS-каналов.
-   [Xbm](/previous-versions/aa740486(v=msdn.10)), формат создания образов, предназначенный для систем на основе X, не поддерживается.
-   [Базовые теги](/previous-versions/aa740486(v=msdn.10)) за пределами головного документа не допускаются.

Применяется к стандартному режиму Internet Explorer 8 и выше:

-   [Незакрытые элементы P](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) автоматически закрываются, когда за ними следуют элементы [**Table**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx), [**Form**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx), [**noframes**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx)или [**script**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx) .
-   [Неверно сформированный HTML](/archive/blogs/ie/site-compatibility-and-ie8) не поддерживается в пользу правильно сформированной допустимой разметки.
-   Синтаксис [атрибута ClassName](/archive/blogs/ie/site-compatibility-and-ie8) не поддерживается в пользу синтаксиса "class".
-   [Коллекция Attributes](/archive/blogs/ie/site-compatibility-and-ie8) не содержит все возможные атрибуты, распознаваемые Windows Internet Explorer.
-   [Упорядочивание атрибутов изменилось](/archive/blogs/ie/site-compatibility-and-ie8), влияет на коллекцию атрибутов, innerHTML и outerHTML.
-   [GetElementById](/archive/blogs/ie/site-compatibility-and-ie8) учитывает регистр и не выполняет поиск атрибутов имени.
-   [Селекторы универсальных префиксов CSS](/archive/blogs/ie/site-compatibility-and-ie8) (т \\ . е. синтаксис v: \* ) не поддерживаются в пользу явных имен тегов.
-   [Выражения CSS](/archive/blogs/ie/site-compatibility-and-ie8) не поддерживаются в пользу улучшенной поддержки CSS или логики DHTML.
-   Код, предназначенный для пользовательских методов объекта JSON, может конфликтовать с [новым собственным объектом JSON](/archive/blogs/ie/site-compatibility-and-ie8) в Internet Explorer 8.
-   Отменить начальные [Свойства](/archive/blogs/ie/site-compatibility-and-ie8) для объекта куррентстиле возвращают свое начальное значение.
-   [Значения неуказанных свойств](/archive/blogs/ie/site-compatibility-and-ie8) объекта стиля объекта куррентстиле возвращают пустую строку (например, в меню ASP.NET и в записи блога об [белой ошибке визуализации IE8](/archive/blogs/giorgio/) ).

<!-- -->

-   Для сайтов и приложений, в которых важна доступность специальных возможностей, обновите [синтаксис ARIA во всех режимах рендеринга Internet Explorer](/archive/blogs/ie/).
-   Просмотрите [полный список обновлений CSS из Internet Explorer 6 в Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Усовершенствования системы безопасности

-   Применяется независимо от режима документа.
-   Вы можете отключить функции безопасности с помощью [Групповая политика](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab).

<!-- -->

-   Обход [окна. средство открытия](/previous-versions/aa740486(v=msdn.10)) в окне запроса. Close не разрешен.
-   [Защита кэширования объектов](/previous-versions/windows/internet-explorer/ie-developer/) включена по умолчанию, что блокирует доступ к ссылкам на объекты, когда пользователи обращаются к новому домену (применяется к Internet Explorer 6 и более поздним версиям в Windows XP с пакетом обновления 2 (SP2) и более поздних версий).
-   [Сценарии DHTML](/previous-versions/windows/internet-explorer/ie-developer/) по умолчанию отключены.
-   [Скрипты, записывающие в строку состояния](/previous-versions/windows/internet-explorer/ie-developer/) , блокируются.
-   [Создание URL-адреса может завершиться ошибкой](/previous-versions/windows/internet-explorer/ie-developer/) , если URL-адреса не соответствуют рекомендациям RFC.
-   Страницы [HTTPS отображают страницу ошибки](/previous-versions/windows/internet-explorer/ie-developer/) , если сайт настроен только для SSLv2 или если сертификат безопасности сайта устарел или недействителен, содержит ошибки или имеет слабые шифры.
-   Поддерживаются только [международные доменные имена в формате Punycode](/previous-versions/windows/internet-explorer/ie-developer/) . Другие форматы, такие как ANSI и UTF-8, блокируются.
-   [Междоменные URL-адреса сценариев](/previous-versions/windows/internet-explorer/ie-developer/), перенаправленная навигация в объектах модели DOM и Навигация по кадрам заблокированы.
-   [Модальные или немодальные диалоговые окна](/previous-versions/aa740486(v=msdn.10)) , созданные из скрипта, могут казаться [немного больше](/archive/blogs/ie/).
-   [Небезопасные протоколы](/previous-versions/aa740486(v=msdn.10)) View-Source, Gopher (на уровне WinInet) и Telnet не работают.

<!-- -->

-   [Фильтр XSS](/archive/blogs/ie/) включен по умолчанию, который блокирует шаблоны скриптов, которые чаще всего похожи на атаки типа-1 XSS, если не отключить их через заголовок HTTP X-XSS-Protection.
-   Междоменные и междокументные атаки с обменом данными, такие как [src в сценариях](/archive/blogs/jscript/) , не поддерживаются в пользу более безопасных [функций XDM и XDR AJAX](/archive/blogs/ie/).
-   Сайты с поддержкой AJAX, которые [вручную управляют хэшем URL-адреса](/previous-versions//cc891506(v=vs.85)) , могут быть разорваны новым свойством навигации Window. Location. hash.
-   [Новые функции AJAX](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) , такие как [XDM](/archive/blogs/ie/) , имеют [**собственные свойства**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) , которые могут конфликтовать с существующими пользовательскими свойствами.
-   [Элемент управления отправка файла](/archive/blogs/ie/) отправляет на сервер только путь к файлу, а не полный путь.
-   Выполнение HTML-кода или скрипта, доставляемого с помощью [ \* типа MIME "Image/"](/archive/blogs/ie/) , заблокировано.
-   При [навигации по кадру верхнего уровня](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) на сайт в другом контексте безопасности открывается новое окно или вкладка, а не выполняется Навигация в существующем фрейме.
-   Сценарий в кодировке [UTF-7](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) принудительно преобразуется в формат Windows-1252, что может привести к отрисовке обычного текста.
-   На [страницах смешанного режима HTTP/HTTPS](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) отображается диалоговое окно, по умолчанию отображающее только безопасные элементы (а не предыдущее небезопасное по умолчанию). Пользователи могут по ошибке [выбрать блокировку элементов HTTP](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0), таких как изображения ключей.
-   [DEP/NX включен по умолчанию](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx), который блокирует определенные надстройки (то есть элементы управления ActiveX и COM-объекты), созданные с помощью более старых версий ATL, из кода, который помечен как "не исполняемый" в памяти.
-   [Содержимое, возвращаемое веб-прокси](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) , блокируется, если в ответ на запрос подключения к исходному серверу не установлен туннель SSL.

Изменения архитектуры

-   Применяется независимо от документа или режима совместимости.

<!-- -->

-   [Защищенный режим](/previous-versions/windows/internet-explorer/ie-developer/) включен по умолчанию для [зон Интернета, интрасети и ограниченных сайтов](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85)). Этот режим [блокирует расширения браузера, которые могут представлять угрозу безопасности](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) от запуска и [более низкого уровня прав доступа к процессам с более высоким уровнем привилегий](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85)), таким как меню "Пуск", панель управления и реестр Microsoft Windows (применяется к Internet Explorer 7 и более поздним версиям в Windows Vista и более поздних версиях).

<!-- -->

-   [Обновление защищенного режима](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85)): интрасеть работает на среднем (а не на низком) уровне целостности по умолчанию.
-   [Слабо связанный Internet Explorer](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) может блокировать надстройки (то есть элементы ActiveX и COM-объекты), которые выполняют одно из следующих действий:
    -   Используйте методы иерархии Windows для наведения фрейма пользовательского интерфейса и окон вкладок (которые теперь выполняются в отдельных процессах на разных уровнях целостности).
    -   Создайте подкласс фрейма пользовательского интерфейса (теперь на среднем уровне целостности) из процесса вкладки с низкой целостностью.
    -   Используйте неподдерживаемые методы обмена сообщениями между рамкой пользовательского интерфейса и вкладками.



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устранение совместимости приложений при переходе на Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
