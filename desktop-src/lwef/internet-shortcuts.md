---
title: Ярлыки Интернета
description: Объект ярлык Интернета используется для создания ярлыков на рабочем столе для веб-сайтов.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Объекты ярлыков Интернета
- Элементы управления WebBrowser
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aba53c320ed740fe7d91a2425b4d47d66e28d78aa35e4ce893efeed12380c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749412"
---
# <a name="internet-shortcuts"></a>Ярлыки Интернета

Объект ярлык Интернета используется для создания ярлыков на рабочем столе для веб-сайтов. Как и ярлыки для элементов в файловой системе, ярлыки Интернета имеют форму значка на рабочем столе. Когда пользователь щелкает значок, запускается браузер и отображается сайт, связанный с ярлыком.

Обсуждаются следующие темы.

-   [Создание ярлыков Интернета](#creating-internet-shortcuts)
    -   [Создание ярлыка Интернета из элемента управления WebBrowser](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Создание ярлыка из Интернета на основе URL-адреса](#creating-an-internet-shortcut-from-a-url)
-   [доступ к свойству служба хранилища](#accessing-property-storage)
-   [Интерфейсы](#interfaces)
    -   [интерфейсы OLE](#ole-interfaces)
    -   [Интерфейсы оболочки](#shell-interfaces)
-   [Функции](#functions)
    -   [Функции ярлыка Интернета](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Создание ярлыков Интернета

Можно создать ярлык Интернета с помощью элемента управления WebBrowser или URL-адреса страницы.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Создание ярлыка Интернета из элемента управления WebBrowser

Если в приложении размещается элемент управления WebBrowser, можно использовать объект ярлыка Интернета для создания ярлыков следующим образом.

1.  Создайте экземпляр объекта ярлыка Интернета с [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), используя идентификатор класса CLSID \_ интернетшорткут.
2.  Передайте указатель на интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) WebBrowser в объект ярлыка Интернета с помощью [IObjectWithSite:: SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).
3.  Вызовите метод [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) объекта ярлыка Интернета, если нужно создать ярлык для страницы, просматриваемой элементом управления WebBrowser.

Ярлык будет создан в расположении, указанном в [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). Это расположение позволяет элементу управления WebBrowser восстанавливать свое состояние, что включает в себя задачу загрузки правильных документов в наборы рамок.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Создание ярлыка из Интернета на основе URL-адреса

Можно также создать ярлык Интернета, если у вас есть URL-адрес страницы, на которую необходимо установить связь.

1.  Создайте экземпляр объекта ярлыка Интернета с [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), используя CLSID \_ интернетшорткут CLSID.
2.  Используйте метод [иуниформресаурцелокатор:: SetURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) , чтобы задать URL-адрес в ярлыке.
3.  Используйте метод [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , чтобы сохранить файл ярлыка в нужном месте.

## <a name="accessing-property-storage"></a>доступ к свойству служба хранилища

Объект ярлык Интернета содержит несколько свойств, доступ к которым можно получить с помощью интерфейса [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) объекта с помощью следующей процедуры.

1.  Получите интерфейс [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) , вызвав [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) с IID \_ IPropertySetStorage.
2.  Чтобы получить интерфейс Интернетсите, обратитесь к набору данных свойства ярлыка Интернета, вызвав [IPropertySetStorage:: Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) with FMTID \_ интшкут или FMTID \_ ипропертистораже. [](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage)
3.  Прочтите сведения о хранилище свойств с помощью [ипропертистораже:: реадмултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) , ПЕРЕДАВ соответствующий идентификатор свойства.

В [версии 4,70 или более поздней](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) Shell32.dll можно также получить интерфейс [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) , вызвав [**ишеллфолдер:: биндтостораже**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) с параметром *Пидл* , для которого задано значение. Для файла URL и параметра *riid* задано значение IID \_ IPropertySetStorage.

Для FMTID интшкут можно запросить следующие идентификаторы свойств \_ .



| PROPID               | Тип варианта | Описание                                 |
|----------------------|--------------|---------------------------------------------|
| Идентификатор процесса \_ — \_ URL-адрес         | VT \_ LPWSTR   | URL-адрес, на который указывает ярлык             |
| Идентификатор процесса \_ — \_ имя        | VT \_ LPWSTR   | Имя ярлыка Интернета               |
| PID \_ — \_ воркингдир  | VT \_ LPWSTR   | Рабочий каталог для ярлыка          |
| PID \_ — это \_ сочетание клавиш      | VT \_ UI2      | Сочетание клавиш для ярлыка                     |
| PID \_ — \_ шовкмд     | VT \_ I4       | Отобразить команду для ярлыка                   |
| PID \_ — \_ икониндекс   | VT \_ I4       | Индекс значка                           |
| PID \_ — \_ иконфиле    | VT \_ LPWSTR   | Файл, содержащий значок                 |
| PID \_ — \_ вхатснев    | VT \_ LPWSTR   | Новый текст                             |
| PID \_ является \_ автором      | VT \_ LPWSTR   | Автор                                      |
| PID \_ — \_ Описание | VT \_ LPWSTR   | Текст описания для сайта                    |
| Идентификатор процесса \_ — \_ комментарий     | VT \_ LPWSTR   | Комментарий с заметками пользователя                      |
| Идентификатор \_ процесса \_ перемещен      | Логическое значение VT \_     | True, если ярлык перемещен в первый раз |



 

Для FMTID интернетсите можно запросить следующие идентификаторы свойств \_ .



| PROPID                     | Тип варианта | Описание                                       |
|----------------------------|--------------|---------------------------------------------------|
| PID \_ интсите \_ вхатснев     | VT \_ LPWSTR   | Новый текст                                   |
| Идентификатор PID \_ интсите \_ Author       | VT \_ LPWSTR   | Автор                                            |
| PID \_ интсите \_ LASTVISIT    | VT \_ fileTime | Время последнего посещения сайта                        |
| PID \_ интсите \_ ластмод      | VT \_ fileTime | Время последнего изменения сайта                       |
| PID \_ интсите \_ виситкаунт   | VT \_ UI4      | Число посещений пользователей                  |
| \_Описание PID интсите \_  | VT \_ LPWSTR   | Текст описания для сайта                          |
| \_Комментарий ИНТСИТЕ \_ PID      | VT \_ LPWSTR   | Комментарий с заметками пользователя                            |
| \_ \_ Флаги PID интсите        | VT \_ UI4      | Указывает использование \_ флагов пидисф (см. ниже)       |
| PID \_ интсите \_ контентлен   | Н/Д          | Сейчас не поддерживается                           |
| PID \_ интсите \_ контенткоде  | Н/Д          | Сейчас не поддерживается                           |
| PID \_ интсите \_ рекурсия      | Н/Д          | Сейчас не поддерживается                           |
| PID \_ интсите \_ Контрольные значения        | Н/Д          | Сейчас не поддерживается                           |
| \_интсите по \_ ПОДписке PID | VT \_ UI8      | Значение СУБСКРИПТИОНКУКИЕ для диспетчера подписки |
| \_ \_ URL-адрес интсите PID          | VT \_ LPWSTR   | URL-адрес, на который указывает ярлык                   |
| \_название PID интсите \_        | VT \_ LPWSTR   | Название                                             |
| Идентификатор процесса \_ интсите \_ кодовая страница     | VT \_ UI4      | Кодовая страница документа                          |
| Идентификатор PID \_ интсите \_ отслеживания     | Н/Д          | Сейчас не поддерживается                           |
| PID \_ интсите \_ икониндекс    | VT \_ I4       | Индекс значка                                 |
| PID \_ интсите \_ иконфиле     | VT \_ LPWSTR   | Файл, содержащий значок                       |
| Идентификатор процесса \_ интсите \_ перемещен       | VT \_ UI4      | Запись была добавлена из-за роуминга                |



 

Ниже приведены флаги Интернет-сайта.



| Флаг                    | Описание                                |
|-------------------------|--------------------------------------------|
| ПИДИСФ \_ рецентличанжед | Указывает, что сайт был недавно изменен |
| ПИДИСФ \_ качедстикки    | Сейчас не поддерживается                    |
| ПИДИСФ \_ качеимажес     | Сейчас не поддерживается                    |
| ПИДИСФ \_ фолловалллинкс  | Сейчас не поддерживается                    |



 

Для перемещаемого журнала Интернета используются следующие значения.



| Значение PID \_ интсите \_ перемещено         | Описание                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Значение не задано или не ПИДИСР \_ в актуальном \_ \_ состоянии | Эта запись кэша не была изменена роумингом.                                                                                                                       |
| ПИДИСР \_ требуется \_ Добавить                    | Эта запись кэша была добавлена в кэш роумингом. Установите ПИДИСР \_ в актуальном \_ \_ состоянии после завершения обработки записи.                                                   |
| ПИДИСР \_ требуется \_ обновление                 | Эта запись кэша уже существовала на локальном компьютере, но была обновлена роумингом. Установите ПИДИСР \_ в актуальном \_ \_ состоянии после завершения обработки записи.                 |
| ПИДИСР \_ требуется \_ удалить                 | Роуминг обнаружил, что эта запись кэша должна быть удалена. Например, пользователь мог очистить свой журнал браузера. Удалите запись с помощью Делетеурлкачинтри. |



 

## <a name="interfaces"></a>Интерфейсы

Объект ярлыка Интернета предоставляет ряд интерфейсов.

### <a name="ole-interfaces"></a>интерфейсы OLE

-   [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [IOleCommandTarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [IObjectWithSite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Интерфейсы оболочки

-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**иекстрактикон**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**иневшорткусук**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**ишеллекстинит**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**ишелллинк**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**ишеллпропшитекст**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**икуеринфо**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>Функции

Существует несколько служебных функций, которые можно использовать с объектом ярлыка Интернета.

### <a name="internet-shortcut-utility-functions"></a>Функции ярлыка Интернета

-   [**инетисоффлине**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**мимеассоЦиатиондиалог**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**транслатеурл**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**урлассоЦиатиондиалог**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 