---
title: Элементы управления ActiveX
description: Элементы управления ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413781"
---
# <a name="activex-controls"></a>Элементы управления ActiveX

Элементы управления ActiveX — это основы, состоящие из COM, доступных для подключения объектов, составных документов, страниц свойств, OLE-автоматизации, сохраняемости объектов и предоставляемых системой объектов шрифтов и изображений. Как показано ниже, каждая из этих основных технологий играет роль в элементах управления.

<dl> <dt>

<span id="COM"></span><span id="com"></span>-
</dt> <dd>

Элемент управления, по сути, является COM-объектом, предоставляющим интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , через который клиенты могут получать указатели на другие интерфейсы. Элементы управления могут поддерживать лицензирование через [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) и самостоятельную регистрацию. Дополнительные сведения об COM, лицензировании и самостоятельной регистрации см. [в разделе Объектная модель компонентов](the-component-object-model.md) .

</dd> <dt>

<span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Подключаемые объекты
</dt> <dd>

Элементы управления могут поддерживать исходящие интерфейсы через подключаемые объекты, чтобы элемент управления мог взаимодействовать со своим клиентом. Например, исходящий интерфейс может активировать действие в клиенте, может уведомлять Клиента о некоторых изменениях в элементе управления или запрашивать разрешение у клиента до того, как элемент управления потребует какого бы то ни было действия. Дополнительные сведения о том, как работают подключаемые объекты, см. [в разделе события в com и Connected Objects](events-in-com-and-connectable-objects.md) .

</dd> <dt>

<span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Единая для обмена данными
</dt> <dd>

Элементы управления могут быть перенесены и удалены в контейнере с помощью справки из их контейнера. Дополнительные сведения о перетаскивании см. в разделе [**иолеинплацеобжектвиндовлесс:: жетдроптаржет**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) .

</dd> <dt>

<span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Составные документы
</dt> <dd>

Элемент управления может быть встроенным активным объектом, который может быть внедрен в содержащий его клиент. Конечный пользователь активирует элемент управления для инициации действия в контейнерном приложении. Дополнительные сведения об активации на месте и других интерфейсах составных документов см. в разделе [составные документы](compound-documents.md) .

</dd> <dt>

<span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Страницы свойств
</dt> <dd>

Элементы управления могут предоставлять страницы свойств, чтобы конечные пользователи могли просматривать и изменять свойства элемента управления. Дополнительные сведения о работе страниц свойств см. в разделе [страницы свойств и вкладки свойств](property-pages-and-property-sheets.md) .

</dd> <dt>

<span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE Automation
</dt> <dd>

Элементы управления могут предоставлять возможности программирования с помощью OLE-автоматизации, чтобы клиенты могли воспользоваться преимуществами функций элемента управления через язык программирования, предоставляемый клиентом. Дополнительные сведения о OLE Automation см. в разделе OLE Automation.

</dd> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Постоянное хранилище
</dt> <dd>

Элемент управления может реализовывать один или несколько интерфейсов сохраняемости для поддержки сохранения состояния. Разработчик элемента управления должен решить, какие типы сохраняемости наиболее важны, и реализовать соответствующие интерфейсы сохраняемости. Клиент решает, какой интерфейс предпочтительнее использовать. Дополнительные сведения о всех интерфейсах сохраняемости см. [в разделе Объектная модель компонентов](the-component-object-model.md) .

</dd> <dt>

<span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Объекты Font и Picture
</dt> <dd>

Элементы управления могут использовать эти предоставляемые системой объекты для предоставления визуального представления в пределах клиента. Объект Font реализует несколько интерфейсов, включая [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) и [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp). Объект Font можно создать с помощью [**олекреатефонтиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect). Объект Picture также реализует несколько интерфейсов, включая [**ипиктуре**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) и [**ипиктуредисп**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp). Объект Picture можно создать с помощью [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) и загрузить из потока с помощью [**олелоадпиктуре**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).

</dd> </dl>

Важно понимать, что эти функции можно использовать в любом объекте OLE. Для использования этих функций не требуется реализовывать элемент управления. Кроме того, единственным необходимым интерфейсом для элемента управления является IUnknown. Элемент управления дополнительно поддерживает другие интерфейсы в зависимости от необходимости поддержки связанных функций.

Помимо этих функций, следующие интерфейсы и функции относятся к технологиям элементов управления: [**метод интерфейса IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)и [**олетранслатеколор**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor). Кроме того, конкретные элементы управления представляют собой набор стандартов для свойств и методов, которые могут поддерживаться элементом управления или контейнером элемента управления.

> [!Note]  
> Системная библиотека OleAut32.dll содержит реализации функций ([**олекреатепропертифраме**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**олекреатепропертифрамеиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**олекреатефонтиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)и [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)). Кроме того, OleAut32.dll содержит реализации стандартных объектов Font и Picture, а также библиотеку типов для всех интерфейсов, используемых с элементами управления, а также дополнительные структуры данных и типы данных.

 

Дополнительные сведения см. в следующих разделах:

-   [Архитектура элементов управления ActiveX](activex-controls-architecture.md)
-   [Интерфейсы элементов управления ActiveX](activex-controls-interfaces.md)
-   [Свойства и методы](properties-and-methods.md)
-   [События элементов управления](control-events.md)
-   [Визуальное представление](visual-representation.md)
-   [Обработка клавиатуры для элементов управления](keyboard-handling-for-controls.md)
-   [Сохраняемость](persistence.md)
-   [Регистрация и лицензирование](registration-and-licensing.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Рекомендации по контейнерам элементов управления и элементов управления ActiveX](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 