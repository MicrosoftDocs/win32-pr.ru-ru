---
title: Пользовательские эффекты
description: Описание процесса написания собственных пользовательских эффектов с помощью стандартных HLSL.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134527"
---
# <a name="custom-effects"></a>Пользовательские эффекты

[Direct2D](./direct2d-portal.md) поставляется с библиотекой эффектов, которые выполняют различные распространенные операции с образами. Полный список эффектов см. в разделе [встроенные эффекты](built-in-effects.md) . Для функций, которые не могут быть реализованы с помощью встроенных эффектов, Direct2D позволяет создавать собственные пользовательские эффекты с использованием стандартных [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl). Эти пользовательские эффекты можно использовать вместе со встроенными эффектами, поставляемыми с Direct2D.

Примеры результатов полного шейдера пикселей, вершины и вычислений см. в [примере D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

В этом разделе мы покажем вам шаги и понятия, необходимые для проектирования и создания полнофункционального пользовательского действия.

## <a name="introduction-what-is-inside-an-effect"></a>Введение. что находится в силе?

![Диаграмма эффектов тени.](images/custom-effects1.png)

По сути, эффект [Direct2D](./direct2d-portal.md) выполняет задачу создания образов, например изменение яркости, снятие насыщенности изображения или, как показано выше, путем создания тени. Для приложения они просты. Они могут принимать ноль или более входных изображений, предоставлять несколько свойств, управляющих их работой, и создавать одно выходное изображение.

Существует четыре различные части пользовательского действия, за которые отвечает Автор:

1.  Интерфейс Effect: интерфейс влияния концептуально определяет, как приложение взаимодействует с пользовательским действием (например, количество входов, принимаемых этим действием и доступные свойства). Интерфейс Effect управляет графом преобразования, который содержит фактические операции с образами.
2.  Граф преобразования: каждый результат создает внутренний граф преобразования, состоящие из отдельных преобразований. Каждое преобразование представляет одну операцию с изображением. Этот результат отвечает за связывание этих преобразований в графе для выполнения предполагаемого применения образов. Результат может добавлять, удалять, изменять и переупорядочивать преобразования в ответ на изменения внешних свойств эффектов.
3.  Преобразование: Преобразование представляет одну операцию с изображением. Его основное назначение заключается в размещении шейдеров, которые выполняются для каждого выходного пикселя. Для этого он отвечает за вычисление нового размера выходного изображения на основе логики в шейдерах. Кроме того, необходимо вычислить область входного изображения, из которой должны считываться шейдеры для отрисовки запрошенной выходной области.
4.  Шейдер. шейдер выполняется для входных данных преобразования на GPU (или ЦП, если программная отрисовка указывается, когда приложение создает устройство Direct3D). Шейдеры эффектов записываются на языке штриховки высокого уровня ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) и компилируются в байтовый код во время компиляции, которая затем загружается с помощью этого действия во время выполнения. В этом справочном документе описано, как написать HLSL, совместимый с [Direct2D](./direct2d-portal.md). В документации по Direct3D содержится базовый обзор HLSL.

## <a name="creating-an-effect-interface"></a>Создание интерфейса Effect

Интерфейс Effect определяет, как приложение взаимодействует с пользовательским действием. Чтобы создать интерфейс Effects, класс должен реализовывать ID2D1EffectImpl, определять метаданные, описывающие этот результат (например, его имя, число входов и свойства), а также создавать методы, которые регистрируют Пользовательский результат для использования с [Direct2D](./direct2d-portal.md).

После реализации всех компонентов интерфейса Effect заголовок Class будет выглядеть следующим образом:


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a>Реализация ID2D1EffectImpl

Интерфейс [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) содержит три метода, которые необходимо реализовать:

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a>Инициализация (ID2D1EffectContext \* пконтекстинтернал, ID2D1TransformGraph \* птрансформграф)

[Direct2D](./direct2d-portal.md) вызывает метод [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) после того, как приложение вызовет метод [**ID2D1DeviceContext:: креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) . Этот метод можно использовать для выполнения внутренней инициализации или любых других операций, необходимых для этого действия. Кроме того, его можно использовать для создания исходного графа преобразования эффектов.

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a>Сетграф (ID2D1TransformGraph \* птрансформграф)

[Direct2D](./direct2d-portal.md) вызывает метод [**сетграф**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) , когда изменяется число входов для результата. Хотя большинство эффектов имеют постоянное число входов, другие, такие как [составной эффект](composite.md) , поддерживают переменное число входов. Этот метод позволяет этим эффектам обновить Граф преобразований в ответ на изменение счетчика входных данных. Если воздействие не поддерживает переменное число входов, этот метод может просто вернуть E \_ нотимпл.

### <a name="prepareforrender-d2d1_change_type-changetype"></a>Препарефоррендер (D2D1 \_ изменение \_ типа изменения)

