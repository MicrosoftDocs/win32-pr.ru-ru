---
description: Ссылка на оболочку — это объект данных, который содержит сведения, используемые для доступа к другому объекту в пространстве имен оболочки&\# 8212, то есть любой объект, видимый в проводнике Windows.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Ссылки оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265089"
---
# <a name="shell-links"></a>Ссылки оболочки

*Ссылка на оболочку* — это объект данных, который содержит сведения, используемые для доступа к другому объекту в пространстве имен оболочки, т. е. любой объект, видимый в проводнике Windows. К типам объектов, к которым можно получить доступ через ссылки оболочки, относятся файлы, папки, диски и принтеры. Ссылка на оболочку позволяет пользователю или приложению получить доступ к объекту из любого места в пространстве имен. Пользователю или приложению не нужно знать текущее имя и расположение объекта.

-   [О связях оболочки](#about-shell-links)
    -   [Разрешение ссылок](#link-resolution)
    -   [Файлы ссылок](#link-files)
    -   [Идентификаторы элементов и списки идентификаторов](#item-identifiers-and-identifier-lists)
-   [Использование ссылок оболочки](#using-shell-links)
    -   [Создание ярлыка и ярлыка папки для файла](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [Разрешение ярлыка](#resolving-a-shortcut)
    -   [Создание ярлыка для нефайлового объекта](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>О связях оболочки

Пользователь создает ссылку на оболочку, выбрав команду **создать ярлык** в контекстном меню объекта. Система автоматически создает значок для связи с оболочкой, комбинируя значок объекта с маленькой стрелкой (называемой системным значком перекрытия ссылок), который отображается в левом нижнем углу значка. Ссылка на оболочку, имеющую значок, называется ярлыком; Однако термины «ссылка» и «ярлык оболочки» часто используются взаимозаменяемыми. Как правило, пользователь создает ярлыки для быстрого доступа к объектам, хранящимся во вложенных папках или в общих папках на других компьютерах. Например, пользователь может создать ярлык для документа Microsoft Word, который находится во вложенной папке, и поместить значок ярлыка на Рабочий стол. Затем пользователь может открыть документ, дважды щелкнув значок ярлыка. Если документ перемещается или переименовывается после создания ярлыка, система попытается обновить ярлык при следующем выборе пользователем.

Приложения также могут создавать и использовать ссылки и ярлыки оболочки. Например, приложение для обработки текста может создать ссылку оболочки для реализации списка недавно использовавшихся документов. Приложение создает ссылку оболочки с помощью интерфейса [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) для создания объекта связи оболочки. Приложение использует интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) или [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) для хранения объекта в файле или потоке.

> [!Note]  
> Нельзя использовать [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) для создания ссылки на URL-адрес.

 

В этом обзоре описывается интерфейс [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) и объясняется, как с его помощью создавать и разрешать ссылки оболочки из приложения на основе Microsoft Win32. Так как структура ссылок оболочки основана на модели COM, необходимо ознакомиться с основными понятиями программирования COM и OLE перед чтением этого обзора.

### <a name="link-resolution"></a>Разрешение ссылок

Если пользователь создает ярлык для объекта, а имя или расположение объекта позднее изменилось, система автоматически выполняет шаги по обновлению или разрешению, если при следующем выборе пользователя он будет выполнен в следующий раз. Однако если приложение создает ссылку оболочки и сохраняет ее в потоке, система не пытается автоматически разрешить эту ссылку. Приложение должно разрешить ссылку, вызвав метод [**ишелллинк:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) .

При создании ссылки на оболочку система сохраняет сведения о ссылке. При разрешении ссылки — либо автоматически, либо с помощью вызова [**ишелллинк:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) — система сначала извлекает путь, связанный со ссылкой оболочки, используя указатель на список идентификаторов для ссылки оболочки. Дополнительные сведения о списке идентификаторов см. в разделе [идентификаторы элементов и списки идентификаторов](#item-identifiers-and-identifier-lists). Система выполняет поиск связанного объекта в этом пути и, если находит объект, разрешает ссылку. Если система не может найти объект, то она вызывается в [службе DLT,](../fileio/distributed-link-tracking-and-object-identifiers.md) если она доступна, чтобы найти объект. Если служба DLT недоступна или не может найти объект, система ищет в одном каталоге объект с тем же временем создания файла и атрибутами, но с другим именем. Этот тип поиска разрешает ссылку на объект, который был переименован.

Если система по-прежнему не может найти объект, она выполняет поиск по каталогам, рабочему столу и локальным томам, выполняя рекурсивный просмотр дерева каталогов для объекта с тем же именем или временем создания. Если система по-прежнему не находит совпадения, отображается диалоговое окно с запросом на ввод расположения. Приложение может подавлять диалоговое окно, указывая значение **однообъективных зеркальных \_ без \_ пользовательского интерфейса** в вызове [**ишелллинк:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).

### <a name="initialization-of-the-component-object-library"></a>Инициализация библиотеки объектов компонентов

Прежде чем приложение сможет создавать и разрешать ярлыки, оно должно инициализировать библиотеку объектов компонентов, вызвав функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) . Для каждого вызова **CoInitialize** требуется соответствующий вызов функции [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , которую приложение должно вызывать при завершении. Вызов **CoUninitialize** гарантирует, что приложение не завершит работу до получения всех его ожидающих сообщений.

### <a name="location-independent-names"></a>Имена Location-Independent

Система предоставляет независимые от расположения имена для ссылок оболочки на объекты, хранящиеся в общих папках. Если объект хранится локально, система предоставляет локальный путь и имя файла для объекта. Если объект хранится удаленно, система предоставляет имя сетевого ресурса в формате UNC для объекта. Так как система предоставляет имена, независимые от расположения, ссылка на оболочку может служить универсальным именем для файла, который можно передать на другие компьютеры.

### <a name="link-files"></a>Файлы ссылок

Когда пользователь создает ярлык для объекта, выбрав команду **создать ярлык** в контекстном меню объекта, Windows хранит сведения, необходимые для доступа к объекту в файле ссылки — двоичный файл с расширением LNK. Файл ссылки содержит следующие сведения:

-   Расположение (путь) объекта, на который ссылается ярлык (этот объект называется соответствующим объектом).
-   Рабочий каталог соответствующего объекта.
-   Список аргументов, передаваемых системой соответствующему объекту при активации метода [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) для ярлыка.
-   Команда отображения, используемая для задания начального состояния отображения соответствующего объекта. Это одно из значений SW, \_ описанных в разделе [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).
-   Расположение (путь и индекс) значка ярлыка.
-   Строка описания ярлыка.
-   Сочетание клавиш для ярлыка.

При удалении файла ссылки соответствующий объект не изменяется.

При создании ярлыка для другого ярлыка система просто копирует файл ссылки, а не создает новый файл ссылки. В этом случае сочетания клавиш не будут зависеть друг от друга.

Приложение может зарегистрировать расширение имени файла в качестве типа файла ярлыка. Если файл имеет расширение, зарегистрированное в качестве типа файла ярлыка, система автоматически добавляет к значку файла значок перекрытия ссылок, определенный системой (маленькая стрелка). Чтобы зарегистрировать расширение имени файла в качестве типа ярлыка, необходимо добавить значение в реестре для расширения имени файла, как показано в примере ниже. Обратите внимание, что оболочку необходимо перезапустить, чтобы значок оверлея вступил в силу. У "a" нет значения данных.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>Имена ярлыков

Имя ярлыка, представляющее собой строку, которая отображается под значком оболочки, фактически является именем файла самого ярлыка. Пользователь может изменить строку описания, выбрав ее и введя новую строку.

### <a name="location-of-shortcuts-in-the-namespace"></a>Расположение ярлыков в пространстве имен

Ярлык может находиться на рабочем столе или в любом месте пространства имен оболочки. Аналогичным образом объект, связанный с ярлыком, также может существовать в любом месте пространства имен оболочки. Приложение может использовать метод [**ишелллинк:: сетпас**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) , чтобы задать путь и имя файла для связанного объекта, а также метод [**ишелллинк::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) GetObject для получения текущего пути и имени файла для объекта.

### <a name="shortcut-working-directory"></a>Ярлык рабочего каталога

Рабочий каталог — это каталог, в котором соответствующий объект ярлыка загружает или хранит файлы, когда пользователь не определяет конкретный каталог. Файл ссылки содержит имя рабочего каталога для соответствующего объекта. Приложение может задать имя рабочего каталога для соответствующего объекта с помощью метода [**ишелллинк:: сетворкингдиректори**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) и может получить имя текущего рабочего каталога для соответствующего объекта с помощью метода [**Ишелллинк:: жетворкингдиректори**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) .

### <a name="shortcut-command-line-arguments"></a>Аргументы командной строки ярлыка

Файл ссылки содержит аргументы командной строки, которые оболочка передает в соответствующий объект, когда пользователь выбирает ссылку. Приложение может задать аргументы командной строки для ярлыка с помощью метода [**ишелллинк:: сетаргументс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) . Можно задать аргументы командной строки, если соответствующее приложение, такое как компоновщик или компилятор, принимает специальные флаги в качестве аргументов. Приложение может извлекать аргументы командной строки из ярлыка с помощью метода [**ишелллинк::-Arguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) .

### <a name="shortcut-show-commands"></a>Команды быстрого показа

Когда пользователь дважды щелкает ярлык, система запускает приложение, связанное с соответствующим объектом, и устанавливает начальное отображение состояния приложения на основе команды показ, заданной с помощью ярлыка. Команда отображения может иметь любое из значений SW, \_ входящих в описание функции [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) . Приложение может задать команду отображения для ярлыка с помощью метода [**ишелллинк:: сетшовкмд**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) , а также получить команду Current-шоу с помощью метода [**Ишелллинк:: жетшовкмд**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) .

### <a name="shortcut-icons"></a>Значки ярлыков

Как и другие объекты оболочки, ярлык имеет значок. Пользователь обращается к объекту, связанному с ярлыком, дважды щелкнув значок ярлыка. Когда система создает значок для ярлыка, он использует точечный рисунок соответствующего объекта и добавляет в нижний левый угол значок перекрытия ссылок, определенный системой (маленькая стрелка). Приложение может задать расположение (путь и индекс) значка ярлыка с помощью метода [**ишелллинк:: сетиконлокатион**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) . Приложение может извлечь это расположение с помощью метода [**ишелллинк:: жетиконлокатион**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) .

### <a name="shortcut-descriptions"></a>Описания ярлыков

Сочетания клавиш имеют описания, но пользователь не видит их. Приложение может использовать описание для хранения любой текстовой информации. Описания задаются с помощью метода [**ишелллинк:: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) и извлекаются с помощью метода [**ишелллинк:: «Description**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) ».

### <a name="shortcut-keyboard-shortcuts"></a>Сочетания клавиш

С объектом ярлыка может быть связано сочетание клавиш. Сочетания клавиш позволяют пользователю нажать сочетание клавиш, чтобы активировать ярлык. Приложение может задать сочетание клавиш для ярлыка с помощью метода [**ишелллинк:: сесоткэй**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) и может получить текущее сочетание клавиш с помощью метода [**ишелллинк::-горячих**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) .

### <a name="item-identifiers-and-identifier-lists"></a>Идентификаторы элементов и списки идентификаторов

Оболочка использует идентификаторы объектов в пространстве имен оболочки. Все объекты, видимые в оболочке (файлы, каталоги, серверы, рабочие группы и т. д.), имеют уникальные идентификаторы между объектами в их родительской папке. Эти идентификаторы называются идентификаторами элементов и имеют тип данных [**шитемид**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , как определено в файле заголовка штипес. h. Идентификатор элемента — это байтовый поток переменной длины, который содержит сведения, определяющие объект в папке. Только создатель идентификатора элемента знает содержимое и формат идентификатора. Единственная часть идентификатора элемента, используемая оболочкой, — первые два байта, которые указывают размер идентификатора.

Каждая родительская папка имеет собственный идентификатор элемента, который идентифицирует его в собственной родительской папке. Таким образом, любой объект оболочки может быть однозначно идентифицирован списком идентификаторов элементов. В родительской папке хранится список идентификаторов элементов, которые он содержит. Список имеет тип данных [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Списки идентификаторов элементов выделяются оболочкой и могут передаваться через интерфейсы оболочки, такие как [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder). Важно помнить, что каждый идентификатор в списке идентификаторов элементов имеет смысл только в контексте родительской папки.

Приложение может задать список идентификаторов элементов ярлыка с помощью метода [**ишелллинк:: сетидлист**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) . Этот метод полезен при задании ярлыка для объекта, который не является файлом, например принтером или диском. Приложение может получить список идентификаторов элементов ярлыка с помощью метода [**ишелллинк:: жетидлист**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) .

## <a name="using-shell-links"></a>Использование ссылок оболочки

В этом разделе содержатся примеры, демонстрирующие создание и разрешение ярлыков в приложениях на основе Win32. В этом разделе предполагается, что вы знакомы с программированием Win32, C++ и OLE COM.

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>Создание ярлыка и ярлыка папки для файла

Пример функции Креателинк в следующем примере создает ярлык. Параметры включают указатель на имя файла, с которым выполняется ссылка, указатель на имя создаваемого ярлыка и указатель на описание ссылки. Описание состоит из строки "ярлык **имени файла**", где **имя** файла — это имя файла, с которым необходимо создать ссылку.

Чтобы создать ярлык папки с помощью образца функции Креателинк, вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с помощью CLSID \_ фолдершорткут вместо CLSID \_ шелллинк (CLSID \_ фолдершорткут поддерживает ишелллинк). Весь остальной код остается прежним.

Поскольку Креателинк вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , предполагается, что функция [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) уже была вызвана. Креателинк использует интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) для сохранения ярлыка и интерфейса [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) для хранения имени и описания файла.


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a>Разрешение ярлыка

Приложению может потребоваться доступ к созданному ранее ярлыку и управление им. Эта операция называется разрешением ярлыка.

Определяемая приложением функция Ресолвеит в следующем примере разрешает ярлык. Его параметры включают в себя маркер окна, указатель на путь ярлыка и адрес буфера, который получает новый путь к объекту. Обработчик окна определяет родительское окно для всех окон сообщений, которые может потребоваться отобразить оболочке. Например, оболочка может отображать окно сообщения, если ссылка находится на необщем носителе, в случае возникновения проблем в сети, если пользователю нужно вставить дискету и т. д.

Функция Ресолвеит вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и предполагает, что функция [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) уже была вызвана. Обратите внимание, что Ресолвеит должен использовать интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) для хранения сведений о ссылках. **IPersistFile** реализуется объектом [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) . Сведения о связи должны быть загружены до получения сведений о пути, которые показаны Далее в примере. Сбой загрузки сведений о ссылках приводит к сбою вызовов функций членов [**ишелллинк::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) Ишелллинк и [**:: undescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) .


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a>Создание ярлыка для нефайлового объекта

Создание ярлыка для нефайлового объекта, например принтера, похоже на создание ярлыка для файла, за исключением того, что вместо указания пути к файлу необходимо задать для списка идентификаторов принтер. Чтобы задать список идентификаторов, вызовите метод [**ишелллинк:: сетидлист**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) , указав адрес списка идентификаторов.

Каждый объект в пространстве имен оболочки имеет идентификатор элемента. Оболочка часто объединяет идентификаторы элементов в списки, заканчивающиеся нулем, состоящие из любого числа идентификаторов элементов. Дополнительные сведения об идентификаторах элементов см. в разделе [идентификаторы элементов и списки идентификаторов](#item-identifiers-and-identifier-lists).

В общем случае, если необходимо задать ярлык для элемента, у которого нет имени файла, например принтера, у вас уже есть указатель на интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) объекта. **Ишеллфолдер** используется для создания расширений пространства имен.

После получения идентификатора класса для [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)можно вызвать функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы получить адрес интерфейса. Затем можно вызвать интерфейс для перечисления объектов в папке и получить адрес идентификатора элемента для искомого объекта. Наконец, можно использовать адрес в вызове функции-члена [**ишелллинк:: сетидлист**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) , чтобы создать ярлык для объекта.

 

 
