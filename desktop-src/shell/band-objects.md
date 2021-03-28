---
description: Панель обозревателя появилась в обозревателе Microsoft Internet Explorer 4,0, чтобы предоставить область просмотра, смежную с областью браузера.
title: Создание пользовательских панелей обозревателя, панелей инструментов и рабочих столов
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104557064"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Создание настраиваемых панелей обозревателя, панелей инструментов и полос рабочих столов

Панель обозревателя появилась в обозревателе Microsoft Internet Explorer 4,0, чтобы предоставить область просмотра, смежную с областью браузера. Это, по сути, дочернее окно в окне Internet Explorer, и его можно использовать для вывода информации и взаимодействия с пользователем практически таким же образом. Панели обозревателя чаще всего отображаются в виде вертикальной панели в левой части области браузера. Однако панель обозревателя также может отображаться горизонтально, под областью браузера.

![Снимок экрана, на котором показаны вертикальная и горизонтальная панели обозревателя.](images/expl1.jpg)

Панель обозревателя имеет широкий спектр возможных применений. Пользователи могут выбрать вариант, который должен отображаться несколькими разными способами, включая его выбор из подменю " **панель обозревателя** " в меню " **вид** " или нажатием кнопки на панели инструментов. Internet Explorer предоставляет несколько стандартных панелей обозревателя, включая Избранное и поиск.

Одним из способов настройки обозревателя Internet Explorer является добавление настраиваемой панели обозревателя. При реализации и регистрации они будут добавлены в подменю " **панель обозревателя** " меню " **вид** ". При выборе пользователем область просмотра панели обозревателя может использоваться для вывода информации и ввода данных пользователем во многом так же, как у обычного окна.

![снимок экрана панели обозревателя](images/expl2.jpg)

Чтобы создать настраиваемую панель обозревателя, необходимо реализовать и зарегистрировать *объект диапазона*. Объекты управления версиями появились в оболочке версии 4,71 и предоставляют возможности, аналогичные обычным окнам. Однако, поскольку они являются объектами модели COM и содержатся в Internet Explorer или оболочке, они реализуются несколько по-разному. Для создания примеров полос обозревателя, отображаемых на первом рисунке, использовались простые объекты полос. Реализация образца вертикальной панели обозревателя будет подробно рассмотрена в следующем разделе.

## <a name="tool-bands"></a>Полосы инструментов

Панель *инструментов — это* объект с полосой, который появился в Microsoft Internet Explorer 5 для поддержки функции Windows Radio Tool. Панель инструментов Internet Explorer на самом деле является [элементом управления главной](../controls/rebar-controls.md) панели, который содержит несколько [элементов управления ToolBar](../controls/toolbar-control-reference.md). Создавая панель инструментов, можно добавить полосу к этому элементу управления главной панели. Однако, как и в случае с панелями обозревателя, панель инструментов является окном общего назначения.

![снимок экрана с полосами инструментов](images/toolband1.jpg)

Пользователи выводят панель инструментов, выбирая ее из подменю **панели инструментов** меню **вид** или из контекстного меню, которое отображается щелчком правой кнопкой мыши в области панели инструментов.

## <a name="desk-bands"></a>Полосы рабочего стола

Для создания *полос рабочих столов* также можно использовать объекты полос. Хотя их Базовая реализация похожа на панели обозревателя, полосы рабочего стола не связаны с Internet Explorer. Настольный полоса — это, по сути, способ создания закрепляемого окна на рабочем столе. Пользователь выбирает его, щелкнув правой кнопкой мыши панель задач и выбрав ее в подменю **панели инструментов** .

![Снимок экрана, на котором показан пример полосы рабочего стола.](images/desk2.png)

Изначально полосы рабочего стола закреплены на панели задач.

![Снимок экрана, на котором показаны полосы рабочего стола, закрепленные на панели задач.](images/desk1.jpg)

Затем пользователь может перетащить полосу настольных ПК на Рабочий стол, и она появится в виде обычного окна.