Метод [**препарефоррендер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) предоставляет возможности для выполнения любых операций в ответ на внешние изменения. [Direct2D](./direct2d-portal.md) вызывает этот метод непосредственно перед отображением результата, если выполняется хотя бы одно из следующих условий:

-   Этот результат был ранее инициализирован, но еще не нарисован.
-   Свойство Effect изменилось с момента последнего вызова Draw.
-   Состояние вызывающего контекста [Direct2D](./direct2d-portal.md) (например, DPI) изменилось с момента последнего вызова Draw.

### <a name="implement-the-effect-registration-and-callback-methods"></a>Реализация методов регистрации эффектов и обратного вызова

Приложения должны зарегистрировать эффекты с помощью [Direct2D](./direct2d-portal.md) , прежде чем создавать их экземпляры. Эта регистрация ограничивается экземпляром фабрики Direct2D и должна повторяться каждый раз при запуске приложения. Чтобы включить эту регистрацию, Пользовательский результат определяет уникальный идентификатор GUID, Открытый метод, который регистрирует этот результат, и закрытый метод обратного вызова, который возвращает экземпляр этого действия.

### <a name="define-a-guid"></a>Определение GUID

Необходимо определить идентификатор GUID, который однозначно определяет результат регистрации с помощью [Direct2D](./direct2d-portal.md). Приложение использует то же самое для обнаружения результата при вызове [**ID2D1DeviceContext:: креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).

Этот код демонстрирует определение такого идентификатора GUID для воздействия. Необходимо создать собственный уникальный идентификатор GUID с помощью средства создания GUID, например guidgen.exe.


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a>Определение общедоступного метода регистрации

Затем определите открытый метод для вызова приложения, чтобы зарегистрировать воздействие на [Direct2D](./direct2d-portal.md). Так как регистрация влияния зависит от экземпляра фабрики Direct2D, метод принимает интерфейс [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) в качестве параметра. Чтобы зарегистрировать этот результат, метод вызывает API [**ID2D1Factory1:: регистереффектфромстринг**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) в параметре **ID2D1Factory1** .

Этот API принимает XML-строку, описывающую метаданные, входные данные и свойства этого действия. Метаданные для этого действия предназначены только для информационных целей и могут запрашиваться приложением через интерфейс [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) . Данные входных данных и свойств, с другой стороны, используются [Direct2D](./direct2d-portal.md) и представляют функциональность эффектов.

Ниже показана XML-строка для минимального результата выборки. Добавление пользовательских свойств в XML рассматривается в разделе Добавление пользовательских свойств в раздел эффектов.


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a>Определение метода обратного вызова фабрики эффектов

