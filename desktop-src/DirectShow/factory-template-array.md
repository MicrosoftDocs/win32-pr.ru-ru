---
description: Массив шаблонов фабрики
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Массив шаблонов фабрики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1888a2a054473865c713d96cdfa5706c35229dc938f23513a95066176ab138c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401849"
---
# <a name="factory-template-array"></a>Массив шаблонов фабрики

Шаблон фабрики содержит следующие открытые переменные члена:

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

Два указателя функций, [**m \_ лпфннев**](cfactorytemplate-m-lpfnnew.md) и [**m \_ лпфнинит**](cfactorytemplate-m-lpfninit.md), используют следующие определения типов:

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

Первый — это функция создания экземпляра для компонента. Второй — Необязательная функция инициализации. Если вы предоставляете функцию инициализации, она вызывается из функции точки входа DLL. (Функция точки входа DLL обсуждается далее в этой статье.)

Предположим, вы создаете библиотеку DLL, содержащую компонент с именем Кмикомпонент, который наследует от [**кункновн**](cunknown.md). В библиотеке DLL необходимо указать следующие элементы:

-   Функция инициализации — открытый метод, возвращающий новый экземпляр Кмикомпонент.
-   Глобальный массив шаблонов фабрики, именуемый *g \_ Templates.* Этот массив содержит шаблон фабрики для Кмикомпонент.
-   Глобальная переменная с именем *g \_ ктемплатес* , указывающая размер массива.

В следующем примере показано, как объявить эти элементы:


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



`CreateInstance`Метод вызывает конструктор класса и возвращает указатель на новый экземпляр класса. Параметр *Punk* является указателем на агрегатор [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Этот параметр можно просто передать конструктору класса. Параметр *фр* является указателем на значение HRESULT. Конструктор класса присваивает этому свойству соответствующее значение, но если конструктор завершается неудачно, задайте для него значение E \_ OUTOFMEMORY.

Макрос [**Name**](name.md) создает строку в отладочных сборках, но разрешается в **значение NULL** в розничных сборках. Он используется в этом примере для присвоения компоненту имени, которое отображается в журналах отладки, но не занимается памятью в окончательной версии.

`CreateInstance`Метод может иметь любое имя, так как фабрика классов ссылается на указатель на функцию в шаблоне фабрики. Однако *\_ шаблоны g* и *g \_ ктемплатес* являются глобальными переменными, которые фабрика класса планирует найти, поэтому они должны иметь в точности эти имена.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[создание библиотеки DLL для фильтра DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
