---
title: Вкладки свойств и страницы свойств
description: Вкладки свойств и страницы свойств
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7991ea650838e9980292257c14d26909e9476f0f35422fa21deab2b0b5ecbbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104941"
---
# <a name="property-sheets-and-property-pages"></a>Вкладки свойств и страницы свойств

Свойства объекта предоставляются клиентам аналогично методам через COM-интерфейсы или реализацией **IDispatch** объекта, что позволяет изменять свойства в программах, вызывающих эти методы. технология OLE страниц свойств предоставляет средства для создания пользовательского интерфейса для свойств объекта в соответствии с Windows стандартами пользовательского интерфейса. Поэтому свойства предоставляются конечным пользователям. Страница свойств объекта — это диалоговое окно с вкладками, где каждая вкладка соответствует определенной странице свойств. Модель OLE для работы со страницами свойств состоит из следующих функций:

-   Каждая страница свойств управляется внутрипроцессный объект, реализующий либо [**ипропертипаже**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) , либо [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2). Каждая страница идентифицируется своим уникальным идентификатором CLSID.
-   Объект задает поддержку страниц свойств путем реализации [**испеЦифипропертипажес**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Через этот интерфейс вызывающий объект может получить список идентификаторов CLSID, определяющих определенные страницы свойств, которые поддерживает объект. Если объект указывает CLSID страницы свойств, объект должен иметь возможность получать изменения свойств со страницы свойств.
-   Любой фрагмент кода (клиента или объекта), который хочет отобразить страницу свойств объекта, передает указатель [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) объекта (или массив, если необходимо затронуть несколько объектов) вместе с массивом CLSID страницы для [**олекреатепропертифраме**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) или [**олекреатепропертифрамеиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), который создает диалоговое окно с вкладками.
-   Диалоговое окно кадра свойств создает экземпляр каждой страницы свойств, используя [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для каждого идентификатора CLSID. Кадр свойства получает по меньшей мере указатель [**ипропертипаже**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) для каждой страницы. Кроме того, фрейм создает для каждой страницы объект сайта страницы свойств. Каждый сайт реализует [**ипропертипажесите**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , и этот указатель передается на каждую страницу. Затем страница взаимодействует с сайтом через этот указатель интерфейса.
-   На каждой странице также учитывается объект или объекты, для которых она была вызвана. то есть кадр свойств передает указатели [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)объектов на каждую страницу. Когда инструкция применяет изменения к объектам, каждая страница запрашивает соответствующий указатель интерфейса и передает новые значения свойств объектам любым необходимым способом. Нет никаких указаний о том, как такое взаимодействие должно произойти.
-   Объект также может поддерживать просмотр свойств через интерфейс [**иперпропертибровсинг**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) , позволяя объекту указать, какое свойство должно получать начальное фокус при отображении страницы свойств, а также указать строки и значения, которые могут отображаться клиентом в собственном интерфейсе пользователя.

Эти функции показаны на следующей схеме:

![Схема, на которой показаны вкладки свойств и функции страниц свойств.](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

Эти интерфейсы определяются следующим образом:

``` syntax
interface ISpecifyPropertyPages : IUnknown 
  { 
    HRESULT GetPages([out] CAUUID *pPages); 
  }; 
 
 
interface IPropertyPage : IUnknown 
  { 
    HRESULT SetPageSite([in] IPropertyPageSite *pPageSite); 
    HRESULT Activate([in] HWND hWndParent, [in] LPCRECT prc 
        , [in] BOOL bModal); 
    HRESULT Deactivate(void); 
    HRESULT GetPageInfo([out] PROPPAGEINFO *pPageInfo); 
    HRESULT SetObjects([in] ULONG cObjects 
        , [in, max_is(cObjects)] IUnknown **ppunk); 
    HRESULT Show([in] UINT nCmdShow); 
    HRESULT Move([in] LPCRECT prc); 
    HRESULT IsPageDirty(void); 
    HRESULT Apply(void); 
    HRESULT Help([in] LPCOLESTR pszHelpDir); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
interface IPropertyPageSite : IUnknown 
  { 
    HRESULT OnStatusChange([in] DWORD dwFlags); 
    HRESULT GetLocaleID([out] LCID *pLocaleID); 
    HRESULT GetPageContainer([out] IUnknown **ppUnk); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
```

Метод [**испеЦифипропертипажес::**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) GetObject возвращает числовой массив значений UUID (GUID), каждый из которых описывает идентификатор CLSID страницы свойств, которую должен отобразить объект. Кто угодно вызывает вкладку свойств с помощью [**олекреатепропертифраме**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) или [**олекреатепропертифрамеиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) , передает этот массив в функцию. Обратите внимание, что если вызывающий объект хочет отображать страницы свойств для нескольких объектов, он должен передать этим функциям только пересечение списков CLSID всех объектов. Иными словами, вызывающий объект должен вызывать только те страницы свойств, которые являются общими для всех объектов.

Кроме того, вызывающий объект передает указатели [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) на затронутые объекты в функции API. Обе функции API создают диалоговое окно "кадр свойств" и создают экземпляр сайта страницы с [**ипропертипажесите**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) для каждой загружаемой страницы. Через этот интерфейс страница свойств может:

-   Получение текущего языка, используемого в таблице свойств, через [**жетлокалеид**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid).
-   Попросите кадр обработать нажатия клавиш через [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator).
-   Уведомлять кадр изменений на странице через [**онстатусчанже**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).
-   Получите указатель интерфейса для самого кадра через [**жетпажеконтаинер**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer), несмотря на то, что для этой функции в данный момент не определены интерфейсы, всегда возвращает E \_ нотимпл.

Рамка свойства создает экземпляр каждого объекта страницы свойств и получает интерфейс [**ипропертипаже**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) каждой страницы. Через этот интерфейс кадр информирует страницу узла страницы ([**сетпажесите**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)), получает размеры и строки страницы ([**жетпажеинфо**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)), передает указатели интерфейса затронутым объектам ([**сетобжектс**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)), сообщает странице о необходимости создания и уничтожения элементов управления ([**Активация**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) и [**деактивация**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)). указывает, что страница должна отображать или изменять положение ("[**Показывать**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) " и " [**переместить**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)"), предписывает странице применить текущие значения к затронутым объектам ([**Применить**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)), проверять состояние "грязной" страницы ([**испажедирти**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)), вызывать справку ([**справку**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)) и передавать нажатия клавиш на страницу ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).

Объект также поддерживает просмотр по каждому свойству, который предоставляет следующие возможности.

1.  Способ (с помощью [**иперпропертибровсинг**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) и [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)), указывающий, какое свойство на странице свойств должно получать первоначальный фокус при первом отображении страницы свойств
2.  Способ (через [**иперпропертибровсинг**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) для объекта, чтобы указать предопределенные значения и соответствующие описательные строки, которые могут отображаться в пользовательском интерфейсе клиента для свойств.

Объект может выбрать поддержку (2) без поддержки (1), например, если у объекта нет страницы свойств.

Интерфейсы [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) и [**иперпропертибровсинг**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) определяются следующим образом:

``` syntax
interface IPerPropertyBrowsing : IUnknown 
  { 
    HRESULT GetDisplayString([in] DISPID dispID, [out] BSTR *pbstr); 
    HRESULT MapPropertyToPage([in] DISPID dispID, [out] CLSID *pclsid); 
    HRESULT GetPredefinedStrings([in] DISPID dispID, [out] CALPOLESTR *pcaStringsOut, [out] CADWORD *pcaCookiesOut); 
    HRESULT GetPredefinedValue([in] DISPID dispID, [in] DWORD dwCookie, [out] VARIANT *pvarOut); 
  } 
 
interface IPropertyPage2 : IPropertyPage 
  { 
    HRESULT EditProperty([in] DISPID dispID); 
  } 
 
```

Чтобы задать поддержку таких возможностей, объект реализует [**иперпропертибровсинг**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing). С помощью этого интерфейса вызывающий объект может запросить сведения, необходимые для получения обзора, например стандартные строки ([**жетпредефинедстрингс**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) и значения ([**жетпредефинедвалуе**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)), а также отображаемую строку для заданного свойства ([**жетдисплайстринг**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).

Кроме того, клиент может получить идентификатор CLSID страницы свойств, позволяющий пользователю редактировать заданное свойство, идентифицированное с помощью DISPID ([**маппропертитопаже**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)). Затем клиент указывает кадру свойства активировать эту страницу изначально, передав идентификаторы CLSID и DISPID в [**олекреатепропертифрамеиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect). Кадр активирует эту страницу первой и передает идентификатор DISPID на страницу через [**IPropertyPage2:: едитпроперти**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty). Затем страница устанавливает фокус на поле редактирования этого свойства. Таким образом, клиент может перейти от имени свойства в собственном пользовательском интерфейсе к странице свойств, которая может манипулировать этим свойством.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Страницы свойств и вкладки свойств](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