Этот результат также должен предоставлять закрытый метод обратного вызова, который возвращает экземпляр действия с помощью одного параметра IUnknown \* \* . Указатель на этот метод предоставляется для [Direct2D](./direct2d-portal.md) , когда результат регистрируется через API [**ID2D1Factory1:: регистереффектфромстринг**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) через параметр [**\_ \_ фабрики PD2D1 Effect**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a>Реализация интерфейса IUnknown

Наконец, в результате должен быть реализован интерфейс IUnknown для совместимости с COM.

## <a name="creating-the-effects-transform-graph"></a>Создание графа преобразования эффектов

В результате может использоваться несколько различных преобразований (отдельных операций с изображениями), чтобы создать требуемый результат создания образа. Для управления порядком, в котором эти преобразования применяются к изображению ввода, он упорядочивает их в графе преобразования. Граф преобразования может использовать эффекты и преобразования, входящие в [Direct2D](./direct2d-portal.md) , а также пользовательские преобразования, созданные автором эффекта.

### <a name="using-transforms-included-with-direct2d"></a>Использование преобразований, входящих в состав Direct2D

Это наиболее часто используемые преобразования, предоставляемые с [Direct2D](./direct2d-portal.md).

-   [**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform). это преобразование смешивает произвольное число входов вместе с описанием смешения, см. раздел [**\_ \_ Описание D2D1 Blend**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) и [Пример составных эффектов Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) для примеров смешения. Это преобразование возвращается методом [**ID2D1EffectContext:: креатеблендтрансформ**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .
-   [**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): это преобразование расширяет размер вывода изображения в соответствии с заданным [**\_ \_ режимом расширения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) . Это преобразование возвращается методом [**ID2D1EffectContext:: креатебордертрансформ**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .
-   [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): это преобразование смещает (преобразует) свои входные данные на любое целое число пикселей. Это преобразование возвращается методом [**ID2D1EffectContext:: креатеоффсеттрансформ**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .
-   Любой существующий результат может рассматриваться как преобразование в целях создания графа преобразования с помощью метода [**ID2D1EffectContext:: креатетрансформнодефромеффект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .

### <a name="creating-a-single-node-transform-graph"></a>Создание графа преобразования с одним узлом

После создания преобразования входные данные этого действия должны быть подключены к входным данным преобразования, а выходные данные преобразования должны быть подключены к выходным данным этого результата. Если результат содержит только одно преобразование, для этого можно использовать метод [**ID2D1TransformGraph:: сетсинглетрансформноде**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) .

Можно создать или изменить преобразование в методах [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) или [**сетграф**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) действия с помощью предоставленного параметра ID2D1TransformGraph. Если в результате изменения графа преобразования в другом методе, где этот параметр недоступен, результат может быть [**сохранен в качестве**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) переменной-члена класса и обращаться к нему в другом месте, например [**препарефоррендер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) или метод обратного вызова настраиваемого свойства.

Пример метода [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) показан здесь. Этот метод создает граф преобразования с одним узлом, который смещает изображение на 100 пикселей на каждой оси.


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a>Создание графа преобразования с несколькими узлами

Добавление нескольких преобразований к графу преобразования эффекта позволяет внутренним образом выполнять несколько операций с изображениями, представляемых приложению в виде единого единого эффекта.

Как отмечалось выше, граф преобразования результата можно изменить в любом методе Effect, используя параметр [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) , полученный в методе [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) этого действия. Для создания или изменения графа преобразования эффектов можно использовать следующие API-интерфейсы:

### <a name="addnodeid2d1transformnode-pnode"></a>AddNode (ID2D1TransformNode \* пноде)

Метод [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , фактически, регистрирует преобразование с результатом и должен вызываться перед тем, как преобразование можно будет использовать с любыми другими методами графа преобразования.

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a>Коннекттоеффектинпут (UINT32 Тоеффектинпутиндекс, ID2D1TransformNode \* пноде, UINT32 тонодеинпутиндекс)

Метод [**коннекттоеффектинпут**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) соединяет входные данные изображения эффектов с входными данными преобразования. Один и тот же ввод результата может быть подключен к нескольким преобразованиям.

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a>Коннектноде (ID2D1TransformNode \* пфромноде, ID2D1TransformNode \* ПТОНОДЕ, UINT32 тонодеинпутиндекс)

Метод [**коннектноде**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) подключает выходные данные преобразования к входу другого преобразования. Выход преобразования может быть подключен к нескольким преобразованиям.

### <a name="setoutputnodeid2d1transformnode-pnode"></a>Сетаутпутноде (ID2D1TransformNode \* пноде)

Метод [**сетаутпутноде**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) соединяет выходные данные преобразования с выходными данными результата. Поскольку результат имеет только один выход, в качестве выходного узла можно назначить только одно преобразование.

Этот код использует два отдельных преобразования для создания единого воздействия. В этом случае эффектом является переведенная тень.


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a>Добавление пользовательских свойств к результату

Эффекты могут определять пользовательские свойства, позволяющие приложению изменять поведение эффекта во время выполнения. Определение свойства для пользовательского действия состоит из трех этапов:

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a>Добавление метаданных свойства в данные регистрации действия

### <a name="add-property-to-registration-xml"></a>Добавление свойства в XML-файл регистрации

Необходимо определить свойства пользовательского действия во время начальной регистрации этого действия с помощью [Direct2D](./direct2d-portal.md). Сначала необходимо обновить XML-код регистрации результата в общедоступном методе регистрации с помощью нового свойства:


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



При определении свойства Effect в XML требуется имя, тип и отображаемое имя. Отображаемое имя свойства, а также значения категории, автора и описания общего результата могут быть локализованы.

Для каждого свойства в результате можно дополнительно указать значения по умолчанию, min и Max. Эти значения предназначены только для использования в информационных целях. Они не применяются функцией [Direct2D](./direct2d-portal.md). Вы самостоятельно реализуете любую логику по умолчанию/min/max в классе Effect.

Значение типа, указанное в XML-коде для свойства, должно соответствовать соответствующему типу данных, используемому методами getter и Setter свойства. В этой таблице показаны соответствующие значения XML для каждого типа данных:



| Тип данных                                                                                                                              | Соответствующее значение XML |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| пвстр                                                                                                                                  | строка                  |
| BOOL                                                                                                                                   | bool                    |
| UINT                                                                                                                                   | uint32                  |
| INT                                                                                                                                    | int32                   |
| FLOAT                                                                                                                                  | FLOAT                   |
| [**\_Экземпляр D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | Vector2                 |
| [**\_3F вектора D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | Vector3                 |
| [**\_4F вектора D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | Vector4                 |
| [**\_Матрица D2D \_ 3X2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool)) | matrix3x2               |
| [**\_Матрица D2D \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | matrix4x3               |
| [**\_Матрица D2D \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | matrix4x4               |
| [**\_Матрица D2D \_ 5x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | matrix5x4               |
| ДВУХБАЙТОВЫХ\[\]                                                                                                                               | большой двоичный объект                    |
| IUnknown\*                                                                                                                             | IUnknown                |
| [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*                                                                                       | колорконтекст            |
| CLSID                                                                                                                                  | clsid                   |
| Перечисление ([**\_ \_ Режим интерполяции D2D1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode)и т. д.)                                                | enum                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a>Сопоставьте новое свойство с методами getter и Set

Далее результат должен сопоставлять это новое свойство с методами getter и Set. Это делается через массив [**\_ \_ привязки свойств D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) , который передается в метод [**ID2D1Factory1:: регистереффектфромстринг**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .

Массив [**\_ \_ привязки свойств D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) выглядит следующим образом:


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



После создания массива XML и привязок передайте их в метод [**регистереффектфромстринг**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



\_ \_ \_ Для макроса привязки типа значения D2D1 требуется, чтобы класс Effect наследовал от [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) перед любым другим интерфейсом.

Пользовательские свойства для воздействия индексируются в том порядке, в котором они объявляются в XML, а после создания могут быть доступны в приложении с помощью методов [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) и [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) . Для удобства можно создать общедоступное перечисление, в котором перечислены все свойства в файле заголовка результата.


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a>Создание методов getter и Setter для свойства

Следующим шагом является создание методов getter и Setter для нового свойства. Имена методов должны совпадать с именами, указанными в массиве [**\_ \_ привязки свойства D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) . Кроме того, тип свойства, указанный в XML-коде действия, должен соответствовать типу параметра метода задания и возвращаемому значению метода Getter.


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a>Преобразование эффектов обновления в ответ на изменение свойства

Чтобы фактически обновить вывод изображения в ответ на изменение свойства, результат должен изменить его базовые преобразования. Обычно это делается в методе [**препарефоррендер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) в результате, который [Direct2D](./direct2d-portal.md) автоматически вызывает, когда одно из свойств эффектов изменилось. Однако преобразования могут быть обновлены в любом из методов, таких как инициализация или методы задания свойств эффектов.

Например, если в результате содержался [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) и требовалось изменить значение смещения в ответ на изменение свойства Offset этого действия, в [**препарефоррендер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender)будет добавлен следующий код:


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a>Создание пользовательского преобразования

Чтобы реализовать операции с изображениями, помимо предоставляемых в [Direct2D](./direct2d-portal.md), необходимо реализовать пользовательские преобразования. Пользовательские преобразования могут произвольно изменить входной образ с помощью настраиваемых шейдеров HLSL.

Преобразования реализуют один из двух различных интерфейсов в зависимости от используемых типов шейдеров. Преобразования с помощью пиксельных и/или шейдеров вершин должны реализовывать [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), а преобразования с использованием шейдеров вычислений должны реализовывать [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform). Эти интерфейсы наследуют от [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform). В этом разделе основное внимание уделяется реализации функций, общих для обоих.

Интерфейс [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) имеет четыре метода для реализации:

### <a name="getinputcount"></a>GetInputCount

Этот метод возвращает целое число, представляющее число входных данных для преобразования.


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a>мапинпутректстуутпутрект

[Direct2D](./direct2d-portal.md) вызывает метод [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) каждый раз при отрисовке преобразования. Direct2D передает прямоугольник, представляющий границы каждого из входных данных для преобразования. Затем преобразование отвечает за вычисление границ выходного изображения. Размер прямоугольников для всех методов на этом интерфейсе ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) определяется в пикселях, а не DIP.

Этот метод также отвечает за вычисление области выходных данных, которые являются непрозрачными в зависимости от логики его шейдера и непрозрачных регионов каждого входного параметра. Непрозрачная область изображения определяется так, чтобы альфа-канал был "1" для всего прямоугольника. Если неясно, является ли выход преобразования непрозрачным, то непрозрачный для вывода прямоугольник должен иметь значение (0, 0, 0, 0) в качестве безопасного значения. [Direct2D](./direct2d-portal.md) использует эти сведения для оптимизации подготовки к просмотру с гарантированно непрозрачным содержимым. Если это значение неверное, это может привести к неправильной отрисовке.

Во время выполнения этого метода можно изменить поведение при отрисовке преобразования (как определено в разделах с 6 по 8). Однако вы не можете изменить другие преобразования в графе преобразования или схему диаграммы здесь.


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



Для более сложного примера рассмотрим, как будет представлено простое размытие:

Если в операции размытия используется радиус 5 пикселей, размер прямоугольника вывода должен расширяться на 5 пикселей, как показано ниже. При изменении координат прямоугольника преобразование должно гарантировать, что его логика не приведет к превышению или потере точности в координатах прямоугольника.


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



Поскольку изображение размыто, область изображения, которая была непрозрачной, теперь может быть частично прозрачной. Это связано с тем, что область за пределами изображения по умолчанию имеет прозрачный черный цвет, и эта прозрачность будет смешиваться с краями вокруг краев изображения. Преобразование должно отражать это в выводимых вычислениях непрозрачных прямоугольников:


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



Эти вычисления отображаются здесь:

![Иллюстрация вычисления прямоугольника.](images/custom-effects2.png)

Дополнительные сведения об этом методе см. на странице справочника по [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .

### <a name="mapoutputrecttoinputrects"></a>мапаутпутректтоинпутректс

[Direct2D](./direct2d-portal.md) вызывает метод [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) после [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). Преобразование должно вычислить часть изображения, из которой он должен быть считан, чтобы правильно отобразить запрошенную выходную область.

Как и ранее, если результат строго сопоставляет пикселы 1-1, он может передать прямоугольник вывода через прямоугольник ввода:


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



Аналогично, если преобразование сжимает или развертывает изображение (например, пример размытия), Пиксели часто используют окружающие Пиксели для вычисления их значения. При размытии пиксел вычисляется с учетом окружающих его пикселов, даже если они выходят за границы входного изображения. Это поведение отражается в вычислении. Как и ранее, преобразование проверяет наличие перекрывающихся точек при расширении координат прямоугольника.


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



На этом рисунке показано вычисление. [Direct2D](./direct2d-portal.md) автоматически выбирает прозрачные черные пиксели, где не существует входного изображения, что позволяет постепенно смешивать размытие с существующим содержимым на экране.

![Иллюстрация непрозрачных черных точек с выборкой эффектов за пределами прямоугольника.](images/custom-effects3.png)

Если сопоставление не является тривиальным, этот метод должен установить максимальный размер области, чтобы гарантировать правильность результатов. Для этого установите для левого и верхнего краев значение INT \_ min, а правое и нижнее края — максимум int \_ .

Дополнительные сведения об этом методе см. в разделе [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .

### <a name="mapinvalidrect"></a>мапинвалидрект

[Direct2D](./direct2d-portal.md) также вызывает метод [**мапинвалидрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Однако, в отличие от методов [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) и [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) , Direct2D не гарантирует его вызов в определенный момент времени. Этот метод концептуально определяет, какая часть выходных данных преобразования должна быть повторно подготовлена в ответ на часть или все изменения входных данных. Существует три разных сценария для вычисления недопустимого Rect преобразования.

### <a name="transforms-with-one-to-one-pixel-mapping"></a>Преобразование с сопоставлением "один к одному" в пикселях

Для преобразований, которые сопоставляют пиксел 1-1, просто передают Недопустимый входной прямоугольник в недопустимый выходной прямоугольник:


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a>Преобразования с сопоставлением "многие ко многим" в пикселях

Если выходные точки преобразования зависят от окружающей области, недопустимый входной прямоугольник должен быть развернут соответствующим образом. Это необходимо для отражения того, что пиксели вокруг недопустимого прямоугольника ввода также будут затронуты и станут недействительными. Например, размытие в 5 пикселей использует следующее вычисление:


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a>Преобразования со сложным сопоставлением пикселей

Для преобразований, где входные и выходные Пиксели не имеют простого сопоставления, все выходные данные могут быть помечены как недопустимые. Например, если преобразование просто выводит средний цвет входных данных, все выходные данные преобразования преобразуются, если изменяется даже небольшая часть входных данных. В этом случае недопустимый прямоугольник вывода должен быть задан логически бесконечным прямоугольником (как показано ниже). [Direct2D](./direct2d-portal.md) автоматически применяет это к границам выходных данных.


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



Дополнительные сведения об этом методе см. в разделе [**мапинвалидрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .

После реализации этих методов заголовок преобразования будет содержать следующее:


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a>Добавление шейдера пикселей к пользовательскому преобразованию

После создания преобразования необходимо предоставить шейдер, который будет манипулировать пикселями изображения. В этом разделе описаны шаги по использованию шейдера пикселей с пользовательским преобразованием.

### <a name="implementing-id2d1drawtransform"></a>Реализация ID2D1DrawTransform

Для использования шейдера пикселей преобразование должно реализовывать интерфейс [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , который наследуется от интерфейса [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) , описанного в разделе 5. Этот интерфейс содержит один новый метод для реализации:

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a>Сетдравинфо (ID2D1DrawInfo \* пдравинфо)

[Direct2D](./direct2d-portal.md) вызывает метод [**сетдравинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) при первом добавлении преобразования к графу преобразования воздействия. Этот метод предоставляет параметр [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) , который управляет отображением преобразования. Методы, доступные здесь, см. в разделе **ID2D1DrawInfo** .

Если преобразование выбирает сохранение этого параметра в качестве переменной-члена класса, доступ к объекту *дравинфо* можно получить и изменить с других методов, таких как методы задания свойств или [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). В частности, ее нельзя вызывать из методов [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) или [**мапинвалидрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) в [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).

### <a name="creating-a-guid-for-the-pixel-shader"></a>Создание идентификатора GUID для шейдера пикселей

Затем преобразование должно определить уникальный идентификатор GUID для самого построителя текстуры. Это используется, когда [Direct2D](./direct2d-portal.md) загружает шейдер в память, а также когда преобразование выбирает, какой шейдер пикселей использовать для выполнения. Такие средства, как guidgen.exe, включенные в Visual Studio, можно использовать для создания случайного идентификатора GUID.


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a>Загрузка построителя текстуры с помощью Direct2D

Построитель текстуры необходимо загрузить в память, прежде чем его можно будет использовать в преобразовании.

Чтобы загрузить шейдер пикселей в память, преобразование должно считать скомпилированный байтовый код шейдера из. Файл CSO, созданный Visual Studio (подробные сведения см. в документации по [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ), в массив байтов. Этот метод подробно описан в [примере D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

После загрузки данных шейдера в массив байтов вызовите метод [**лоадпикселшадер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) объекта [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) результата. [Direct2D](./direct2d-portal.md) игнорирует вызовы **лоадпикселшадер** , если уже загружен шейдер с таким же идентификатором GUID.

После загрузки построителя текстуры в память преобразование необходимо выбрать для выполнения, передав его идентификатор GUID методу [**сетпикселшадер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) в параметре [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) , предоставленном в методе [**сетдравинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) . Перед тем как выбрать для выполнения, шейдер пикселей должен быть уже загружен в память.

### <a name="changing-shader-operation-with-constant-buffers"></a>Изменение операции шейдера с постоянными буферами

Чтобы изменить способ выполнения шейдера, преобразование может передать буфер константы в шейдер пикселей. Для этого преобразование определяет структуру, содержащую нужные переменные в заголовке класса:


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



Затем преобразование вызывает метод [**ID2D1DrawInfo:: сетпикселшадерконстантбуффер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) для параметра [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) , указанного в методе [**сетдравинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) , чтобы передать этот буфер шейдеру.

[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) также необходимо определить соответствующую структуру, которая представляет буфер констант. Переменные, содержащиеся в структуре шейдера, должны соответствовать значениям в структуре преобразования.


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



После определения буфера значения, содержащиеся в, могут быть считаны в любом месте шейдера пикселей.

### <a name="writing-a-pixel-shader-for-direct2d"></a>Создание построителя текстуры для Direct2D

Преобразования [Direct2D](./direct2d-portal.md) используют шейдеры, созданные с помощью стандартного [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl). Однако существует несколько ключевых концепций для написания шейдера пикселей, выполняемого из контекста преобразования. Готовый пример полностью функционального шейдера пикселей см. в [примере D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

[Direct2D](./direct2d-portal.md) автоматически сопоставляет входные данные преобразования с объектами [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) и [**самплерстате**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) в HLSL. Первый **Texture2D** находится в папке Register T0, а первый **самплерстате** находится в регистре S0. Каждый дополнительный вход находится в следующих соответствующих регистрах (например, T1 и S1). Данные в пикселях для определенных входных данных могут быть выборке путем вызова Sample в объекте **Texture2D** и передачи соответствующего объекта **самплерстате** и координат шаг текселя.

Пользовательский шейдер пикселей выполняется один раз для каждого отображаемого пикселя. При каждом запуске шейдера [Direct2D](./direct2d-portal.md) автоматически предоставляет три параметра, которые обозначают текущее расположение выполнения:

-   Выходное пространство сцены. Этот параметр представляет текущую точку выполнения с точки зрения общей целевой поверхности. Он определен в пикселях, а его минимальное и максимальное значения соответствуют границам прямоугольника, возвращаемого функцией [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).
-   Выходные данные клипа: этот параметр используется Direct3D и не должен использоваться в шейдере пикселей преобразования.
-   Шаг текселя-Space input: этот параметр представляет текущую точку выполнения в определенной текстуре ввода. Шейдер не должен зависеть от того, как вычисляется это значение. Он должен использовать его только для выборки входных шейдеров пикселей, как показано в приведенном ниже коде.


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a>Добавление шейдера вершин к пользовательскому преобразованию

Шейдеры вершин можно использовать для выполнения различных сценариев работы с образами, чем шейдеры пикселей. В частности, шейдеры вершин могут выполнять эффекты изображений на основе геометрии путем преобразования вершин, составляющих изображение. Шейдеры вершин можно использовать независимо друг от друга и в сочетании с заданными шейдерами пикселей. Если шейдер вершин не указан, [Direct2D](./direct2d-portal.md) замещает в шейдер вершин по умолчанию для использования с пользовательским шейдером пикселей.

Процесс добавления шейдера вершин к пользовательскому преобразованию аналогичен построителю построителей текстуры — преобразование реализует интерфейс [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , создает идентификатор GUID и (необязательно) передает буферы константы в шейдер. Однако существует несколько основных дополнительных шагов, которые являются уникальными для шейдеров вершин.

### <a name="creating-a-vertex-buffer"></a>Создание буфера вершин

Шейдер вершин по определению выполняется для переданных вершин, а не для отдельных пикселов. Чтобы указать вершины для выполнения в шейдере, преобразование создает буфер вершин для передачи шейдеру. Макет буферов вершин выходит за рамки данного документа. Дополнительные сведения см. в [справочнике по Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) или [примере D2DCustomEffects SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) для примера реализации.

После создания буфера вершин в памяти преобразование использует метод [**креатевертексбуффер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) объекта [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) содержащего его результата для передачи этих данных в GPU. Пример реализации см. в [примере пакета SDK для D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) .

Если преобразование не указывает ни одного буфера вершин, [Direct2D](./direct2d-portal.md) передает буфер вершин по умолчанию, представляющий расположение прямоугольного изображения.

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a>Изменение Сетдравинфо для использования шейдера вершин

Как и в шейдерах пикселей, преобразование должно загрузиться и выбрать шейдер вершин для выполнения. Чтобы загрузить шейдер вершин, он вызывает метод [**лоадвертексшадер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) для метода [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) , полученного в методе Initialize результата. Чтобы выбрать шейдер вершин для выполнения, он вызывает [**сетвертекспроцессинг**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) в параметре [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) , полученном в методе [**сетдравинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) преобразования. Этот метод принимает идентификатор GUID для ранее загруженного шейдера вершин, а также (дополнительно) созданного ранее буфера вершин для выполнения шейдера.

### <a name="implementing-a-direct2d-vertex-shader"></a>Реализация шейдера вершин Direct2D

Преобразование «Рисование» может содержать как шейдер пикселей, так и шейдер вершин. Если преобразование определяет и шейдер пикселей, и шейдер вершин, то выходные данные шейдера вершин передаются непосредственно шейдеру пикселей. приложение может настроить возвращаемую сигнатуру шейдера вершин или параметры шейдера пикселей, если они являются единообразными.

С другой стороны, если преобразование содержит только шейдер вершин и полагается на построитель текстуры [Direct2D](./direct2d-portal.md)по умолчанию, он должен вернуть следующий результат по умолчанию:


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Шейдер вершин сохраняет результат преобразований вершин в выходной переменной построителя текстуры. Чтобы вычислить выходные данные в пространстве Clip и шаг текселя переменные, [Direct2D](./direct2d-portal.md) автоматически предоставляет матрицы преобразования в буфере констант:


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



Ниже приведен пример кода шейдера вершин, в котором используются матрицы преобразования для вычисления правильных шаг текселя и пробелов, ожидаемых [Direct2D](./direct2d-portal.md):


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



Приведенный выше код можно использовать в качестве отправной точки для шейдера вершин. Он просто проходит через входной образ без выполнения преобразований. См. [Пример D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) для полностью реализованного преобразования на основе шейдера вершин.

Если в преобразовании не задан буфер вершин, [Direct2D](./direct2d-portal.md) заменяет в буфере вершин по умолчанию, представляющего Прямоугольное расположение изображения. Параметры шейдера вершин заменяются на значения, указанные в выходных данных шейдера по умолчанию:


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Шейдер вершин не может изменять параметры *сценеспацеаутпут* и *клипспацеаутпут* . Он должен вернуть их без изменений. Однако это может привести к изменению параметров *текселспацеинпут* для каждого входного изображения. Если преобразование также содержит пользовательский шейдер пикселей, шейдер вершин по-прежнему может передавать дополнительные пользовательские параметры непосредственно в шейдер пикселей. Кроме того, пользовательский буфер матриц преобразования *сценеспаце* (B0) больше не предоставляется.

## <a name="adding-a-compute-shader-to-a-custom-transform"></a>Добавление шейдера вычислений к пользовательскому преобразованию

Наконец, пользовательские преобразования могут использовать шейдеры вычислений для определенных целевых сценариев. Шейдеры вычислений можно использовать для реализации сложных эффектов изображения, требующих произвольного доступа к входным и выходным буферам изображений. Например, базовый алгоритм гистограммы не может быть реализован с шейдером пикселей из-за ограничений доступа к памяти.

Поскольку шейдеры вычислений имеют более высокие требования к оборудованию, чем шейдеры пикселей, следует использовать шейдеры пикселей, если это возможно для реализации данного воздействия. В частности, шейдеры вычислений работают только на большинстве карт на уровне DirectX 10 и выше. Если преобразование выбирает использование шейдера вычислений, оно должно проверять наличие соответствующей аппаратной поддержки во время создания экземпляра в дополнение к реализации интерфейса [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .

### <a name="checking-for-compute-shader-support"></a>Проверка поддержки шейдера вычислений

Если действие использует шейдер вычислений, оно должно проверять поддержку шейдера вычислений во время его создания с помощью метода [**ID2D1EffectContext:: чеккфеатуресуппорт**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) . Если GPU не поддерживает шейдеры вычислений, этот результат должен возвращать [**D2DERR \_ недостаточных \_ \_ возможностей устройства**](direct2d-error-codes.md).

Существует два разных типа шейдеров вычислений, которые может использовать преобразование: Shader Model 4 (DirectX 10) и Shader Model 5 (DirectX 11). Существуют определенные ограничения шейдера Shader Model 4. Дополнительные сведения см. в документации по [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) . Преобразования могут содержать оба типа шейдеров и могут возвращаться к модели шейдера 4 при необходимости: см. [Пример D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) для реализации этого.

### <a name="implement-id2d1computetransform"></a>Реализация ID2D1ComputeTransform

Этот интерфейс содержит два новых метода для реализации в дополнение к классам в [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a>Сеткомпутеинфо (ID2D1ComputeInfo \* пкомпутеинфо)

Как и в шейдерах пикселей и вершин, [Direct2D](./direct2d-portal.md) вызывает метод [**сеткомпутеинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) при первом добавлении преобразования к графу преобразования воздействия. Этот метод предоставляет параметр [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) , который управляет отображением преобразования. Это включает выбор шейдера вычислений для выполнения с помощью метода [**ID2D1ComputeInfo:: сеткомпутешадер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) . Если преобразование выбирает сохранение этого параметра в качестве переменной-члена класса, к нему можно получить доступ и изменить любой метод преобразования или воздействия с исключением методов [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) и [**мапинвалидрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Другие методы, доступные здесь, см. в разделе **ID2D1ComputeInfo** .

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a>Калкулатесреадграупс (ID2D1ComputeInfo \* паутпутрект, UInt32 \* ПДИМЕНСИОНКС, UInt32 \* пдименсиони, UInt32 \* пдименсионз)

В то время как шейдеры пикселей выполняются для каждого отдельного пикселя, а шейдеры вершин выполняются для каждой вершины, шейдеры вычислений выполняются для каждого 'среадграуп. Среадграуп представляет собой количество потоков, выполняемых параллельно на GPU. Код HLSLа COMPUTE Shader определяет, сколько потоков должно выполняться для каждого среадграуп. Этот результат масштабирует количество среадграупс, чтобы шейдер выполнял нужное количество раз, в зависимости от логики шейдера.

Метод [**калкулатесреадграупс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) позволяет преобразованию сообщать [Direct2D](./direct2d-portal.md) о том, сколько групп потоков требуется, в зависимости от размера изображения и собственных знаний о преобразовании шейдера.

Количество раз, когда выполняется шейдер вычислений, — это продукт с указанными здесь счетчиками среадграуп и заметка "numthreads" в [HLSLе](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)COMPUTE Shader. Например, если преобразование задает среадграуп измерения (2, 2, 1), то шейдер задаст (3, 3, 1) потоки на среадграуп, затем будет выполняться 4 среадграупс, каждый с 9 потоками в них, всего 36 экземпляров потоков.

Распространенным сценарием является обработка одного выходного пикселя для каждого экземпляра вычислительного шейдера. Чтобы вычислить количество групп потоков для этого сценария, преобразование делит ширину и высоту изображения на соответствующие измерения x и y заметки "numthreads" в Compute Shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).

Важно! при выполнении этого деления число запрошенных групп потоков должно быть округлено до ближайшего целого числа, в противном случае "остаток" не будет выполняться после. Если шейдер (например) рассчитывает один пиксель с каждым потоком, код метода будет выглядеть следующим образом.


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) использует следующий код, чтобы указать число потоков в каждой группе потоков:


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



Во время выполнения текущий индекс потока и текущий среадграуп передаются в качестве параметров в метод шейдера:


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a>Чтение данных изображения

С помощью шейдеров вычислений доступ к входному изображению преобразования можно получить в виде одной двухмерной текстуры:


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



Однако, как и шейдеры пикселей, данные изображения не обязательно должны начинаться с (0,0) на текстуре. Вместо этого [Direct2D](./direct2d-portal.md) предоставляет системные константы, позволяющие шейдеру компенсировать любое смещение:


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



После определения приведенного выше буфера констант и вспомогательного метода шейдер может выполнить выборку данных изображения с помощью следующего:


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a>Запись данных образа

[Direct2D](./direct2d-portal.md) ожидает шейдер для определения выходного буфера для конечного изображения. В модели шейдера 4 (DirectX 10) это должен быть одномерный буфер из-за ограничений функций:


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



Текстура вывода индексируется по строкам, чтобы разрешить сохранение всего изображения.


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



С другой стороны, шейдер Shader Model 5 (DirectX 11) может использовать двухмерные выходные текстуры:


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



В шейдере Shader Model 5 [Direct2D](./direct2d-portal.md) предоставляет дополнительный параметр "аутпутоффсет" в буфере констант. Вывод шейдера должен быть оффсеттед следующим объемом:


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



Ниже показана завершенная пошаговая шейдер-передаваемая модель шейдеров 5. В нем каждый поток шейдера вычислений считывает и записывает один пиксель входного изображения.


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



В приведенном ниже коде показана эквивалентная версия шейдера модели шейдеров 4. Обратите внимание, что шейдер теперь преобразуется в одномерный выходной буфер.


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Пример пакета SDK для D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 