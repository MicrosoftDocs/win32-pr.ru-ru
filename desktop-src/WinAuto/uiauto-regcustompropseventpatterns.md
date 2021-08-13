---
title: Регистрация пользовательских свойств, событий и шаблонов элементов управления
description: Прежде чем можно будет использовать пользовательское свойство, событие или шаблон элемента управления, поставщик и клиент должны зарегистрировать свойство, событие или шаблон элемента управления во время выполнения.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Модель автоматизации пользовательского интерфейса, пользовательские свойства
- Модель автоматизации пользовательского интерфейса, общие сведения о событиях
- Модель автоматизации пользовательского интерфейса, общие сведения о шаблонах элементов управления
- Автоматизация пользовательского интерфейса, регистрация пользовательских свойств
- Автоматизация пользовательского интерфейса, регистрация событий
- Автоматизация пользовательского интерфейса, регистрация шаблонов элементов управления
- Пользовательские свойства, регистрация
- события, регистрация
- шаблоны элементов управления, регистрация
- регистрация, пользовательские свойства
- регистрация, события
- регистрация, шаблоны элементов управления
- шаблоны элементов управления, пользовательские
- шаблоны элементов управления, реализация пользовательского
- Реализация пользовательских шаблонов элементов управления
- пользовательские шаблоны элементов управления
- клиентские оболочки
- обработчики шаблонов
- Реализация обработчиков шаблонов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7205d088f76f235b3078d5a053202f3d39b609389ef6adbc5dbdbca18d9b652b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564063"
---
# <a name="register-custom-properties-events-and-control-patterns"></a>Регистрация пользовательских свойств, событий и шаблонов элементов управления

