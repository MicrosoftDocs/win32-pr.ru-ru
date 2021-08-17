---
description: интерфейсы (среда выполнения Windows C++)
ms.assetid: CB05B5F8-BE15-4BE0-A651-F6E8912D649D
title: интерфейсы (среда выполнения Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 468944bcd2437309d953fe53e64e36366ca0cd7ac6ad4d8c32aa9c8d71f91ca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741648"
---
# <a name="interfaces"></a>Интерфейсы

## <a name="in-this-section"></a>Содержание раздела

| Интерфейс | Описание |
|-|-|
| [**иактиватаблеклассрегистратион**](/windows/win32/api/activationregistration/nn-activationregistration-iactivatableclassregistration) | Включает получение сведений о регистрации для класса. |
| [**IActivationFactory**](/windows/win32/api/activation/nn-activation-iactivationfactory) | Разрешает активацию одного или нескольких классов средой выполнения Windows. |
| [**иагилереференце**](/windows/desktop/api/objidl/nn-objidl-iagilereference) | Включает получение гибкой ссылки на объект. |
| [**иапартментшутдовн**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) | Включает регистрацию обработчика уведомлений о завершении работы апартамента. |
| [**асинкактионкомплетедхандлер**](asyncactioncompletedhandler.md) | Представляет метод, который вызывается при завершении асинхронного действия. |
| [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) | Представляет асинхронное действие. |
| [**иасинкактионпрогресшандлер<TProgress>**](/previous-versions//br205782(v=vs.85)) | Представляет метод, который вызывается, когда асинхронное действие сообщает о ходе выполнения. |
| [**IAsyncActionWithProgress<TProgress>**](/previous-versions//br205784(v=vs.85)) | Представляет асинхронное действие, сообщающее о ходе выполнения. |
| [**иасинкактионвиспрогресскомплетедхандлер<TProgress>**](/previous-versions//br205785(v=vs.85)) | Представляет метод, который вызывается, когда завершается асинхронное действие, которое сообщает о завершении выполнения. |
| [**иасинЦинфо**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo) | Обеспечивает поддержку асинхронных операций. |
| [**IAsyncOperation<TResult>**](/previous-versions//br205802(v=vs.85)) | Представляет асинхронную операцию, которая возвращает результат. |
| [**иасинкоператионкомплетедхандлер<TResult>**](/previous-versions//br205803(v=vs.85)) | Представляет метод, который вызывается после завершения асинхронной операции. |
| [**иасинкоператионпрогресшандлер**](/previous-versions//br205805(v=vs.85)) | Представляет метод, который вызывается, когда асинхронная операция сообщает о ходе выполнения. |
| [**IAsyncOperationWithProgress**](/previous-versions//br205807(v=vs.85)) | Возвращает асинхронную операцию, которая возвращает результат и отчитывается о ходе выполнения. |
| [**Иасинкоператионвиспрогресскомплетедхандлер<TResult, TProgress>**](/previous-versions//br205808(v=vs.85)) | Представляет метод, который вызывается, когда завершается асинхронная операция, сообщающая о завершении выполнения. |
| [**иаудиофраменативе**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative) | Представляет кадр звуковых данных. |
| [**иаудиофраменативефактори**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenativefactory) | Создает экземпляры [**иаудиофраменативе**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative). |
| [**IBuffer**](/previous-versions//hh438362(v=vs.85)) | Представляет массив байтов. |
| [**ибуффербитеакцесс**](/previous-versions//hh846267(v=vs.85)) | Представляет буфер в виде массива байтов. |
| [**IClosable**](/windows/win32/api/windows.foundation/nn-windows-foundation-iclosable) | Определяет метод освобождения распределенных ресурсов. |
| [**икомпоситиондравингсурфацеинтероп**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop) | Собственный интерфейс взаимодействия, позволяющий рисовать на объекте Surface с помощью RECT для определения области, в которой производится рисование. |
| [**ICompositionDrawingSurfaceInterop2**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2) | Собственный интерфейс взаимодействия, позволяющий считывать содержимое области рисования композиции (или поверхность виртуального рисования композиции). |
| [**икомпоситионграфиксдевицеинтероп**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiongraphicsdeviceinterop) | Собственный интерфейс взаимодействия, позволяющий получить и настроить графическое устройство. |
| [**иконтактманажеринтероп**](/previous-versions//dn302109(v=vs.85)) | Обеспечивает доступ к методам [**ContactManager**](/uwp/api/Windows.ApplicationModel.Contacts.ContactManager?view=winrt-19041) в приложении, которое управляет несколькими окнами. |
| [**икореаппликатион**](/previous-versions//hh438365(v=vs.85)) | Позволяет приложениям обрабатывать изменения состояния, управлять окнами и интегрировать различные платформы пользовательского интерфейса. |
| [**икореаппликатионексит**](/previous-versions//hh438366(v=vs.85)) | предоставляет средства для завершения работы приложений Windows Store. |
| [**икореаппликатионинитиализатион**](/previous-versions//hh438370(v=vs.85)) | Содержит метод Run, используемый для запуска объекта приложения из точки входа приложения. |
| [**икореаппликатионвиев**](/previous-versions//hh438372(v=vs.85)) | Представляет представление приложения. |
| [**икореиммерсивеаппликатион**](/previous-versions//hh438382(v=vs.85)) | Содержит методы для управления представлениями в приложении. |
| [**икореинпутинтероп**](/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop) | включает источник входных данных для объекта [**кореинпут**](https://www.bing.com/search?q=**CoreInput**) приложения хранилища Windows. |
| [**икоревиндовинтероп**](/windows/desktop/api/corewindow/nn-corewindow-icorewindowinterop) | Позволяет приложениям получать окно, хандлеоф окно ([**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041)), связанное с этим интерфейсом. |
| [**идллсерверактиватаблеклассрегистратион**](/windows/win32/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration) | Включает получение сведений о регистрации для внутрипроцессного сервера. |
| [**иерроррепортингсеттингс**](/previous-versions//br205818(v=vs.85)) | обеспечивает интеграцию отладчика для приложений среда выполнения Windows. |
| [**иевенсандлер<T>**](/previous-versions//hh438385(v=vs.85)) | Представляет метод, обрабатывающий событие, имеющее данные о событии типа **T**. |
| [**иексесерверактиватаблеклассрегистратион**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration) | Включает получение сведений о регистрации для сервера вне процесса. |
| [**иексесерверрегистратион**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserverregistration) | Представляет зарегистрированный сервер вне процесса. |
| [**ифиндреференцетаржетскаллбакк**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ifindreferencetargetscallback) | Определяет интерфейс для обратных вызовов из [**иреференцетраккер:: финдтраккертаржетс**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets). Реализация этого интерфейса должна передавать все найденные экземпляры [**иреференцетраккертаржет**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) методу **фаундтраккертаржет** . |
| [**IInputPaneInterop**](/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop) | Обеспечивает доступ к членам класса [**инпутпане**](/uwp/api/Windows.UI.ViewManagement.InputPane?view=winrt-19041) в классическом приложении. |
| [**IInputStream**](/previous-versions//hh438387(v=vs.85)) | Включает получение асинхронной операции чтения для последовательного потока байтов. |
| [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) | предоставляет функциональные возможности, необходимые для всех классов среда выполнения Windows. |
| [**IIterable<T>**](/previous-versions//br205825(v=vs.85)) | Предоставляет итератор, который поддерживает простой перебор для коллекции указанного типа. |
| [**иитератор<T>**](/previous-versions//br205827(v=vs.85)) | Поддерживает итерацию по коллекции. |
| [**IKeyValuePair<K, V>**](/previous-versions//br205831(v=vs.85)) | Представляет пару "ключ-значение". |
| [**илангуажеексцептионерроринфо**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo) | Включает получение указателя [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , хранящегося в сведениях об ошибке, с помощью вызова руригинателангуажеексцептион. |
| [**ILanguageExceptionErrorInfo2**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2) | Позволяет использовать языковые проекции для предоставления и получения сведений об ошибках, как и в случае с [**илангуажеексцептионерроринфо**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo), с дополнительным преимуществом работы на разных языках. |
| [**илангуажеексцептионтрансформ**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptiontransform) | Позволяет проектам языка предоставлять доступ к системе любому и всему контексту из исключения, которое вызывается из контекста обработчика catch, который перехватывает другое исключение. |
| [**илангуажеексцептионстаккбакктраце**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionstackbacktrace) | Позволяет проекциям предоставлять настраиваемую трассировку стека для этого исключения. |
| [**IMap<K, V>**](/previous-versions//br205834(v=vs.85)) | Представляет ассоциативную коллекцию. |
| [**имапчанжедевентаргс<K>**](/previous-versions//br205835(v=vs.85)) | Предоставляет данные для события [**мапчанжед**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) . |
| [**IMapView<K, V>**](/previous-versions//br205838(v=vs.85)) | Представляет неизменяемое представление в [**IMAP (K, V)**](/previous-versions//br205834(v=vs.85)). |
| [**имеморибуффербитеакцесс**](/previous-versions//mt297505(v=vs.85)) | Предоставляет доступ к [**имеморибуффер**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) в виде массива байтов. |
| [**IMetaDataAssemblyImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport) | Предоставляет методы для доступа и изучения содержимого манифеста сборки. |
| [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) | Предоставляет методы для создания новой области метаданных или открытия существующей. |
| [**IMetaDataDispenserEx**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenserex) | Расширяет интерфейс [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) , чтобы предоставить возможность контролировать работу API метаданных в текущей области метаданных. |
| [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) | Предоставляет методы для импорта существующих метаданных из переносимого исполняемого (PE) файла или другого источника, такого как библиотека типов или отдельный двоичный файл метаданных среды выполнения, а также управления этим метаданными. |
| [**IMetaDataImport2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport2) | Расширяет интерфейс [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) для обеспечения возможности работы с универсальными типами. |
| [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) | Предоставляет методы для хранения и извлечения сведений о метаданных в таблицах. |
| [**IMetaDataTables2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables2) | Расширяет [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) , чтобы включить методы для работы с потоками метаданных. |
| [**IObservableMap<K, V>**](/previous-versions//br205851(v=vs.85)) | Уведомляет обработчики о динамических изменениях на карте, например при добавлении или удалении элементов. |
| [**IObservableVector<T>**](/previous-versions//br205854(v=vs.85)) | Уведомляет обработчики событий об изменениях в векторе. |
| [**иоплоккбреакингхандлер**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-ioplockbreakinghandler) | Этот интерфейс в настоящее время не реализован. |
| [**IOutputStream**](/previous-versions//hh438390(v=vs.85)) | Включает получение асинхронной операции записи для последовательного потока байтов. |
| [**ипдфрендерернативе**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) | Представляет высокопроизводительный API для отображения одной страницы PDF-файла. |
| [**ипаккажедебугсеттингс**](/previous-versions//hh438393(v=vs.85)) | позволяет разработчикам отладчика управлять жизненным циклом приложения для магазина Windows, например при его приостановке или возобновлении. |
| [**IPlayToManagerInterop**](/windows/desktop/api/playtomanagerinterop/nn-playtomanagerinterop-iplaytomanagerinterop) | обеспечивает доступ к методам [**плайтоманажер**](/uwp/api/Windows.Media.PlayTo.PlayToManager?view=winrt-19041) в приложении для магазина Windows, которое управляет несколькими окнами. |
| [**IPrintManagerInterop**](/windows/desktop/api/printmanagerinterop/nn-printmanagerinterop-iprintmanagerinterop) | обеспечивает доступ к методам [**принтманажер**](/uwp/api/Windows.Graphics.Printing.PrintManager?view=winrt-19041) в приложении для магазина Windows, которое управляет несколькими окнами. |
| [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) | представляет значение в хранилище свойств среда выполнения Windows. |
| [**ипропертивалуестатикс**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics) | Создает объекты [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) , которые можно хранить в хранилище свойств. |
| [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) | Включает получение асинхронного модуля чтения байтов или модуля записи байтов, расположенного в указанном месте в потоке байтов произвольного доступа. |
| [**ирандомакцессстреамфилеакцессмоде**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-irandomaccessstreamfileaccessmode) | Предоставляет доступ к режиму доступа к файлу, который использовался при вызове метода [**StorageFile. OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) для открытия потока байтов произвольного доступа. |
| [**IReference<T>**](/previous-versions//br224583(v=vs.85)) | включает расширение системы свойств среда выполнения Windows для определяемых пользователем перечислений, структур и типов делегатов. |
| [**иреференцеаррай<T>**](/previous-versions//br224584(v=vs.85)) | включает расширение системы свойств среда выполнения Windows для массивов определяемых пользователем перечислений, структур и типов делегатов. |
| [**иреференцетраккер**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) | Определяет интерфейс, реализуемый платформой XAML для управления ссылками на объекты XAML. |
| [**иреференцетраккерхост**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost) | Определяет интерфейс, предоставляющий глобальные службы, используемые системой сборки мусора (GC), используемой платформой XAML. |
| [**иреференцетраккерманажер**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager) | Определяет интерфейс для диспетчера ссылок на объект XAML. Реализуйте этот интерфейс для управления экземплярами [**иреференцетраккер**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) на объектах XAML. |
| [**иреференцетраккертаржет**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) | Определяет интерфейс, реализуемый объектом сборщика мусора, на который ссылается XAML. |
| [**ирестриктедерроринфо**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) | Представляет сведения об ошибке, включая ограниченные сведения об ошибках. |
| [**исофтваребитмапнативе**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative) | Представляет точечный рисунок программного обеспечения. |
| [**исофтваребитмапнативефактори**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnativefactory) | Создает экземпляры [**исофтваребитмапнативе**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative). |
| [**исторажефолдерхандлеакцесс**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istoragefolderhandleaccess) | Предоставляет доступ к обработчику операционной системы папки хранилища. |
| [**исторажеитемхандлеакцесс**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istorageitemhandleaccess) | Предоставляет доступ к обработчику операционной системы файла хранилища. |
| [**IStringable**](/windows/win32/api/windows.foundation/nn-windows-foundation-istringable) | Предоставляет способ представления текущего объекта в виде строки. |
| [**исурфацеимажесаурцеманажернативе**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcemanagernative) | Позволяет выполнять групповые операции во всех объектах [**сурфацеимажесаурце**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) , созданных в одном процессе. |
| [**ISurfaceImageSourceNativeWithD2D**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d) | Предоставляет реализацию общей поверхности Microsoft DirectX, которая отображается в [**сурфацеимажесаурце**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) или [**виртуалсурфацеимажесаурце**](/uwp/api/Windows.UI.Xaml.Media.Imaging.VirtualSurfaceImageSource?view=winrt-19041). |
| [**исурфацеимажесаурценативе**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative) | Предоставляет реализацию общей поверхности фиксированного размера для рисования Direct2D. |
| [**исуспендингдеферрал**](isuspendingdeferral.md) | Управляет отложенной операцией приостановки приложения. |
| [**исуспендинжевентаргс**](isuspendingeventargs.md) | Предоставляет данные для события приостановки приложения. |
| [**исуспендингоператион**](isuspendingoperation.md) | Предоставляет сведения о приостановке работы приложения. |
| [**исвапчаинбаккграундпанелнативе**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative) | Обеспечивает взаимодействие между XAML и цепочкой буфера обмена DirectX. |
| [**ISwapChainPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative) | Обеспечивает взаимодействие между XAML и цепочкой буфера обмена DirectX. В отличие от [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041), **SwapChainPanel** может отображаться на любом уровне в дереве отображения XAML, и в любом определенном дереве может присутствовать более 1. |
| [**ISwapChainPanelNative2**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative2) | Обеспечивает взаимодействие между XAML и цепочкой буфера обмена DirectX. В отличие от [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041), **SwapChainPanel** может отображаться на любом уровне в дереве отображения XAML, и в любом определенном дереве может присутствовать более 1. |
| [**Итипедевенсандлер<TSender, Таргс>**](/previous-versions//hh438424(v=vs.85)) | Представляет метод, который будет выполнять обработку события от отправителя типа **TSender** и данных события типа **T**. |
| [**иунбуффередфилехандлеоплокккаллбакк**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleoplockcallback) | Определяет метод обратного вызова, который необходимо выполнить, когда оппортунистическая блокировка для маркера, полученного путем вызова метода [**иунбуффередфилехандлепровидер:: опенунбуффередфилехандле**](/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle) , нарушена. |
| [**иунбуффередфилехандлепровидер**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleprovider) | Предоставляет доступ к дескрипторам из потока байтов произвольного доступа, созданного методом [**StorageFile. OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) . |
| [**IVector<T>**](/previous-versions//br224590(v=vs.85)) | Представляет коллекцию элементов с произвольным доступом. |
| [**ивекторчанжедевентаргс**](ivectorchangedeventargs.md) | Предоставляет данные для события [**векторчанжед**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) . |
| [**IVectorView<T>**](/previous-versions//br224594(v=vs.85)) | Представляет неизменяемое представление в [**IVector (T)**](/uwp/api/windows.foundation.collections.ivector-1?view=winrt-19041). |
| [**ивидеофраменативе**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative) | Представляет кадр видеоданных. |
| [**ивидеофраменативефактори**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenativefactory) | Создает экземпляры [**ивидеофраменативе**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative). |
| [**ивиевпровидер**](/previous-versions//hh438426(v=vs.85)) | Представляет представление в приложении. |
| [**ивиевпровидерфактори**](/previous-versions//hh438427(v=vs.85)) | Создает экземпляр представлений, реализующих интерфейс [**ивиевпровидер**](/previous-versions//hh438426(v=vs.85)) . |
| [**ивиртуалсурфацеимажесаурценативе**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) | Предоставляет реализацию большого (больше размера экрана) общей поверхности для рисования DirectX. |
| [**ивиртуалсурфацеупдатескаллбаккнативе**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative) | Предоставляет интерфейс для реализации поведения рисования, когда [**виртуалсурфацеимажесаурце**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) запрашивает обновление. |
| [**IWeakReference**](/windows/win32/api/weakreference/nn-weakreference-iweakreference) | Представляет слабую ссылку на объект. |
| [**IWeakReferenceSource**](/windows/win32/api/weakreference/nn-weakreference-iweakreferencesource) | Представляет исходный объект, для которого может быть извлечена слабая ссылка. |
| [**Мапчанжедевенсандлер<K, V>**](/previous-versions//br224612(v=vs.85)) | Представляет метод, обрабатывающий событие [**мапчанжед**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) наблюдаемой схемы. |
| [**VectorChangedEventHandler<T>**](/previous-versions//br224626(v=vs.85)) | Представляет метод, обрабатывающий событие [**векторчанжед**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) наблюдаемого вектора. |