![снимок экрана с полосами рабочих столов](images/desk3.png)

## <a name="implementing-band-objects"></a>Реализация диапазонных объектов

Обсуждаются следующие темы.

-   [Основы использования объекта Band](#band-object-basics)
-   [Регистрация аппаратного контроллера управления](#band-registration)
-   [Простой пример настраиваемой панели обозревателя](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Основы использования объекта Band

Несмотря на то, что их можно использовать во многом в обычных окнах, объекты управления полосами являются COM-объектами, которые существуют в контейнере. Панели обозревателя содержатся в Internet Explorer, а полосы рабочего стола — в оболочке. Хотя они выполняют различные функции, их Базовая реализация очень похожа. Основное различие заключается в способе регистрации объекта Band, который, в свою очередь, управляет типом объекта и его контейнером. В этом разделе обсуждаются аспекты реализации, общие для всех объектов полос. Дополнительные сведения о реализации см. [в простом примере настраиваемой панели обозревателя](#a-simple-example-of-a-custom-explorer-bar) .

Помимо [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), все объекты полос должны реализовывать следующие интерфейсы.

-   [**идескбанд**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

Кроме регистрации идентификатора класса (CLSID), для соответствующей категории компонентов также должны быть зарегистрированы панель обозревателя и объекты полосы рабочего стола. Регистрация категории компонента определяет тип объекта и его контейнер. Полосы инструментов используют другую процедуру регистрации и не имеют идентификатора категории (CATID). CATID для трех объектов с диапазоном, которые им необходимы:



| Тип полосы               | Категории компонентов |
|-------------------------|--------------------|
| Вертикальная панель обозревателя   | CATID \_ инфобанд    |
| Горизонтальная панель обозревателя | CATID \_ коммбанд    |
| Настольный полос               | CATID \_ дескбанд    |



 

Дополнительные сведения о регистрации объектов с полосами см. в статье [Регистрация аппаратного контроллера управления](#band-registration) .

Если объект диапазона должен принимать вводимые пользователем данные, он также должна реализовывать [**иинпутобжект**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject). Чтобы добавить элементы в контекстное меню для панели обозревателя или полос рабочего стола, объект диапазона должен экспортировать [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). Панели инструментов не поддерживают контекстные меню.

Поскольку объекты управления доступом реализуют дочернее окно, они также должны реализовать процедуру окна для обработки сообщений Windows.

Объекты полос могут отсылать команды в контейнер через интерфейс [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) контейнера. Чтобы получить указатель интерфейса, вызовите метод [**иинпутобжектсите:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) контейнера и запросите IID \_ IOleCommandTarget. Затем вы отправляете команды в контейнер с помощью [**IOleCommandTarget:: Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec). Группа команд — КГИД \_ дескбанд. При вызове метода [**идескбанд:: жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) объекта Band контейнер использует параметр *двбандид* , чтобы назначить объект диапазона идентификатор, который используется для трех команд. Поддерживаются четыре идентификатора команды **IOleCommandTarget:: Exec** .

-   DBID \_ бандинфочанжед

    Сведения о полосе изменились. Задайте для параметра *пваин* идентификатор диапазона, полученный в последнем вызове [**Идескбанд:: жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Контейнер будет вызывать метод **идескбанд:: жетбандинфо** объекта Band для запроса обновленной информации.

-   DBID \_ максимизебанд

    Разверните полосу. Задайте для параметра *пваин* идентификатор диапазона, полученный в последнем вызове [**Идескбанд:: жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).

-   DBID \_ шовонли

    Включите или отключите другие полосы в контейнере. Задайте для параметра *пваин* \_ Тип VT Unknown с одним из следующих значений:

    

    | Значение | Описание                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | pUnk  | Указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) объекта полосы. Все остальные полосы рабочего стола будут скрыты. |
    | 0     | Скрыть все полосы настольных рабочих столов.                                                                                        |
    | 1     | Отображение всех полос настольных рабочих столов.                                                                                        |

    

     

-   DBID \_ пушчеврон

    [Версия 5](versions.md). Отображение шевронного меню. Контейнер отправляет сообщение [**\_ пушчеврон RB**](../controls/rb-pushchevron.md) , а объект Band получает уведомление [ \_ чевронпушед РБН](../controls/rbn-chevronpushed.md) , которое выводит запрос на отображение углового меню. Задайте для параметра *нкмдексекопт* метода [**IOleCommandTarget:: Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) идентификатор диапазона, полученный в последнем вызове [**идескбанд:: жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Установите параметр *пваин* метода **IOleCommandTarget:: Exec** в \_ Тип VT I4 с определенным приложением значением. Он передается обратно объекту Band в качестве значения *лаппвалуе* \_ уведомления чевронпушед РБН.

### <a name="band-registration"></a>Регистрация аппаратного контроллера управления

Объект диапазона должен быть зарегистрирован как внутрипроцессный сервер OLE, поддерживающий потоковое подразделение. Значением по умолчанию для сервера является текстовая строка меню. Для панелей обозревателя он будет отображаться в подменю **панели обозревателя** в меню **вид** Internet Explorer. Для панелей инструментов она появится в подменю **панели** элементов меню **вид** Internet Explorer. Для полос рабочего стола она появится в подменю **панели инструментов** контекстного меню панели задач. Как и в случае с ресурсами меню, размещение амперсанда (&) перед буквой приведет к его подчеркиванием и включению сочетаний клавиш. Например, строка меню вертикальной панели обозревателя, показанной на первом рисунке, — «пример &вертикальной панели обозревателя».

Изначально Internet Explorer получает перечисление зарегистрированных объектов панели обозревателя из реестра с помощью категорий компонентов. Чтобы повысить производительность, он кэширует это перечисление, представляя впоследствии добавленные панели обозревателя. Чтобы заставить Windows Internet Explorer перестроить кэш и распознавать новую панель обозревателя, при регистрации новой панели обозревателя удалите следующие разделы реестра:

**HKey \_ Текущее \_ пользовательское** \\ **программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Explorer невозможная \\  \\  \\ Категория компонентов **настройок** \\  \\ **{00021493-0000-0000-C000-000000000046}** \\ **enum**

**HKey \_ Текущее \_ пользовательское** \\ **программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Explorer невозможная \\  \\  \\ Категория компонентов **настройок** \\  \\ **{00021494-0000-0000-C000-000000000046}** \\ **enum**

> [!Note]  
> Так как для каждого пользователя создается кэш панели обозревателя, приложению установки может потребоваться перечислить все кусты реестра пользователя или добавить заглушку для каждого пользователя, которая будет запускаться при первом входе пользователя в систему.

 

Как правило, основная запись реестра для объекта диапазона будет выглядеть следующим образом.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

Для панелей инструментов также должен быть зарегистрирован CLSID своего объекта в Internet Explorer. Для этого присвойте значение в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **панель инструментов** с идентификатором CLSID объекта панели инструментов, как показано ниже. Его значение данных игнорируется, поэтому тип значения не важен.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

В реестр также можно добавить несколько необязательных значений. Например, следующее значение необходимо, если вы хотите использовать панель обозревателя для отображения HTML. отображаемое значение не является примером, а действительное значение, которое следует использовать.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

Если вы хотите использовать панель обозревателя для отображения HTML, в сочетании с указанным выше значением также необходимо следующее необязательное значение. Это значение должно быть установлено в расположение файла, содержащего HTML-содержимое для панели обозревателя.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

Еще одно необязательное значение определяет ширину или высоту панели обозревателя по умолчанию в зависимости от того, является ли она вертикальной или горизонтальной, соответственно.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

Для значения Барсизе должно быть задано значение Width или Height линейки. Для этого значения требуется восемь байт и оно помещается в реестр как двоичное значение. Первые четыре байта задают размер в пикселях в шестнадцатеричном формате, начиная с крайнего левого байта. Последние четыре байта зарезервированы и должны быть равны нулю.

Например, здесь показаны полные записи реестра для панели обозревателя с поддержкой HTML с шириной по умолчанию 291 (0x123) пикселей.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

Регистрацию идентификатора CATID объекта диапазона можно выполнять программным способом. Создайте объект диспетчера категорий компонентов (CLSID \_ стдкомпоненткатегориесмгр) и запросите указатель на его интерфейс [**икатрегистер**](/windows/win32/api/comcat/nn-comcat-icatregister) . Передайте идентификаторы CLSID и CATID объекта полоси в [**икатрегистер:: регистерклассимплкатегориес**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Простой пример настраиваемой панели обозревателя

В этом примере рассматривается реализация образца вертикальной панели обозревателя, показанного в введении.

Ниже приведена базовая процедура создания пользовательской панели обозревателя.

1.  [Реализуйте функции, необходимые для библиотеки DLL](#dll-functions).
2.  [Реализуйте необходимые COM-интерфейсы.](#required-interface-implementations)
3.  [Реализуйте все требуемые необязательные COM-интерфейсы.](#optional-interface-implementations)
4.  [Зарегистрируйте CLSID объекта и, если необходимо, категорию компонента.](#clsid-registration)
5.  Создайте дочернее окно Internet Explorer, чтобы оно соответствовало области отображаемой панели обозревателя.
6.  [Используйте дочернее окно для вывода сведений и взаимодействия с пользователем.](#the-window-procedure)

Очень простая реализация, используемая в образце панели обозревателя, может фактически использоваться для любого типа панели обозревателя или полосы рабочего стола, просто зарегистрировав ее для соответствующей категории компонента. Более сложные реализации необходимо настроить для области вывода и контейнера каждого типа объекта. Однако большую часть этой настройки можно добиться, приняв пример кода и расширив его, применив привычные методики программирования Windows к дочернему окну. Например, можно добавить элементы управления для взаимодействия с пользователем или графики для более насыщенного экрана.

### <a name="dll-functions"></a>Функции DLL

Все три объекта упаковываются в одну библиотеку DLL, которая предоставляет следующие функции.

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**Регистрация**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

Первые три функции — это стандартные реализации, которые не будут обсуждаться здесь. Реализация фабрики класса также является стандартной.

### <a name="required-interface-implementations"></a>Требуемые реализации интерфейса

В вертикальном образце панели обозревателя реализованы четыре необходимых интерфейса: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)и [**идескбанд**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) в составе класса цексплорербар. Реализации конструктора, деструктора и **IUnknown** являются простыми и не обсуждаются здесь. Подробности см. в примере кода.

Подробно рассматриваются следующие интерфейсы.

-   [IObjectWithSite](#iobjectwithsite)
-   [IPersistStream](#ipersiststream)
-   [идескбанд](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

Когда пользователь выбирает панель обозревателя, контейнер вызывает метод [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) соответствующего объекта полосы. Для параметра *пунксите* будет задан указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) сайта.

Как правило, реализация [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) должна выполнять следующие действия:

1.  Освобождение любого указателя на сайт, который в данный момент удерживается.
2.  Если указатель, переданный в [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) , имеет значение **null**, полоса удаляется. **SetSite** может вернуть S \_ ОК.
3.  Если указатель, переданный в [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) , имеет **значение**, отличное от NULL, устанавливается новый сайт. **SetSite** должен выполнить следующие действия:
    1.  Вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на сайте для своего интерфейса [**иолевиндов**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .
    2.  Вызовите [**иолевиндов:: Onwindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) , чтобы получить маркер родительского окна. Сохраните маркер для последующего использования. Выпустите [**иолевиндов**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) , если он больше не нужен.
    3.  Создайте окно объекта полоси в качестве дочернего элемента окна, полученного на предыдущем шаге. Не создавайте его как видимое окно.
    4.  Если объект Band реализует [**иинпутобжект**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на сайте для своего интерфейса [**иинпутобжектсите**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) . Сохранить указатель на этот интерфейс для последующего использования.
    5.  Если все шаги выполнены успешно, возвращается значение S \_ ОК. В противном случае возвращается код ошибки, определенный OLE, указывающий на сбой.

Образец панели обозревателя реализует [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) следующим образом. В следующем коде *m \_ псите* является закрытой переменной-членом, содержащей указатель [**иинпутобжектсите**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) , а *m \_ хвндпарент* содержит маркер родительского окна. В этом примере также обрабатывается создание окна. Если окно не существует, этот метод создает окно панели обозревателя как дочерний элемент соответствующего размера родительского окна, полученного с помощью **SetSite**. Дескриптор дочернего окна хранится в *\_ дескрипторе m*.


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



[**Реализация SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) в примере просто заключает вызов метода [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) сайта, используя указатель сайта, сохраненный с помощью [](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a>IPersistStream

Internet Explorer будет вызывать интерфейс [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) панели обозревателя, чтобы позволить панели обозревателя загружать или сохранять постоянные данные. Если постоянные данные отсутствуют, методы должны по-прежнему возвращать код успешного выполнения. Интерфейс **IPersistStream** наследует от [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), поэтому необходимо реализовать пять методов.

-   [**IPersist::, ClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream:: IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream:: Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream:: Жетсиземакс**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

Образец панели обозревателя не использует постоянные данные и имеет только минимальную реализацию [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). [**IPersist::**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) GETOBJECT Возвращает CLSID объекта (CLSID \_ сампликсплорербар), а остаток возвращает либо s \_ ОК, либо \_ false, либо E \_ нотимпл.

### <a name="ideskband"></a>идескбанд

Интерфейс [**идескбанд**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) относится к объектам диапазона. В дополнение к одному методу он наследует от [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), который, в свою очередь, наследует от [**иолевиндов**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).

Существует два метода [**иолевиндов**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) [**: и**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) [**иолевиндов:: контекстсенситивехелп**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp). Реализация метода **Window** в образце панели обозревателя возвращает его дескриптор дочернего окна, m и *\_ HWND*. Контекстно-зависимая справка не реализована, поэтому **контекстсенситивехелп** возвращает **E \_ нотимпл**.

Интерфейс [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) имеет три метода.

-   [**Идоккингвиндов:: Шовдв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**Идоккингвиндов:: Клоседв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**Идоккингвиндов:: Ресизебордердв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

Метод [**ресизебордердв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) не используется с каким-либо типом объекта Band и всегда должен возвращать E \_ нотимпл. Метод [**шовдв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) либо показывает, либо скрывает окно панели обозревателя в зависимости от значения его параметра.


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



Метод [**клоседв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) уничтожает окно панели обозревателя.


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



Оставшийся метод, [**жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), относится к **идескбанд**. Internet Explorer использует его для указания идентификатора и режима просмотра панели обозревателя. Internet Explorer также может запросить один или несколько фрагментов информации из панели обозревателя, заполнив элемент **двмаск** структуры [**дескбандинфо**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) , которая передается в качестве третьего параметра. **Жетбандинфо** должен хранить идентификатор и режим просмотра и заполнить структуру **дескбандинфо** запрошенными данными. Образец панели обозревателя реализует **жетбандинфо** , как показано в следующем примере кода.


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a>Необязательные реализации интерфейса

Существует два необязательных интерфейса, но это может быть полезно для реализации: [**иинпутобжект**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) и [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). Образец панели обозревателя реализует **иинпутобжект**. Сведения о том, как реализовать **IContextMenu**, см. в документации.

### <a name="iinputobject"></a>иинпутобжект

Интерфейс [**иинпутобжект**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) должен быть реализован, если объект диапазона принимает вводимые пользователем данные. Internet Explorer реализует [**иинпутобжектсите**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) и использует **иинпутобжект** для поддержания соответствующего фокуса ввода пользователя, если он содержит несколько окон, содержащихся в них. Панель обозревателя должна реализовывать три метода.

-   [**Иинпутобжект:: Уиактиватеио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**Иинпутобжект:: Хасфокусио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**Иинпутобжект:: Транслатеакцелераторио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer вызывает [**уиактиватеио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) , чтобы сообщить панели обозревателя о том, что она активируется или деактивируется. При активации образец панели обозревателя вызывает [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) , чтобы установить фокус на окно.

Internet Explorer вызывает [**хасфокусио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) , когда пытается определить, какое окно находится в фокусе. Если окно панели обозревателя или один из его потомков имеет фокус, **хасфокусио** должен вернуть значение s \_ ОК. В противном случае оно должно возвращать \_ значение S false.

[**Транслатеакцелераторио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) позволяет объекту обрабатывать сочетания клавиш. Образец панели обозревателя не реализует этот метод, поэтому он возвращает \_ значение false.

Реализация [**иинпутобжектсите**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) в строке примера выглядит следующим образом.


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a>Регистрация CLSID

Как и для всех COM-объектов, необходимо зарегистрировать CLSID на панели обозревателя. Чтобы объект правильно функционировал в Internet Explorer, он также должен быть зарегистрирован для соответствующей категории компонентов (CATID \_ инфобанд). Соответствующий раздел кода для панели обозревателя показан в следующем примере кода.


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



При регистрации объектов Band в образце используются обычные процедуры COM.

Помимо идентификатора CLSID, серверный объект также должен быть зарегистрирован для одной или нескольких категорий компонентов. В действительности это основное различие в реализации между вертикальными и горизонтальными образцами панели обозревателя. Этот процесс обрабатывается путем создания объекта диспетчера категорий компонентов (CLSID \_ стдкомпоненткатегориесмгр) и использования метода [**икатрегистер:: регистерклассимплкатегориес**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) для регистрации сервера объектного диапазона. В этом примере регистрация категории компонента обрабатывается путем передачи CLSID и CATID образца панели обозревателя в закрытую функцию —**регистеркомкат**, как показано в следующем примере кода.


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a>Процедура окна

Поскольку объект диапазона использует дочернее окно для своего экрана, он должен реализовать процедуру окна для обработки сообщений Windows. Образец "полоса" имеет минимальную функциональность, поэтому процедура окна обрабатывает только пять сообщений:

-   [**WM \_ нккреате**](../winmsg/wm-nccreate.md)
-   [**WM \_ Paint**](../gdi/wm-paint.md)
-   [**\_команда WM**](../menurc/wm-command.md)
-   [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)
-   [**WM \_ киллфокус**](../inputdev/wm-killfocus.md)

Процедуру можно легко расширить для размещения дополнительных сообщений, чтобы обеспечить поддержку дополнительных функций.


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



\_Обработчик команд WM просто возвращает ноль. \_Обработчик рисования WM создает простой текст, отображаемый в примере на панели обозревателя во введении.


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



\_Обработчики WM SETFOCUS и WM \_ киллфокус уведомляют сайт об изменении фокуса, вызывая метод [**Иинпутобжектсите:: онфокусчанжеис**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) сайта.


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



Объекты управления доступом обеспечивают гибкий и мощный способ расширения возможностей Internet Explorer путем создания настраиваемых панелей обозревателя. Реализация рабочего диапазона позволяет расширить возможности обычных окон. Хотя требуется какое-то программирование COM, оно в конечном итоге предоставляет дочернее окно для пользовательского интерфейса. В этом случае основная часть реализации может использовать привычные методы программирования Windows. Хотя в приведенном здесь примере используются только ограниченные функциональные возможности, он иллюстрирует все необходимые функции объекта диапазона, и его можно легко расширить для создания уникального и мощного пользовательского интерфейса.

 

 