Прежде чем можно будет использовать пользовательское свойство, событие или шаблон элемента управления, поставщик и клиент должны зарегистрировать свойство, событие или шаблон элемента управления во время выполнения. Регистрация действует глобально в рамках процесса приложения и остается эффективной до тех пор, пока процесс не будет закрыт или последний объект элемента автоматизации пользовательского интерфейса Майкрософт ([**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) или [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) выйдет из процесса.

Для этого необходимо передать идентификатор GUID в автоматизацию пользовательского интерфейса, а также подробные сведения о настраиваемом свойстве, событии или шаблоне элемента управления. Попытка зарегистрировать один и тот же GUID во второй раз с теми же сведениями завершится успешно, но попытка зарегистрировать один и тот же GUID в второй раз, но с разными сведениями (например, пользовательское свойство другого типа) завершится ошибкой. В будущем, если пользовательская спецификация принята и интегрирована в ядро автоматизации пользовательского интерфейса, модель автоматизации пользовательского интерфейса будет проверять пользовательские данные регистрации и использовать уже зарегистрированный код вместо "официальной" реализации платформы, тем самым минимизируя проблемы совместимости приложений. Невозможно удалить уже зарегистрированные свойства, события или шаблоны элементов управления.

Этот раздел состоит из следующих подразделов.

-   [Регистрация пользовательских свойств и событий](#registering-custom-properties-and-events)
-   [Реализация пользовательских шаблонов элементов управления](#implementing-custom-control-patterns)
    -   [Оболочка клиента и обработчик шаблона](#the-client-wrapper-and-the-pattern-handler)
    -   [Реализация оболочки клиента](#implementing-the-client-wrapper)
    -   [Реализация обработчика шаблона](#implementing-the-pattern-handler)
    -   [Регистрация пользовательского шаблона элемента управления](#registering-a-custom-control-pattern)
    -   [Пример реализации пользовательского шаблона элемента управления](#example-implementation-of-a-custom-control-pattern)
-   [Связанные темы](#related-topics)

## <a name="registering-custom-properties-and-events"></a>Регистрация пользовательских свойств и событий

Регистрация пользовательского свойства или события позволяет поставщику и клиенту получить идентификатор для свойства или события, которое затем может быть передано различным методам API, принимающим идентификаторы в качестве параметров.

Чтобы зарегистрировать свойство или событие, сделайте следующее:

1.  Определите идентификатор GUID для пользовательского свойства или события.
2.  Заполните структуру [**уиаутоматионпропертинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) или [**уиаутоматионевентинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) информацией о свойстве или событии, включая идентификатор GUID и нелокализуемое строку, содержащую имя пользовательского свойства или события. Для пользовательских свойств также требуется указать тип данных свойства, например, содержит ли свойство целое число или строку. Тип данных должен быть одним из следующих типов, указанных в перечислении [**уиаутоматионтипе**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . Другие типы данных для пользовательских свойств не поддерживаются.
    -   **\_Bool уиаутоматионтипе**
    -   **Уиаутоматионтипе \_ Double**
    -   **Уиаутоматионтипе, \_ элемент**
    -   **Уиаутоматионтипе \_ int**
    -   **\_Точка уиаутоматионтипе**
    -   **\_Строка уиаутоматионтипе**
3.  Используйте функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра объекта [**куиаутоматионрегистрар**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) и получения указателя на интерфейс [**иуиаутоматионрегистрар**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) объекта.
4.  Вызовите метод [**иуиаутоматионрегистрар:: регистерпроперти**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) или [**регистеревент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) и передайте адрес структуры [**уиаутоматионпропертинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) или структуры [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .

Метод [**иуиаутоматионрегистрар:: регистерпроперти**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) или [**регистеревент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) ВОЗВРАЩАЕТ идентификатор свойства или идентификатор события, который приложение может передать в любой метод автоматизации пользовательского интерфейса, принимающий такой идентификатор в качестве параметра. Например, можно передать зарегистрированный идентификатор свойства в метод [**иуиаутоматионелемент:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) или метод [**Иуиаутоматион:: креатепропертикондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .

В следующем примере показано, как зарегистрировать пользовательское свойство.


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



Идентификаторы свойств и событий, извлекаемых методами [**иуиаутоматионрегистрар:: регистерпроперти**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) и [**регистеревент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) , допустимы только в контексте приложения, которое их извлекает, и только в течение времени существования приложения. Методы регистрации могут возвращать различные целочисленные значения для одного и того же идентификатора GUID при вызове в разных экземплярах среды выполнения одного приложения.

Нет метода, который отменяет регистрацию пользовательского свойства или события. Вместо этого они неявно отменяют регистрацию при освобождении последнего объекта модели автоматизации пользовательского интерфейса.

> [!IMPORTANT]
> Если код является клиентом Microsoft Active Accessibility (MSAA), необходимо вызвать функцию [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) при изменении значения пользовательского свойства.

 

## <a name="implementing-custom-control-patterns"></a>Реализация пользовательских шаблонов элементов управления

Пользовательский шаблон элемента управления не включается в API автоматизации пользовательского интерфейса, но предоставляется третьей стороной во время выполнения. Разработчики приложений клиента и поставщика должны совместно работать с определением пользовательского шаблона элемента управления, включая методы, свойства и события, которые будут поддерживаться шаблоном элемента управления. После определения шаблона элемента управления клиент и поставщик должны реализовать вспомогательные объекты COM, а также код для регистрации шаблона элемента управления во время выполнения. Для пользовательского шаблона элемента управления требуется реализация двух COM-объектов: клиентская оболочка и обработчик шаблона.

> [!Note]  
> В примерах в следующих разделах показано, как реализовать пользовательский шаблон элемента управления, который дублирует функциональные возможности существующего шаблона элемента управления [value](uiauto-implementingvalue.md) . Эти примеры предназначены только для инструкций. Реальный шаблон пользовательского элемента управления должен предоставлять функциональные возможности, недоступные из стандартных шаблонов элементов управления модели автоматизации пользовательского интерфейса.

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a>Оболочка клиента и обработчик шаблона

Обертка клиента реализует API, который используется клиентом для извлечения свойств и вызова методов, предоставляемых пользовательским шаблоном элемента управления. API реализован в виде COM-интерфейса, который передает все запросы свойств и вызовы методов в ядро автоматизации пользовательского интерфейса, которое затем маршалирует запросы и вызовы поставщику.

Код, регистрирующий пользовательский шаблон элемента управления, должен предоставить фабрику класса, которую модель автоматизации пользовательского интерфейса может использовать для создания экземпляров объекта-оболочки клиента. При успешной регистрации пользовательского шаблона элемента управления UI Automation возвращает указатель интерфейса [**иуиаутоматионпаттернинстанце**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , который используется клиентом для переадресации запросов свойств и методов в ядро автоматизации пользовательского интерфейса.

На стороне поставщика ядро автоматизации пользовательского интерфейса принимает запросы свойств и вызовы методов от клиента и передает их объекту обработчика шаблона. Затем обработчик шаблона вызывает соответствующие методы в интерфейсе поставщика для пользовательского шаблона элемента управления.

Код, регистрирующий пользовательский шаблон элемента управления, создает объект обработчика шаблона и при регистрации шаблона элемента управления предоставляет автоматизацию пользовательского интерфейса с указателем на интерфейс [**иуиаутоматионпаттернхандлер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) объекта.

На следующей схеме показано, как запрос клиентского свойства или вызов метода передается из оболочки клиента через базовые компоненты модели автоматизации пользовательского интерфейса в обработчик шаблона, а затем в интерфейс поставщика.

![Схема, показывающая поток от клиентской оболочки до обработчика шаблона и поставщика](images/custompatternsupport.jpg)

Объекты, реализующие оболочку клиента и интерфейсы обработчика шаблонов, должны быть свободными потоками. Кроме того, ядро автоматизации пользовательского интерфейса должно иметь возможность вызывать объекты напрямую без какого бы то ни было промежуточного кода.

### <a name="implementing-the-client-wrapper"></a>Реализация оболочки клиента

Обертка клиента — это объект, предоставляющий интерфейс Икскскспаттерн, используемый клиентом для запроса свойств и вызова методов, поддерживаемых шаблоном пользовательского элемента управления. Интерфейс состоит из пары методов "Getter" для каждого поддерживаемого свойства (Get \_ курренткскскс и Get \_ качедкскскс) и метода "Caller" для каждого поддерживаемого метода. При создании экземпляра объекта конструктор объекта получает указатель на интерфейс [**иуиаутоматионпаттернинстанце**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , который реализуется ядром автоматизации пользовательского интерфейса. Методы интерфейса Икскскспаттерн используют методы [**иуиаутоматионпаттернинстанце::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) и [**каллмесод**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) для пересылки запросов свойств и вызовов методов в ядро автоматизации пользовательского интерфейса.

В следующем примере показано, как реализовать клиентский объект-оболочку для простого шаблона пользовательского элемента управления, поддерживающего одно свойство. Более сложный пример см. в разделе [Пример реализации пользовательского шаблона элемента управления](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a>Реализация обработчика шаблона

Обработчик шаблона — это объект, реализующий интерфейс [**иуиаутоматионпаттернхандлер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) . Этот интерфейс имеет два метода: [**иуиаутоматионпаттернхандлер:: креатеклиентвраппер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) и [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch). Метод **креатеклиентвраппер** вызывается ядром автоматизации пользовательского интерфейса и получает указатель на интерфейс [**иуиаутоматионпаттернинстанце**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) . **Креатеклиентвраппер** отвечает на создание экземпляра объекта-оболочки клиента и передачу указателя интерфейса **иуиаутоматионпаттернинстанце** в конструктор оболочки клиента.

Метод [**диспетчеризации**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) используется ядром автоматизации пользовательского интерфейса для передачи запросов свойств и вызовов методов интерфейсу поставщика для пользовательского шаблона элемента управления. Параметры включают указатель на интерфейс поставщика, отсчитываемый от нуля индекс метода получения или вызываемого свойства, а также массив структур [**уиаутоматионпараметер**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) , содержащих параметры для передачи поставщику. Обработчик шаблона отвечает, проверяя параметр index, чтобы определить, какой метод поставщика следует вызвать, а затем вызывает этот интерфейс поставщика, передавая параметры, содержащиеся в структурах **уиаутоматионпараметер** .

Экземпляр объекта обработчика шаблона создается с помощью того же кода, который регистрирует пользовательский шаблон элемента управления перед регистрацией шаблона элемента управления. Код должен передать указатель интерфейса [**иуиаутоматионпаттернхандлер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) объекта обработчика шаблона в ядро автоматизации пользовательского интерфейса во время регистрации.

В следующем примере показано, как реализовать объект обработчика шаблона для простого пользовательского шаблона элемента управления, поддерживающего одно свойство. Более сложный пример см. в разделе [Пример реализации пользовательского шаблона элемента управления](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a>Регистрация пользовательского шаблона элемента управления

Прежде чем его можно будет использовать, шаблон пользовательского элемента управления должен быть зарегистрирован как поставщиком, так и клиентом. Регистрация предоставляет базовому интерфейсу автоматизации пользовательского интерфейса подробные сведения о шаблоне элемента управления и предоставляет поставщику или клиенту идентификатор шаблона элемента управления, а также идентификаторы для свойств и событий, поддерживаемых шаблоном элемента управления. На стороне поставщика пользовательский шаблон элемента управления должен быть зарегистрирован до того, как связанный элемент управления обрабатывает сообщение [**WM \_ GetObject**](wm-getobject.md) или в то же время.

При регистрации пользовательского шаблона элемента управления поставщик или клиент предоставляет следующие сведения:

-   Идентификатор GUID пользовательского шаблона элемента управления.
-   Нелокализованная строка, содержащая имя пользовательского шаблона элемента управления.
-   Идентификатор GUID интерфейса поставщика, поддерживающего шаблон пользовательского элемента управления.
-   Идентификатор GUID клиентского интерфейса, поддерживающего шаблон пользовательского элемента управления.
-   Массив структур [**уиаутоматионпропертинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) , описывающих свойства, поддерживаемые шаблоном пользовательского элемента управления. Для каждого свойства необходимо указать идентификатор GUID, имя свойства и тип данных.
-   Массив структур [**уиаутоматионмесодинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) , описывающих методы, поддерживаемые шаблоном пользовательского элемента управления. Для каждого метода структура включает следующие сведения: имя метода, количество параметров, список типов данных параметров и список имен параметров.
-   Массив структур [**уиаутоматионевентинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) , описывающих события, создаваемые шаблоном пользовательского элемента управления. Для каждого события необходимо указать идентификатор GUID и имя события.
-   Адрес интерфейса [**иуиаутоматионпаттернхандлер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) объекта обработчика шаблона, который делает пользовательский шаблон элемента управления доступным для клиентов.

Чтобы зарегистрировать пользовательский шаблон элемента управления, поставщик или клиентский код должен выполнить следующие действия.

1.  Заполните структуру [**уиаутоматионпаттернинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) с помощью предыдущих сведений.
2.  Используйте функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра объекта [**куиаутоматионрегистрар**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) и получения указателя на интерфейс [**иуиаутоматионрегистрар**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) объекта.
3.  Вызовите метод [**иуиаутоматионрегистрар:: регистерпаттерн**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , передав адрес структуры [**уиаутоматионпаттернинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .

Метод [**регистерпаттерн**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) возвращает идентификатор шаблона элемента управления, а также список идентификаторов свойств и идентификаторов событий. Приложение может передавать эти идентификаторы любому методу автоматизации пользовательского интерфейса, который принимает такой идентификатор в качестве параметра. Например, можно передать зарегистрированный идентификатор шаблона методу [**иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , чтобы получить указатель на интерфейс поставщика для шаблона элемента управления.

Нет метода, который отменяет регистрацию пользовательского шаблона элемента управления. Вместо этого он неявно отменяет регистрацию при освобождении последнего объекта UI Automation.

Пример, демонстрирующий регистрацию пользовательского шаблона элемента управления, см. в следующем разделе.

### <a name="example-implementation-of-a-custom-control-pattern"></a>Пример реализации пользовательского шаблона элемента управления

В этом разделе содержится пример кода, демонстрирующий реализацию объектов-оболочек клиента и обработчика шаблона для пользовательского шаблона элемента управления. В примере реализуется пользовательский шаблон элемента управления, основанный на шаблоне элемента управления [value](uiauto-implementingvalue.md) .


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Разработка пользовательских свойств, событий и шаблонов элементов управления](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[Общие сведения о свойствах автоматизированного пользовательского интерфейса](uiauto-propertiesoverview.md)
</dt> <dt>

[Обзор событий автоматизации пользовательского интерфейса](uiauto-eventsoverview.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 