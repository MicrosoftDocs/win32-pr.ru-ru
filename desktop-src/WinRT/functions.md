---
description: Справочник по функциям среда выполнения Windows C++.
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: Функции (среда выполнения Windows)
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: 1ed2ea39385ac5cb7afc34770a5ee2d2a572bb8b
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105699302"
---
# <a name="functions-windows-runtime-c-reference"></a>Функции (Справочник по среда выполнения Windows C++)

## <a name="in-this-section"></a>Содержание раздела



| Функция | Описание |
|-|-|
| [**кодекодепрокси**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | Находит реализацию интерфейса модели COM в серверном процессе, используя интерфейс для прокси-объекта. |
| [**креатеконтролинпут**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | Создает объект [**икореинпутсаурцебасе**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) в ПОТОКЕ пользовательского интерфейса вызывающего объекта. |
| [**креатеконтролинпутекс**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | Создает объект [**икореинпутсаурцебасе**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) в рабочем потоке или в ПОТОКЕ пользовательского интерфейса.  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | Создает экземпляр IDirect3DDevice из Идксгидевице. |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | Создает экземпляр IDirect3DSurface из Идксгисурфаце. |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | Создает экземпляр [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) из [идксгидевице](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice). |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | Создает экземпляр [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) из [идксгисурфаце](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface). |
| [**креатерандомакцессстреамонфиле**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | Создает среда выполнения Windows поток произвольного доступа к файлу. |
| [**креатерандомакцессстреамоверстреам**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | Создает среда выполнения Windows поток произвольного доступа вокруг базовой реализации [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . |
| [**креатестреамоверрандомакцессстреам**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | Создает объект [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) вокруг объекта среда выполнения Windows [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) . |
| [**креатексамлуипресентер**](createxamluipresenter.md) | Статическая функция Creator, которая может создать [**ксамлуипресентер**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) для поверхности рендеринга в классическом приложении. |
| [**дбграисеассертионфаилуре**](/previous-versions//jj635749(v=vs.85)) | Вызывает Assert для отладки.  |
| [**Жетдксгиинтерфаце (IDirect3DDevice ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | Извлекает интерфейс DXGI из экземпляра [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) . |
| [**Жетдксгиинтерфаце (IDirect3DSurface ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | Извлекает интерфейс DXGI из экземпляра [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) . |
| [**жетдксгиинтерфацефромобжект**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | Извлекает интерфейс DXGI из объекта. |
| [**жетрестриктедерроринфо**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | Возвращает объект ограниченных сведений об ошибках, заданный предыдущим вызовом [**сетрестриктедерроринфо**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) в текущем логическом потоке. |
| [**HSTRING \_ усерфри**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | Освобождает ресурсы на стороне сервера при вызове файлов заглушки RPC. |
| [**HSTRING \_ UserFree64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | Освобождает ресурсы на стороне сервера при вызове файлов заглушки RPC.  |
| [**HSTRING \_ усермаршал**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | Маршалирует объект [**HString**](hstring.md) в буфер RPC. |
| [**HSTRING \_ UserMarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | Маршалирует объект [**HString**](hstring.md) в буфер RPC. |
| [**HSTRING \_ усерсизе**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | Вычисляет размер сети объекта [**HString**](hstring.md) и получает его обработчик и данные. |
| [**HSTRING \_ UserSize64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | Вычисляет размер сети объекта [**HString**](hstring.md) и получает его обработчик и данные. |
| [**HSTRING \_ усерунмаршал**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | Выполняет распаковку объекта [**HString**](hstring.md) из буфера RPC. |
| [**HSTRING \_ UserUnmarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | Выполняет распаковку объекта [**HString**](hstring.md) из буфера RPC. |
| [**исеррорпропагатионенаблед**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | Указывает, возникает ли событие [**CoreApplication. UnhandledErrorDetected**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) для ошибок, возвращаемых делегатом, зарегистрированным в качестве функции обратного вызова для Среда выполнения Windows события API или завершения асинхронного метода. |
| [**дллжетактиватионфактори**](/previous-versions//br205771(v=vs.85)) | Извлекает фабрику активации из библиотеки DLL, содержащей классы активируемого среда выполнения Windows. |
| [**метадатажетдиспенсер**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | Создает класс распределителя. |
| [**пдфкреатерендерер**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | Возвращает экземпляр интерфейса [**ипдфрендерернативе**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) для отображения одной страницы файла в формате переносимого документа (PDF). |
| [**пдфрендерпарамс**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | Заполняет структуру [**\_ \_ параметров отрисовки PDF**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) . \_Структура параметров рендеринга PDF \_ представляет набор свойств для вывода одной страницы PDF-файла. |
| [**RoActivateInstance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | Активирует указанный класс среда выполнения Windows. |
| [**рокаптуриррорконтекст**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | Сохраняет текущий контекст ошибки, чтобы он был доступен для последующих вызовов функции [**рофаилфаствисеррорконтекст**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) . |
| [**роклеареррор**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | Удаляет существующие сведения об ошибках из текущего блока среды потока (ТЕБ). |
| [**рофаилфаствисеррорконтекст**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | Вызывает исключение, которое не является непрерывным в текущем процессе. |
| [**RoFailFastWithErrorContextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | Вызывает исключение, которое не является непрерывным в текущем процессе, а также позволяет включить дополнительный контекст ошибки, еще не записанный операционной системой. |
| [**рофрипараметеризедтипикстра**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | Освобождает маркер, выделенный [**рожетпараметеризедтипеинстанцеиид**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid). |
| [**рожетактиватаблеклассрегистратион**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | Включает получение сведений о регистрации класса. |
| [**рожетактиватионфактори**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | Возвращает фабрику активации для указанного класса среды выполнения. |
| [**рожетагилереференце**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | Создает динамическую ссылку для объекта, указанного данным интерфейсом. |
| [**рожетапартментидентифиер**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | Возвращает уникальный идентификатор для текущего подразделения. |
| [**рожетбуффермаршалер**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | Предоставляет стандартный модуль IBuffer для реализации семантики, связанной с интерфейсом IBuffer при его маршалировании. |
| [**рожетерроррепортингфлагс**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | Возвращает текущее поведение отчетов среда выполнения Windows функций ошибок. |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | Находит и извлекает файл метаданных, описывающий двоичный интерфейс приложения (ABI) для указанного имени типа. |
| [**рожетпараметеризедтипеинстанцеиид**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | Выполняет вычисление идентификатора интерфейса или типа делегата, полученного в результате создания параметризованного интерфейса или делегата с указанными аргументами типа. |
| [**рожетсерверактиватаблеклассес**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | Извлекает классы активируемого, которые зарегистрированы для данного исполняемого сервера (EXE), зарегистрированного по ИДЕНТИФИКАТОРу пакета вызывающего процесса. |
| [**роинитиализе**](/windows/win32/api/roapi/nf-roapi-roinitialize) | Инициализирует среда выполнения Windows в текущем потоке с заданной моделью параллелизма. |
| [**роинспектсреадерроринфо**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | Возвращает объект Error, представляющий стек вызовов в точке, где была создана ошибка. |
| [**роинспекткаптуредстаккбакктраце**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | Предоставляет отладчикам способ проверки стека вызовов из целевого процесса. |
| [**руригинатиррор**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | Сообщает об ошибке и информативной строке к подключенному отладчику. |
| [**руригинатиррорв**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | Сообщает об ошибке и информативной строке к подключенному отладчику. |
| [**руригинателангуажеексцептион**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | Сообщает о ошибке, информативной строке и объекте ошибки в присоединенном отладчике. |
| [**ропараметеризедтипикстражеттипесигнатуре**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | Возвращает сигнатуру типа, используемую для вычислить идентификатор IID из последнего вызова [**рожетпараметеризедтипеинстанцеиид**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) с указанным маркером. |
| [**ропарсетипенаме**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | Анализирует имя типа и существующие параметры типа в случае параметризованных типов. |
| [**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | Регистрирует фабрики необработанных активаций массива для сервера среда выполнения Windows exe. |
| [**рорегистерфорапартментшутдовн**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | Регистрирует обратный вызов [**иапартментшутдовн**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) для вызова при завершении текущего апартамента. |
| [**рорепортунхандледеррор**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | Запускает глобальный обработчик ошибок при возникновении необработанного исключения. |
| [**рорепортфаиледделегате**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | Активирует глобальный обработчик ошибок, когда происходит сбой делегата. |
| [**роресолвенамеспаце**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | Определите прямые дочерние элементы, типы и подчиненные пространства имен указанного среда выполнения Windows пространства имен на любом языке программирования, поддерживаемом среда выполнения Windows. |
| [**роресолверестриктедерроринфореференце**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | Возвращает указатель интерфейса [**ирестриктедерроринфо**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) на основе заданной ссылки. |
| [**роревокеактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | Удаляет из среда выполнения Windows массив зарегистрированных фабрик активации. |
| [**росетерроррепортингфлагс**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | Задает поведение отчетов для среда выполнения Windows функций ошибок. |
| [**ротрансформеррор**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | Сообщает о измененной ошибке и информативной строке к подключенному отладчику. |
| [**ротрансформеррорв**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | Сообщает преобразованной ошибке и информативную строку с подключенным отладчиком. |
| [**раунинитиализе**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | Закрывает среда выполнения Windows в текущем потоке. |
| [**раунрегистерфорапартментшутдовн**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | Отменяет регистрацию ранее зарегистрированного интерфейса [**иапартментшутдовн**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) . |
| [**сетрестриктедерроринфо**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | Задает ограниченный объект сведений об ошибках для текущего потока. |
| [**виндовскомпарестрингординал**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | Сравнивает два указанных объекта [**HString**](hstring.md) и возвращает целое число, которое указывает их относительное расположение в порядке сортировки. |
| [**виндовсконкатстринг**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | Сцепляет две указанные строки. |
| [**виндовскреатестринг**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | Создает новый [**HString**](hstring.md) на основе указанной исходной строки. |
| [**виндовскреатестрингреференце**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | Создает новую ссылку на строку на основе указанной строки. |
| [**виндовсделетестринг**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | Уменьшает значение счетчика ссылок буфера строк. |
| [**виндовсделетестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | Отменяет предварительно выделенный буфер строк, если он не был повышен до [**HString**](hstring.md). |
| [**виндовсдупликатестринг**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | Создает копию указанной строки. |
| [**виндовсжетстринглен**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | Возвращает длину указанной строки в символах Юникода. |
| [**виндовсжетстрингравбуффер**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | Возвращает резервный буфер для указанной строки. |
| [**виндовсинспектстринг**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | Предоставляет отладчикам возможность отображать значение среда выполнения Windows [**HString**](hstring.md) в другом адресном пространстве, удаленно или из дампа.  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | Предоставляет отладчикам возможность отображать значение среда выполнения Windows [**HString**](hstring.md) в другом адресном пространстве, удаленно или из дампа.  |
| [**виндовсисстринжемпти**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | Указывает, является ли указанная строка пустой строкой. |
| [**виндовспреаллокатестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | Выделяет изменяемый символьный буфер для использования при создании [**HString**](hstring.md) . |
| [**виндовспромотестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | Создает объект [**HString**](hstring.md) из указанного [**\_ буфера HString**](hstring-buffer.md). |
| [**виндовсреплацестринг**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | Заменяет все вхождения набора символов в указанной строке другим набором символов для создания новой строки. |
| [**виндовсстрингхасембеддеднулл**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | Указывает, содержит ли указанная строка внедренные символы NULL. |
| [**виндовссубстринг**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | Извлекает подстроку из указанной строки. Подстрока начинается с указанной позиции символа. |
| [**виндовссубстрингвисспеЦифиедленгс**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | Извлекает подстроку из указанной строки. Подстрока начинается с указанной позиции знака и имеет указанную длину. |
| [**виндовстримстринженд**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | Удаляет все завершающие вхождения указанного набора символов из исходной строки. |
| [**виндовстримстрингстарт**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | Удаляет все ведущие вхождения указанного набора символов из исходной строки. |



 

 

 
