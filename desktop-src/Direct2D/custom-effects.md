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
# <a name="custom-effects"></a><span data-ttu-id="2f00c-103">Пользовательские эффекты</span><span class="sxs-lookup"><span data-stu-id="2f00c-103">Custom effects</span></span>

<span data-ttu-id="2f00c-104">[Direct2D](./direct2d-portal.md) поставляется с библиотекой эффектов, которые выполняют различные распространенные операции с образами.</span><span class="sxs-lookup"><span data-stu-id="2f00c-104">[Direct2D](./direct2d-portal.md) ships with a library of effects that perform a variety of common image operations.</span></span> <span data-ttu-id="2f00c-105">Полный список эффектов см. в разделе [встроенные эффекты](built-in-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-105">See the [built-in effects](built-in-effects.md) topic for the complete list of effects.</span></span> <span data-ttu-id="2f00c-106">Для функций, которые не могут быть реализованы с помощью встроенных эффектов, Direct2D позволяет создавать собственные пользовательские эффекты с использованием стандартных [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl).</span><span class="sxs-lookup"><span data-stu-id="2f00c-106">For functionality that cannot be achieved with the built-in effects, Direct2D allows you to write your own custom effects using standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl).</span></span> <span data-ttu-id="2f00c-107">Эти пользовательские эффекты можно использовать вместе со встроенными эффектами, поставляемыми с Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2f00c-107">You can use these custom effects alongside the built-in effects that ship with Direct2D.</span></span>

<span data-ttu-id="2f00c-108">Примеры результатов полного шейдера пикселей, вершины и вычислений см. в [примере D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="2f00c-108">To see examples of a complete pixel, vertex, and compute shader effect, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="2f00c-109">В этом разделе мы покажем вам шаги и понятия, необходимые для проектирования и создания полнофункционального пользовательского действия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-109">In this topic, we show you the steps and concepts you need to design and create a fully-featured custom effect.</span></span>

## <a name="introduction-what-is-inside-an-effect"></a><span data-ttu-id="2f00c-110">Введение. что находится в силе?</span><span class="sxs-lookup"><span data-stu-id="2f00c-110">Introduction: What is inside an effect?</span></span>

![Диаграмма эффектов тени.](images/custom-effects1.png)

<span data-ttu-id="2f00c-112">По сути, эффект [Direct2D](./direct2d-portal.md) выполняет задачу создания образов, например изменение яркости, снятие насыщенности изображения или, как показано выше, путем создания тени.</span><span class="sxs-lookup"><span data-stu-id="2f00c-112">Conceptually, a [Direct2D](./direct2d-portal.md) effect performs an imaging task, like changing brightness, de-saturating an image, or as shown above, creating a drop shadow.</span></span> <span data-ttu-id="2f00c-113">Для приложения они просты.</span><span class="sxs-lookup"><span data-stu-id="2f00c-113">To the app, they are simple.</span></span> <span data-ttu-id="2f00c-114">Они могут принимать ноль или более входных изображений, предоставлять несколько свойств, управляющих их работой, и создавать одно выходное изображение.</span><span class="sxs-lookup"><span data-stu-id="2f00c-114">They can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="2f00c-115">Существует четыре различные части пользовательского действия, за которые отвечает Автор:</span><span class="sxs-lookup"><span data-stu-id="2f00c-115">There are four different parts of a custom effect that an effect author is responsible for:</span></span>

1.  <span data-ttu-id="2f00c-116">Интерфейс Effect: интерфейс влияния концептуально определяет, как приложение взаимодействует с пользовательским действием (например, количество входов, принимаемых этим действием и доступные свойства).</span><span class="sxs-lookup"><span data-stu-id="2f00c-116">Effect Interface: The effect interface conceptually defines how an app interacts with a custom effect (like how many inputs the effect accepts and what properties are available).</span></span> <span data-ttu-id="2f00c-117">Интерфейс Effect управляет графом преобразования, который содержит фактические операции с образами.</span><span class="sxs-lookup"><span data-stu-id="2f00c-117">The effect interface manages a transform graph, which contains the actual imaging operations.</span></span>
2.  <span data-ttu-id="2f00c-118">Граф преобразования: каждый результат создает внутренний граф преобразования, состоящие из отдельных преобразований.</span><span class="sxs-lookup"><span data-stu-id="2f00c-118">Transform graph: Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="2f00c-119">Каждое преобразование представляет одну операцию с изображением.</span><span class="sxs-lookup"><span data-stu-id="2f00c-119">Each transform represents a single image operation.</span></span> <span data-ttu-id="2f00c-120">Этот результат отвечает за связывание этих преобразований в графе для выполнения предполагаемого применения образов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-120">The effect is responsible for linking these transforms together into a graph to perform the intended imaging effect.</span></span> <span data-ttu-id="2f00c-121">Результат может добавлять, удалять, изменять и переупорядочивать преобразования в ответ на изменения внешних свойств эффектов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-121">An effect can add, remove, modify, and reorder transforms in response to changes to the effect's external properties.</span></span>
3.  <span data-ttu-id="2f00c-122">Преобразование: Преобразование представляет одну операцию с изображением.</span><span class="sxs-lookup"><span data-stu-id="2f00c-122">Transform: A transform represents a single image operation.</span></span> <span data-ttu-id="2f00c-123">Его основное назначение заключается в размещении шейдеров, которые выполняются для каждого выходного пикселя.</span><span class="sxs-lookup"><span data-stu-id="2f00c-123">Its main purpose is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="2f00c-124">Для этого он отвечает за вычисление нового размера выходного изображения на основе логики в шейдерах.</span><span class="sxs-lookup"><span data-stu-id="2f00c-124">To that end, it is responsible for calculating the new size of its output image based on logic in its shaders.</span></span> <span data-ttu-id="2f00c-125">Кроме того, необходимо вычислить область входного изображения, из которой должны считываться шейдеры для отрисовки запрошенной выходной области.</span><span class="sxs-lookup"><span data-stu-id="2f00c-125">It also must calculate which area of its input image the shaders need to read from to render the requested output region.</span></span>
4.  <span data-ttu-id="2f00c-126">Шейдер. шейдер выполняется для входных данных преобразования на GPU (или ЦП, если программная отрисовка указывается, когда приложение создает устройство Direct3D).</span><span class="sxs-lookup"><span data-stu-id="2f00c-126">Shader: A shader is executed against the transform's input on the GPU (or CPU if software rendering is specified when the app creates the Direct3D device).</span></span> <span data-ttu-id="2f00c-127">Шейдеры эффектов записываются на языке штриховки высокого уровня ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) и компилируются в байтовый код во время компиляции, которая затем загружается с помощью этого действия во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-127">Effect shaders are written in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) and are compiled into byte code during the effect's compilation, which is then loaded by the effect during run-time.</span></span> <span data-ttu-id="2f00c-128">В этом справочном документе описано, как написать HLSL, совместимый с [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2f00c-128">This reference document describes how to write [Direct2D](./direct2d-portal.md)-compliant HLSL.</span></span> <span data-ttu-id="2f00c-129">В документации по Direct3D содержится базовый обзор HLSL.</span><span class="sxs-lookup"><span data-stu-id="2f00c-129">The Direct3D documentation contains a basic HLSL overview.</span></span>

## <a name="creating-an-effect-interface"></a><span data-ttu-id="2f00c-130">Создание интерфейса Effect</span><span class="sxs-lookup"><span data-stu-id="2f00c-130">Creating an effect interface</span></span>

<span data-ttu-id="2f00c-131">Интерфейс Effect определяет, как приложение взаимодействует с пользовательским действием.</span><span class="sxs-lookup"><span data-stu-id="2f00c-131">The effect interface defines how an app interacts with the custom effect.</span></span> <span data-ttu-id="2f00c-132">Чтобы создать интерфейс Effects, класс должен реализовывать ID2D1EffectImpl, определять метаданные, описывающие этот результат (например, его имя, число входов и свойства), а также создавать методы, которые регистрируют Пользовательский результат для использования с [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2f00c-132">To create an effect interface, a class must implement ID2D1EffectImpl, define metadata that describes the effect (such as its name, input count and properties), and create methods that register the custom effect for use with [Direct2D](./direct2d-portal.md).</span></span>

<span data-ttu-id="2f00c-133">После реализации всех компонентов интерфейса Effect заголовок Class будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2f00c-133">Once all of the components for an effect interface have been implemented, the class' header will appear like this:</span></span>


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



### <a name="implement-id2d1effectimpl"></a><span data-ttu-id="2f00c-134">Реализация ID2D1EffectImpl</span><span class="sxs-lookup"><span data-stu-id="2f00c-134">Implement ID2D1EffectImpl</span></span>

<span data-ttu-id="2f00c-135">Интерфейс [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) содержит три метода, которые необходимо реализовать:</span><span class="sxs-lookup"><span data-stu-id="2f00c-135">The [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) interface contains three methods that you must implement:</span></span>

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a><span data-ttu-id="2f00c-136">Инициализация (ID2D1EffectContext \* пконтекстинтернал, ID2D1TransformGraph \* птрансформграф)</span><span class="sxs-lookup"><span data-stu-id="2f00c-136">Initialize(ID2D1EffectContext \*pContextInternal, ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="2f00c-137">[Direct2D](./direct2d-portal.md) вызывает метод [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) после того, как приложение вызовет метод [**ID2D1DeviceContext:: креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-137">[Direct2D](./direct2d-portal.md) calls the [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method after the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method has been called by the app.</span></span> <span data-ttu-id="2f00c-138">Этот метод можно использовать для выполнения внутренней инициализации или любых других операций, необходимых для этого действия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-138">You can use this method to perform internal initialization or any other operations needed for the effect.</span></span> <span data-ttu-id="2f00c-139">Кроме того, его можно использовать для создания исходного графа преобразования эффектов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-139">Additionally, you can use it to create the effect's initial transform graph.</span></span>

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a><span data-ttu-id="2f00c-140">Сетграф (ID2D1TransformGraph \* птрансформграф)</span><span class="sxs-lookup"><span data-stu-id="2f00c-140">SetGraph(ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="2f00c-141">[Direct2D](./direct2d-portal.md) вызывает метод [**сетграф**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) , когда изменяется число входов для результата.</span><span class="sxs-lookup"><span data-stu-id="2f00c-141">[Direct2D](./direct2d-portal.md) calls the [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) method when the number of inputs to the effect is changed.</span></span> <span data-ttu-id="2f00c-142">Хотя большинство эффектов имеют постоянное число входов, другие, такие как [составной эффект](composite.md) , поддерживают переменное число входов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-142">While most effects have a constant number of inputs, others like the [Composite effect](composite.md) support a variable number of inputs.</span></span> <span data-ttu-id="2f00c-143">Этот метод позволяет этим эффектам обновить Граф преобразований в ответ на изменение счетчика входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f00c-143">This method allows these effects to update their transform graph in response to a changing input count.</span></span> <span data-ttu-id="2f00c-144">Если воздействие не поддерживает переменное число входов, этот метод может просто вернуть E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="2f00c-144">If an effect does not support a variable input count, this method can simply return E\_NOTIMPL.</span></span>

### <a name="prepareforrender-d2d1_change_type-changetype"></a><span data-ttu-id="2f00c-145">Препарефоррендер (D2D1 \_ изменение \_ типа изменения)</span><span class="sxs-lookup"><span data-stu-id="2f00c-145">PrepareForRender (D2D1\_CHANGE\_TYPE changeType)</span></span>

<span data-ttu-id="2f00c-146">Метод [**препарефоррендер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) предоставляет возможности для выполнения любых операций в ответ на внешние изменения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-146">The [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method provides an opportunity for effects to perform any operations in response to external changes.</span></span> <span data-ttu-id="2f00c-147">[Direct2D](./direct2d-portal.md) вызывает этот метод непосредственно перед отображением результата, если выполняется хотя бы одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="2f00c-147">[Direct2D](./direct2d-portal.md) calls this method just before it renders an effect if at least one of these is true:</span></span>

-   <span data-ttu-id="2f00c-148">Этот результат был ранее инициализирован, но еще не нарисован.</span><span class="sxs-lookup"><span data-stu-id="2f00c-148">The effect has been previously initialized but not yet drawn.</span></span>
-   <span data-ttu-id="2f00c-149">Свойство Effect изменилось с момента последнего вызова Draw.</span><span class="sxs-lookup"><span data-stu-id="2f00c-149">An effect property has changed since the last draw call.</span></span>
-   <span data-ttu-id="2f00c-150">Состояние вызывающего контекста [Direct2D](./direct2d-portal.md) (например, DPI) изменилось с момента последнего вызова Draw.</span><span class="sxs-lookup"><span data-stu-id="2f00c-150">The state of the calling [Direct2D](./direct2d-portal.md) context (like DPI) has changed since the last draw call.</span></span>

### <a name="implement-the-effect-registration-and-callback-methods"></a><span data-ttu-id="2f00c-151">Реализация методов регистрации эффектов и обратного вызова</span><span class="sxs-lookup"><span data-stu-id="2f00c-151">Implement the effect registration and callback methods</span></span>

<span data-ttu-id="2f00c-152">Приложения должны зарегистрировать эффекты с помощью [Direct2D](./direct2d-portal.md) , прежде чем создавать их экземпляры.</span><span class="sxs-lookup"><span data-stu-id="2f00c-152">Apps must register effects with [Direct2D](./direct2d-portal.md) before instantiating them.</span></span> <span data-ttu-id="2f00c-153">Эта регистрация ограничивается экземпляром фабрики Direct2D и должна повторяться каждый раз при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-153">This registration is scoped to an instance of a Direct2D factory, and must be repeated each time the app is run.</span></span> <span data-ttu-id="2f00c-154">Чтобы включить эту регистрацию, Пользовательский результат определяет уникальный идентификатор GUID, Открытый метод, который регистрирует этот результат, и закрытый метод обратного вызова, который возвращает экземпляр этого действия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-154">To enable this registration, a custom effect defines a unique GUID, a public method that registers the effect, and a private callback method that returns an instance of the effect.</span></span>

### <a name="define-a-guid"></a><span data-ttu-id="2f00c-155">Определение GUID</span><span class="sxs-lookup"><span data-stu-id="2f00c-155">Define a GUID</span></span>

<span data-ttu-id="2f00c-156">Необходимо определить идентификатор GUID, который однозначно определяет результат регистрации с помощью [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2f00c-156">You must define a GUID that uniquely identifies the effect for registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="2f00c-157">Приложение использует то же самое для обнаружения результата при вызове [**ID2D1DeviceContext:: креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span><span class="sxs-lookup"><span data-stu-id="2f00c-157">The app uses the same to identify the effect when it calls [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span></span>

<span data-ttu-id="2f00c-158">Этот код демонстрирует определение такого идентификатора GUID для воздействия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-158">This code demonstrates defining such a GUID for an effect.</span></span> <span data-ttu-id="2f00c-159">Необходимо создать собственный уникальный идентификатор GUID с помощью средства создания GUID, например guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="2f00c-159">You must create its own unique GUID using a GUID generation tool such as guidgen.exe.</span></span>


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a><span data-ttu-id="2f00c-160">Определение общедоступного метода регистрации</span><span class="sxs-lookup"><span data-stu-id="2f00c-160">Define a public registration method</span></span>

<span data-ttu-id="2f00c-161">Затем определите открытый метод для вызова приложения, чтобы зарегистрировать воздействие на [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2f00c-161">Next, define a public method for the app to call to register the effect with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="2f00c-162">Так как регистрация влияния зависит от экземпляра фабрики Direct2D, метод принимает интерфейс [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="2f00c-162">Because effect registration is specific to an instance of a Direct2D factory, the method accepts an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface as a parameter.</span></span> <span data-ttu-id="2f00c-163">Чтобы зарегистрировать этот результат, метод вызывает API [**ID2D1Factory1:: регистереффектфромстринг**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) в параметре **ID2D1Factory1** .</span><span class="sxs-lookup"><span data-stu-id="2f00c-163">To register the effect, the method then calls the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API on the **ID2D1Factory1** parameter.</span></span>

<span data-ttu-id="2f00c-164">Этот API принимает XML-строку, описывающую метаданные, входные данные и свойства этого действия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-164">This API accepts an XML string that describes the metadata, inputs, and properties of the effect.</span></span> <span data-ttu-id="2f00c-165">Метаданные для этого действия предназначены только для информационных целей и могут запрашиваться приложением через интерфейс [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-165">The metadata for an effect is for informational purposes only, and can be queried by the app through the [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) interface.</span></span> <span data-ttu-id="2f00c-166">Данные входных данных и свойств, с другой стороны, используются [Direct2D](./direct2d-portal.md) и представляют функциональность эффектов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-166">The input and property data, on the other hand, is used by [Direct2D](./direct2d-portal.md) and represents the effect's functionality.</span></span>

<span data-ttu-id="2f00c-167">Ниже показана XML-строка для минимального результата выборки.</span><span class="sxs-lookup"><span data-stu-id="2f00c-167">An XML string for a minimal sample effect is shown here.</span></span> <span data-ttu-id="2f00c-168">Добавление пользовательских свойств в XML рассматривается в разделе Добавление пользовательских свойств в раздел эффектов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-168">Adding custom properties to the XML is covered in the Adding custom properties to an effect section.</span></span>


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



### <a name="define-an-effect-factory-callback-method"></a><span data-ttu-id="2f00c-169">Определение метода обратного вызова фабрики эффектов</span><span class="sxs-lookup"><span data-stu-id="2f00c-169">Define an effect factory callback method</span></span>

<span data-ttu-id="2f00c-170">Этот результат также должен предоставлять закрытый метод обратного вызова, который возвращает экземпляр действия с помощью одного параметра IUnknown \* \* .</span><span class="sxs-lookup"><span data-stu-id="2f00c-170">The effect must also provide a private callback method that returns an instance of the effect through a single IUnknown\*\* parameter.</span></span> <span data-ttu-id="2f00c-171">Указатель на этот метод предоставляется для [Direct2D](./direct2d-portal.md) , когда результат регистрируется через API [**ID2D1Factory1:: регистереффектфромстринг**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) через параметр [**\_ \_ фабрики PD2D1 Effect**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .</span><span class="sxs-lookup"><span data-stu-id="2f00c-171">A pointer to this method is provided to [Direct2D](./direct2d-portal.md) when the effect is registered via the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API through the [**PD2D1\_EFFECT\_FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)\\ parameter.</span></span>


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



### <a name="implement-the-iunknown-interface"></a><span data-ttu-id="2f00c-172">Реализация интерфейса IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f00c-172">Implement the IUnknown interface</span></span>

<span data-ttu-id="2f00c-173">Наконец, в результате должен быть реализован интерфейс IUnknown для совместимости с COM.</span><span class="sxs-lookup"><span data-stu-id="2f00c-173">Finally, the effect must implement the IUnknown interface for compatibility with COM.</span></span>

## <a name="creating-the-effects-transform-graph"></a><span data-ttu-id="2f00c-174">Создание графа преобразования эффектов</span><span class="sxs-lookup"><span data-stu-id="2f00c-174">Creating the effect's transform graph</span></span>

<span data-ttu-id="2f00c-175">В результате может использоваться несколько различных преобразований (отдельных операций с изображениями), чтобы создать требуемый результат создания образа.</span><span class="sxs-lookup"><span data-stu-id="2f00c-175">An effect can use several different transforms (individual image operations) to create its desired imaging effect.</span></span> <span data-ttu-id="2f00c-176">Для управления порядком, в котором эти преобразования применяются к изображению ввода, он упорядочивает их в графе преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-176">To control the order in which these transforms are applied to the input image, the effect arranges them into a transform graph.</span></span> <span data-ttu-id="2f00c-177">Граф преобразования может использовать эффекты и преобразования, входящие в [Direct2D](./direct2d-portal.md) , а также пользовательские преобразования, созданные автором эффекта.</span><span class="sxs-lookup"><span data-stu-id="2f00c-177">A transform graph can make use of the effects and transforms included in [Direct2D](./direct2d-portal.md) as well as custom transforms created by the effect author.</span></span>

### <a name="using-transforms-included-with-direct2d"></a><span data-ttu-id="2f00c-178">Использование преобразований, входящих в состав Direct2D</span><span class="sxs-lookup"><span data-stu-id="2f00c-178">Using transforms included with Direct2D</span></span>

<span data-ttu-id="2f00c-179">Это наиболее часто используемые преобразования, предоставляемые с [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2f00c-179">These are the most commonly used transforms provided with [Direct2D](./direct2d-portal.md).</span></span>

-   <span data-ttu-id="2f00c-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform). это преобразование смешивает произвольное число входов вместе с описанием смешения, см. раздел [**\_ \_ Описание D2D1 Blend**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) и [Пример составных эффектов Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) для примеров смешения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): This transform blends an arbitrary number of inputs together based on a blend description, see the [**D2D1\_BLEND\_DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) topic and the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) for blending examples.</span></span> <span data-ttu-id="2f00c-181">Это преобразование возвращается методом [**ID2D1EffectContext:: креатеблендтрансформ**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-181">This transform is returned by the [**ID2D1EffectContext::CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) method.</span></span>
-   <span data-ttu-id="2f00c-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): это преобразование расширяет размер вывода изображения в соответствии с заданным [**\_ \_ режимом расширения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): This transform expands an image's output size according to the [**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specified.</span></span> <span data-ttu-id="2f00c-183">Это преобразование возвращается методом [**ID2D1EffectContext:: креатебордертрансформ**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-183">This transform is returned by the [**ID2D1EffectContext::CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) method.</span></span>
-   <span data-ttu-id="2f00c-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): это преобразование смещает (преобразует) свои входные данные на любое целое число пикселей.</span><span class="sxs-lookup"><span data-stu-id="2f00c-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): This transform offsets (translates) its input by any whole number of pixels.</span></span> <span data-ttu-id="2f00c-185">Это преобразование возвращается методом [**ID2D1EffectContext:: креатеоффсеттрансформ**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-185">This transform is returned by the [**ID2D1EffectContext::CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) method.</span></span>
-   <span data-ttu-id="2f00c-186">Любой существующий результат может рассматриваться как преобразование в целях создания графа преобразования с помощью метода [**ID2D1EffectContext:: креатетрансформнодефромеффект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-186">Any existing effect can be treated as a transform for the purposes of transform graph creation by using the [**ID2D1EffectContext::CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) method.</span></span>

### <a name="creating-a-single-node-transform-graph"></a><span data-ttu-id="2f00c-187">Создание графа преобразования с одним узлом</span><span class="sxs-lookup"><span data-stu-id="2f00c-187">Creating a single-node transform graph</span></span>

<span data-ttu-id="2f00c-188">После создания преобразования входные данные этого действия должны быть подключены к входным данным преобразования, а выходные данные преобразования должны быть подключены к выходным данным этого результата.</span><span class="sxs-lookup"><span data-stu-id="2f00c-188">Once you create a transform, the effect's input needs to be connected to the transform's input, and the transform's output needs to be connected to the effect's output.</span></span> <span data-ttu-id="2f00c-189">Если результат содержит только одно преобразование, для этого можно использовать метод [**ID2D1TransformGraph:: сетсинглетрансформноде**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-189">When an effect only contains a single transform, you can use the [**ID2D1TransformGraph::SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) method to easily accomplish this.</span></span>

<span data-ttu-id="2f00c-190">Можно создать или изменить преобразование в методах [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) или [**сетграф**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) действия с помощью предоставленного параметра ID2D1TransformGraph.</span><span class="sxs-lookup"><span data-stu-id="2f00c-190">You can create or modify a transform in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) or [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) methods using the provided ID2D1TransformGraph parameter.</span></span> <span data-ttu-id="2f00c-191">Если в результате изменения графа преобразования в другом методе, где этот параметр недоступен, результат может быть [**сохранен в качестве**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) переменной-члена класса и обращаться к нему в другом месте, например [**препарефоррендер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) или метод обратного вызова настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="2f00c-191">If an effect needs to make changes to the transform graph in another method where this parameter is not available, the effect can save the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter as a member variable of the class and access it elsewhere, such as [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) or a custom property callback method.</span></span>

<span data-ttu-id="2f00c-192">Пример метода [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) показан здесь.</span><span class="sxs-lookup"><span data-stu-id="2f00c-192">A sample [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method is shown here.</span></span> <span data-ttu-id="2f00c-193">Этот метод создает граф преобразования с одним узлом, который смещает изображение на 100 пикселей на каждой оси.</span><span class="sxs-lookup"><span data-stu-id="2f00c-193">This method creates a single-node transform graph that offsets the image by one hundred pixels in each axis.</span></span>


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



### <a name="creating-a-multi-node-transform-graph"></a><span data-ttu-id="2f00c-194">Создание графа преобразования с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="2f00c-194">Creating a multi-node transform graph</span></span>

<span data-ttu-id="2f00c-195">Добавление нескольких преобразований к графу преобразования эффекта позволяет внутренним образом выполнять несколько операций с изображениями, представляемых приложению в виде единого единого эффекта.</span><span class="sxs-lookup"><span data-stu-id="2f00c-195">Adding multiple transforms to an effect's transform graph allows effects to internally perform multiple image operations that are presented to an app as a single unified effect.</span></span>

<span data-ttu-id="2f00c-196">Как отмечалось выше, граф преобразования результата можно изменить в любом методе Effect, используя параметр [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) , полученный в методе [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) этого действия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-196">As noted above, the effect's transform graph may be edited in any effect method using the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter received in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method.</span></span> <span data-ttu-id="2f00c-197">Для создания или изменения графа преобразования эффектов можно использовать следующие API-интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="2f00c-197">The following APIs on that interface can be used to create or modify an effect's transform graph:</span></span>

### <a name="addnodeid2d1transformnode-pnode"></a><span data-ttu-id="2f00c-198">AddNode (ID2D1TransformNode \* пноде)</span><span class="sxs-lookup"><span data-stu-id="2f00c-198">AddNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="2f00c-199">Метод [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , фактически, регистрирует преобразование с результатом и должен вызываться перед тем, как преобразование можно будет использовать с любыми другими методами графа преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-199">The [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) method, in effect, 'registers' the transform with the effect, and must be called before the transform can be used with any of the other transform graph methods.</span></span>

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a><span data-ttu-id="2f00c-200">Коннекттоеффектинпут (UINT32 Тоеффектинпутиндекс, ID2D1TransformNode \* пноде, UINT32 тонодеинпутиндекс)</span><span class="sxs-lookup"><span data-stu-id="2f00c-200">ConnectToEffectInput(UINT32 toEffectInputIndex, ID2D1TransformNode \*pNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="2f00c-201">Метод [**коннекттоеффектинпут**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) соединяет входные данные изображения эффектов с входными данными преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-201">The [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) method connects the effect's image input to a transform's input.</span></span> <span data-ttu-id="2f00c-202">Один и тот же ввод результата может быть подключен к нескольким преобразованиям.</span><span class="sxs-lookup"><span data-stu-id="2f00c-202">The same effect input can be connected to multiple transforms.</span></span>

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a><span data-ttu-id="2f00c-203">Коннектноде (ID2D1TransformNode \* пфромноде, ID2D1TransformNode \* ПТОНОДЕ, UINT32 тонодеинпутиндекс)</span><span class="sxs-lookup"><span data-stu-id="2f00c-203">ConnectNode(ID2D1TransformNode \*pFromNode, ID2D1TransformNode \*pToNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="2f00c-204">Метод [**коннектноде**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) подключает выходные данные преобразования к входу другого преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-204">The [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) method connects a transform's output to another transform's input.</span></span> <span data-ttu-id="2f00c-205">Выход преобразования может быть подключен к нескольким преобразованиям.</span><span class="sxs-lookup"><span data-stu-id="2f00c-205">A transform output can be connected to multiple transforms.</span></span>

### <a name="setoutputnodeid2d1transformnode-pnode"></a><span data-ttu-id="2f00c-206">Сетаутпутноде (ID2D1TransformNode \* пноде)</span><span class="sxs-lookup"><span data-stu-id="2f00c-206">SetOutputNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="2f00c-207">Метод [**сетаутпутноде**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) соединяет выходные данные преобразования с выходными данными результата.</span><span class="sxs-lookup"><span data-stu-id="2f00c-207">The [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) method connects a transform's output to the effect's output.</span></span> <span data-ttu-id="2f00c-208">Поскольку результат имеет только один выход, в качестве выходного узла можно назначить только одно преобразование.</span><span class="sxs-lookup"><span data-stu-id="2f00c-208">Because an effect only has one output, only a single transform can be designated as the 'output node'.</span></span>

<span data-ttu-id="2f00c-209">Этот код использует два отдельных преобразования для создания единого воздействия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-209">This code uses two separate transforms to create a unified effect.</span></span> <span data-ttu-id="2f00c-210">В этом случае эффектом является переведенная тень.</span><span class="sxs-lookup"><span data-stu-id="2f00c-210">In this case, the effect is a translated drop shadow.</span></span>


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



## <a name="adding-custom-properties-to-an-effect"></a><span data-ttu-id="2f00c-211">Добавление пользовательских свойств к результату</span><span class="sxs-lookup"><span data-stu-id="2f00c-211">Adding custom properties to an effect</span></span>

<span data-ttu-id="2f00c-212">Эффекты могут определять пользовательские свойства, позволяющие приложению изменять поведение эффекта во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-212">Effects can define custom properties that allow an app to change the effect's behavior during runtime.</span></span> <span data-ttu-id="2f00c-213">Определение свойства для пользовательского действия состоит из трех этапов:</span><span class="sxs-lookup"><span data-stu-id="2f00c-213">There are three steps to define a property for a custom effect:</span></span>

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a><span data-ttu-id="2f00c-214">Добавление метаданных свойства в данные регистрации действия</span><span class="sxs-lookup"><span data-stu-id="2f00c-214">Add the property metadata to the effect's registration data</span></span>

### <a name="add-property-to-registration-xml"></a><span data-ttu-id="2f00c-215">Добавление свойства в XML-файл регистрации</span><span class="sxs-lookup"><span data-stu-id="2f00c-215">Add property to registration XML</span></span>

<span data-ttu-id="2f00c-216">Необходимо определить свойства пользовательского действия во время начальной регистрации этого действия с помощью [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2f00c-216">You must define a custom effect's properties during the effect's initial registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="2f00c-217">Сначала необходимо обновить XML-код регистрации результата в общедоступном методе регистрации с помощью нового свойства:</span><span class="sxs-lookup"><span data-stu-id="2f00c-217">First, you must update the effect's registration XML in its public registration method with the new property:</span></span>


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



<span data-ttu-id="2f00c-218">При определении свойства Effect в XML требуется имя, тип и отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="2f00c-218">When you define an effect property in XML, it needs a name, a type, and a display name.</span></span> <span data-ttu-id="2f00c-219">Отображаемое имя свойства, а также значения категории, автора и описания общего результата могут быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="2f00c-219">A property's display name, as well as the overall effect's category, author, and description values can and should be localized.</span></span>

<span data-ttu-id="2f00c-220">Для каждого свойства в результате можно дополнительно указать значения по умолчанию, min и Max.</span><span class="sxs-lookup"><span data-stu-id="2f00c-220">For each property, an effect can optionally specify default, min, and max values.</span></span> <span data-ttu-id="2f00c-221">Эти значения предназначены только для использования в информационных целях.</span><span class="sxs-lookup"><span data-stu-id="2f00c-221">These values are for informational use only.</span></span> <span data-ttu-id="2f00c-222">Они не применяются функцией [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2f00c-222">They are not enforced by [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="2f00c-223">Вы самостоятельно реализуете любую логику по умолчанию/min/max в классе Effect.</span><span class="sxs-lookup"><span data-stu-id="2f00c-223">It is up to you to implement any specified default/min/max logic in the effect class yourself.</span></span>

<span data-ttu-id="2f00c-224">Значение типа, указанное в XML-коде для свойства, должно соответствовать соответствующему типу данных, используемому методами getter и Setter свойства.</span><span class="sxs-lookup"><span data-stu-id="2f00c-224">The type value listed in the XML for the property must match the corresponding data type used by the property's getter and setter methods.</span></span> <span data-ttu-id="2f00c-225">В этой таблице показаны соответствующие значения XML для каждого типа данных:</span><span class="sxs-lookup"><span data-stu-id="2f00c-225">Corresponding XML values for each data type are shown in this table:</span></span>



| <span data-ttu-id="2f00c-226">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2f00c-226">Data type</span></span>                                                                                                                              | <span data-ttu-id="2f00c-227">Соответствующее значение XML</span><span class="sxs-lookup"><span data-stu-id="2f00c-227">Corresponding XML value</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="2f00c-228">пвстр</span><span class="sxs-lookup"><span data-stu-id="2f00c-228">PWSTR</span></span>                                                                                                                                  | <span data-ttu-id="2f00c-229">строка</span><span class="sxs-lookup"><span data-stu-id="2f00c-229">string</span></span>                  |
| <span data-ttu-id="2f00c-230">BOOL</span><span class="sxs-lookup"><span data-stu-id="2f00c-230">BOOL</span></span>                                                                                                                                   | <span data-ttu-id="2f00c-231">bool</span><span class="sxs-lookup"><span data-stu-id="2f00c-231">bool</span></span>                    |
| <span data-ttu-id="2f00c-232">UINT</span><span class="sxs-lookup"><span data-stu-id="2f00c-232">UINT</span></span>                                                                                                                                   | <span data-ttu-id="2f00c-233">uint32</span><span class="sxs-lookup"><span data-stu-id="2f00c-233">uint32</span></span>                  |
| <span data-ttu-id="2f00c-234">INT</span><span class="sxs-lookup"><span data-stu-id="2f00c-234">INT</span></span>                                                                                                                                    | <span data-ttu-id="2f00c-235">int32</span><span class="sxs-lookup"><span data-stu-id="2f00c-235">int32</span></span>                   |
| <span data-ttu-id="2f00c-236">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2f00c-236">FLOAT</span></span>                                                                                                                                  | <span data-ttu-id="2f00c-237">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2f00c-237">float</span></span>                   |
| [<span data-ttu-id="2f00c-238">**\_Экземпляр D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="2f00c-238">**D2D\_VECTOR\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | <span data-ttu-id="2f00c-239">Vector2</span><span class="sxs-lookup"><span data-stu-id="2f00c-239">vector2</span></span>                 |
| [<span data-ttu-id="2f00c-240">**\_3F вектора D2D \_**</span><span class="sxs-lookup"><span data-stu-id="2f00c-240">**D2D\_VECTOR\_3F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | <span data-ttu-id="2f00c-241">Vector3</span><span class="sxs-lookup"><span data-stu-id="2f00c-241">vector3</span></span>                 |
| [<span data-ttu-id="2f00c-242">**\_4F вектора D2D \_**</span><span class="sxs-lookup"><span data-stu-id="2f00c-242">**D2D\_VECTOR\_4F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | <span data-ttu-id="2f00c-243">Vector4</span><span class="sxs-lookup"><span data-stu-id="2f00c-243">vector4</span></span>                 |
| <span data-ttu-id="2f00c-244">[**\_Матрица D2D \_ 3X2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span><span class="sxs-lookup"><span data-stu-id="2f00c-244">[**D2D\_MATRIX\_3X2\_F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span></span> | <span data-ttu-id="2f00c-245">matrix3x2</span><span class="sxs-lookup"><span data-stu-id="2f00c-245">matrix3x2</span></span>               |
| [<span data-ttu-id="2f00c-246">**\_Матрица D2D \_ 4X3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="2f00c-246">**D2D\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | <span data-ttu-id="2f00c-247">matrix4x3</span><span class="sxs-lookup"><span data-stu-id="2f00c-247">matrix4x3</span></span>               |
| [<span data-ttu-id="2f00c-248">**\_Матрица D2D \_ 4x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="2f00c-248">**D2D\_MATRIX\_4X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | <span data-ttu-id="2f00c-249">matrix4x4</span><span class="sxs-lookup"><span data-stu-id="2f00c-249">matrix4x4</span></span>               |
| [<span data-ttu-id="2f00c-250">**\_Матрица D2D \_ 5x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="2f00c-250">**D2D\_MATRIX\_5X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | <span data-ttu-id="2f00c-251">matrix5x4</span><span class="sxs-lookup"><span data-stu-id="2f00c-251">matrix5x4</span></span>               |
| <span data-ttu-id="2f00c-252">ДВУХБАЙТОВЫХ\[\]</span><span class="sxs-lookup"><span data-stu-id="2f00c-252">BYTE\[\]</span></span>                                                                                                                               | <span data-ttu-id="2f00c-253">большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="2f00c-253">blob</span></span>                    |
| <span data-ttu-id="2f00c-254">IUnknown\*</span><span class="sxs-lookup"><span data-stu-id="2f00c-254">IUnknown\*</span></span>                                                                                                                             | <span data-ttu-id="2f00c-255">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f00c-255">iunknown</span></span>                |
| <span data-ttu-id="2f00c-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span><span class="sxs-lookup"><span data-stu-id="2f00c-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span></span>                                                                                       | <span data-ttu-id="2f00c-257">колорконтекст</span><span class="sxs-lookup"><span data-stu-id="2f00c-257">colorcontext</span></span>            |
| <span data-ttu-id="2f00c-258">CLSID</span><span class="sxs-lookup"><span data-stu-id="2f00c-258">CLSID</span></span>                                                                                                                                  | <span data-ttu-id="2f00c-259">clsid</span><span class="sxs-lookup"><span data-stu-id="2f00c-259">clsid</span></span>                   |
| <span data-ttu-id="2f00c-260">Перечисление ([**\_ \_ Режим интерполяции D2D1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode)и т. д.)</span><span class="sxs-lookup"><span data-stu-id="2f00c-260">Enumeration ([**D2D1\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span></span>                                                | <span data-ttu-id="2f00c-261">enum</span><span class="sxs-lookup"><span data-stu-id="2f00c-261">enum</span></span>                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a><span data-ttu-id="2f00c-262">Сопоставьте новое свойство с методами getter и Set</span><span class="sxs-lookup"><span data-stu-id="2f00c-262">Map the new property to getter and setter methods</span></span>

<span data-ttu-id="2f00c-263">Далее результат должен сопоставлять это новое свойство с методами getter и Set.</span><span class="sxs-lookup"><span data-stu-id="2f00c-263">Next, the effect must map this new property to getter and setter methods.</span></span> <span data-ttu-id="2f00c-264">Это делается через массив [**\_ \_ привязки свойств D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) , который передается в метод [**ID2D1Factory1:: регистереффектфромстринг**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-264">This is done through the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array that is passed into the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method.</span></span>

<span data-ttu-id="2f00c-265">Массив [**\_ \_ привязки свойств D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2f00c-265">The [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array looks like this:</span></span>


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



<span data-ttu-id="2f00c-266">После создания массива XML и привязок передайте их в метод [**регистереффектфромстринг**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :</span><span class="sxs-lookup"><span data-stu-id="2f00c-266">Once you create the XML and bindings array, pass them into the [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method:</span></span>


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



<span data-ttu-id="2f00c-267">\_ \_ \_ Для макроса привязки типа значения D2D1 требуется, чтобы класс Effect наследовал от [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) перед любым другим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="2f00c-267">The D2D1\_VALUE\_TYPE\_BINDING macro requires the effect class to inherit from [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) before any other interface.</span></span>

<span data-ttu-id="2f00c-268">Пользовательские свойства для воздействия индексируются в том порядке, в котором они объявляются в XML, а после создания могут быть доступны в приложении с помощью методов [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) и [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-268">Custom properties for an effect are indexed in the order they are declared in the XML, and once created can be accessed by the app using the [**ID2D1Properties::SetValue**](id2d1properties-setvalue-overload.md) and [**ID2D1Properties::GetValue**](id2d1properties-getvalue-overload.md) methods.</span></span> <span data-ttu-id="2f00c-269">Для удобства можно создать общедоступное перечисление, в котором перечислены все свойства в файле заголовка результата.</span><span class="sxs-lookup"><span data-stu-id="2f00c-269">For convenience, you can create a public enumeration that lists each property in the effect's header file:</span></span>


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a><span data-ttu-id="2f00c-270">Создание методов getter и Setter для свойства</span><span class="sxs-lookup"><span data-stu-id="2f00c-270">Create the getter and setter methods for the property</span></span>

<span data-ttu-id="2f00c-271">Следующим шагом является создание методов getter и Setter для нового свойства.</span><span class="sxs-lookup"><span data-stu-id="2f00c-271">The next step is to create the getter and setter methods for the new property.</span></span> <span data-ttu-id="2f00c-272">Имена методов должны совпадать с именами, указанными в массиве [**\_ \_ привязки свойства D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-272">The names of the methods must match the ones specified in the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array.</span></span> <span data-ttu-id="2f00c-273">Кроме того, тип свойства, указанный в XML-коде действия, должен соответствовать типу параметра метода задания и возвращаемому значению метода Getter.</span><span class="sxs-lookup"><span data-stu-id="2f00c-273">In addition, the property type specified in the effect's XML must match the type of the setter method's parameter and the getter method's return value.</span></span>


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



### <a name="update-effects-transforms-in-response-to-property-change"></a><span data-ttu-id="2f00c-274">Преобразование эффектов обновления в ответ на изменение свойства</span><span class="sxs-lookup"><span data-stu-id="2f00c-274">Update effect's transforms in response to property change</span></span>

<span data-ttu-id="2f00c-275">Чтобы фактически обновить вывод изображения в ответ на изменение свойства, результат должен изменить его базовые преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-275">To actually update an effect's image output in response to a property change, the effect needs to change its underlying transforms.</span></span> <span data-ttu-id="2f00c-276">Обычно это делается в методе [**препарефоррендер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) в результате, который [Direct2D](./direct2d-portal.md) автоматически вызывает, когда одно из свойств эффектов изменилось.</span><span class="sxs-lookup"><span data-stu-id="2f00c-276">This is typically done in the effect's [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method which [Direct2D](./direct2d-portal.md) automatically calls when one of an effect's properties has been changed.</span></span> <span data-ttu-id="2f00c-277">Однако преобразования могут быть обновлены в любом из методов, таких как инициализация или методы задания свойств эффектов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-277">However, transforms can be updated in any of the effect's methods: such as Initialize or the effect's property setter methods.</span></span>

<span data-ttu-id="2f00c-278">Например, если в результате содержался [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) и требовалось изменить значение смещения в ответ на изменение свойства Offset этого действия, в [**препарефоррендер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender)будет добавлен следующий код:</span><span class="sxs-lookup"><span data-stu-id="2f00c-278">For example, if an effect contained an [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) and wanted to modify its offset value in response to the effect's Offset property being changed, it would add the following code in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span></span>


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



## <a name="creating-a-custom-transform"></a><span data-ttu-id="2f00c-279">Создание пользовательского преобразования</span><span class="sxs-lookup"><span data-stu-id="2f00c-279">Creating a custom transform</span></span>

<span data-ttu-id="2f00c-280">Чтобы реализовать операции с изображениями, помимо предоставляемых в [Direct2D](./direct2d-portal.md), необходимо реализовать пользовательские преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-280">To implement image operations beyond what is provided in [Direct2D](./direct2d-portal.md), you must implement custom transforms.</span></span> <span data-ttu-id="2f00c-281">Пользовательские преобразования могут произвольно изменить входной образ с помощью настраиваемых шейдеров HLSL.</span><span class="sxs-lookup"><span data-stu-id="2f00c-281">Custom transforms can arbitrarily change an input image through the use of custom HLSL shaders.</span></span>

<span data-ttu-id="2f00c-282">Преобразования реализуют один из двух различных интерфейсов в зависимости от используемых типов шейдеров.</span><span class="sxs-lookup"><span data-stu-id="2f00c-282">Transforms implement one of two different interfaces depending on the types of shaders they use.</span></span> <span data-ttu-id="2f00c-283">Преобразования с помощью пиксельных и/или шейдеров вершин должны реализовывать [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), а преобразования с использованием шейдеров вычислений должны реализовывать [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span><span class="sxs-lookup"><span data-stu-id="2f00c-283">Transforms using pixel and/or vertex shaders must implement [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), while transforms using compute shaders must implement [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span></span> <span data-ttu-id="2f00c-284">Эти интерфейсы наследуют от [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="2f00c-284">These interfaces both inherit from [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span> <span data-ttu-id="2f00c-285">В этом разделе основное внимание уделяется реализации функций, общих для обоих.</span><span class="sxs-lookup"><span data-stu-id="2f00c-285">This section focuses on implementing the functionality that is common to both.</span></span>

<span data-ttu-id="2f00c-286">Интерфейс [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) имеет четыре метода для реализации:</span><span class="sxs-lookup"><span data-stu-id="2f00c-286">The [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface has four methods to implement:</span></span>

### <a name="getinputcount"></a><span data-ttu-id="2f00c-287">GetInputCount</span><span class="sxs-lookup"><span data-stu-id="2f00c-287">GetInputCount</span></span>

<span data-ttu-id="2f00c-288">Этот метод возвращает целое число, представляющее число входных данных для преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-288">This method returns an integer representing the input count for the transform.</span></span>


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a><span data-ttu-id="2f00c-289">мапинпутректстуутпутрект</span><span class="sxs-lookup"><span data-stu-id="2f00c-289">MapInputRectsToOutputRect</span></span>

<span data-ttu-id="2f00c-290">[Direct2D](./direct2d-portal.md) вызывает метод [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) каждый раз при отрисовке преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-290">[Direct2D](./direct2d-portal.md) calls the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) method each time the transform is rendered.</span></span> <span data-ttu-id="2f00c-291">Direct2D передает прямоугольник, представляющий границы каждого из входных данных для преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-291">Direct2D passes a rectangle representing the bounds of each of the inputs to the transform.</span></span> <span data-ttu-id="2f00c-292">Затем преобразование отвечает за вычисление границ выходного изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-292">The transform is then responsible for calculating the bounds of the output image.</span></span> <span data-ttu-id="2f00c-293">Размер прямоугольников для всех методов на этом интерфейсе ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) определяется в пикселях, а не DIP.</span><span class="sxs-lookup"><span data-stu-id="2f00c-293">The size of the rectangles for all the methods on this interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) are defined in pixels, not DIPs.</span></span>

<span data-ttu-id="2f00c-294">Этот метод также отвечает за вычисление области выходных данных, которые являются непрозрачными в зависимости от логики его шейдера и непрозрачных регионов каждого входного параметра.</span><span class="sxs-lookup"><span data-stu-id="2f00c-294">This method is also responsible for calculating the region of the output that is opaque based on the logic of its shader and the opaque regions of each input.</span></span> <span data-ttu-id="2f00c-295">Непрозрачная область изображения определяется так, чтобы альфа-канал был "1" для всего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2f00c-295">An opaque region of an image is defined as that where the alpha channel is '1' for the entirety of the rectangle.</span></span> <span data-ttu-id="2f00c-296">Если неясно, является ли выход преобразования непрозрачным, то непрозрачный для вывода прямоугольник должен иметь значение (0, 0, 0, 0) в качестве безопасного значения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-296">If it is unclear whether a transform's output is opaque, the output opaque rectangle should be set to (0, 0, 0, 0) as a safe value.</span></span> <span data-ttu-id="2f00c-297">[Direct2D](./direct2d-portal.md) использует эти сведения для оптимизации подготовки к просмотру с гарантированно непрозрачным содержимым.</span><span class="sxs-lookup"><span data-stu-id="2f00c-297">[Direct2D](./direct2d-portal.md) uses this info to perform rendering optimizations with 'guaranteed opaque' content.</span></span> <span data-ttu-id="2f00c-298">Если это значение неверное, это может привести к неправильной отрисовке.</span><span class="sxs-lookup"><span data-stu-id="2f00c-298">If this value is inaccurate, it can result in incorrect rendering.</span></span>

<span data-ttu-id="2f00c-299">Во время выполнения этого метода можно изменить поведение при отрисовке преобразования (как определено в разделах с 6 по 8).</span><span class="sxs-lookup"><span data-stu-id="2f00c-299">The you can modify the transform's rendering behavior (as defined in sections 6 through 8) during this method.</span></span> <span data-ttu-id="2f00c-300">Однако вы не можете изменить другие преобразования в графе преобразования или схему диаграммы здесь.</span><span class="sxs-lookup"><span data-stu-id="2f00c-300">However, the you can't modify other transforms in the transform graph, or the graph layout itself here.</span></span>


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



<span data-ttu-id="2f00c-301">Для более сложного примера рассмотрим, как будет представлено простое размытие:</span><span class="sxs-lookup"><span data-stu-id="2f00c-301">For a more complex example, consider how a simple blur operation would be represented:</span></span>

<span data-ttu-id="2f00c-302">Если в операции размытия используется радиус 5 пикселей, размер прямоугольника вывода должен расширяться на 5 пикселей, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="2f00c-302">If a blur operation uses a 5 pixel radius, the size of the output rectangle must expand by 5 pixels, as shown below.</span></span> <span data-ttu-id="2f00c-303">При изменении координат прямоугольника преобразование должно гарантировать, что его логика не приведет к превышению или потере точности в координатах прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2f00c-303">When modifying rectangle coordinates, a transform must ensure that its logic does not cause any over/underflows in the rectangle coordinates.</span></span>


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



<span data-ttu-id="2f00c-304">Поскольку изображение размыто, область изображения, которая была непрозрачной, теперь может быть частично прозрачной.</span><span class="sxs-lookup"><span data-stu-id="2f00c-304">Because the image is blurred, a region of the image which was opaque may now be partially transparent.</span></span> <span data-ttu-id="2f00c-305">Это связано с тем, что область за пределами изображения по умолчанию имеет прозрачный черный цвет, и эта прозрачность будет смешиваться с краями вокруг краев изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-305">This is because the area outside the image defaults to transparent black and this transparency will be blended into the image around the edges.</span></span> <span data-ttu-id="2f00c-306">Преобразование должно отражать это в выводимых вычислениях непрозрачных прямоугольников:</span><span class="sxs-lookup"><span data-stu-id="2f00c-306">The transform must reflect this in its output opaque rectangle calculations:</span></span>


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



<span data-ttu-id="2f00c-307">Эти вычисления отображаются здесь:</span><span class="sxs-lookup"><span data-stu-id="2f00c-307">These calculations are visualized here:</span></span>

![Иллюстрация вычисления прямоугольника.](images/custom-effects2.png)

<span data-ttu-id="2f00c-309">Дополнительные сведения об этом методе см. на странице справочника по [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-309">For more info about this method, see the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) reference page.</span></span>

### <a name="mapoutputrecttoinputrects"></a><span data-ttu-id="2f00c-310">мапаутпутректтоинпутректс</span><span class="sxs-lookup"><span data-stu-id="2f00c-310">MapOutputRectToInputRects</span></span>

<span data-ttu-id="2f00c-311">[Direct2D](./direct2d-portal.md) вызывает метод [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) после [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="2f00c-311">[Direct2D](./direct2d-portal.md) calls the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) method after [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="2f00c-312">Преобразование должно вычислить часть изображения, из которой он должен быть считан, чтобы правильно отобразить запрошенную выходную область.</span><span class="sxs-lookup"><span data-stu-id="2f00c-312">The transform must calculate what portion of the image it needs to read from in order to correctly render the requested output region.</span></span>

<span data-ttu-id="2f00c-313">Как и ранее, если результат строго сопоставляет пикселы 1-1, он может передать прямоугольник вывода через прямоугольник ввода:</span><span class="sxs-lookup"><span data-stu-id="2f00c-313">As before, if an effect strictly maps pixels 1-1, it can pass the output rectangle through to the input rectangle:</span></span>


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



<span data-ttu-id="2f00c-314">Аналогично, если преобразование сжимает или развертывает изображение (например, пример размытия), Пиксели часто используют окружающие Пиксели для вычисления их значения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-314">Likewise, if a transform shrinks or expands an image (like the blur example here), pixels often use surrounding pixels to calculate their value.</span></span> <span data-ttu-id="2f00c-315">При размытии пиксел вычисляется с учетом окружающих его пикселов, даже если они выходят за границы входного изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-315">With a blur, a pixel is averaged with its surrounding pixels, even if they are outside of the bounds of the input image.</span></span> <span data-ttu-id="2f00c-316">Это поведение отражается в вычислении.</span><span class="sxs-lookup"><span data-stu-id="2f00c-316">This behavior is reflected in the calculation.</span></span> <span data-ttu-id="2f00c-317">Как и ранее, преобразование проверяет наличие перекрывающихся точек при расширении координат прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2f00c-317">As before, the transform checks for overflows when expanding a rectangle's coordinates.</span></span>


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



<span data-ttu-id="2f00c-318">На этом рисунке показано вычисление.</span><span class="sxs-lookup"><span data-stu-id="2f00c-318">This figure visualizes the calculation.</span></span> <span data-ttu-id="2f00c-319">[Direct2D](./direct2d-portal.md) автоматически выбирает прозрачные черные пиксели, где не существует входного изображения, что позволяет постепенно смешивать размытие с существующим содержимым на экране.</span><span class="sxs-lookup"><span data-stu-id="2f00c-319">[Direct2D](./direct2d-portal.md) automatically samples transparent black pixels where the input image doesn't exist, allowing the blur to be blended gradually with the existing content on the screen.</span></span>

![Иллюстрация непрозрачных черных точек с выборкой эффектов за пределами прямоугольника.](images/custom-effects3.png)

<span data-ttu-id="2f00c-321">Если сопоставление не является тривиальным, этот метод должен установить максимальный размер области, чтобы гарантировать правильность результатов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-321">If the mapping is non-trivial, then this method should set the input rectangle to the maximum area to guarantee correct results.</span></span> <span data-ttu-id="2f00c-322">Для этого установите для левого и верхнего краев значение INT \_ min, а правое и нижнее края — максимум int \_ .</span><span class="sxs-lookup"><span data-stu-id="2f00c-322">To do this, set the left and top edges to INT\_MIN, and the right and bottom edges to INT\_MAX.</span></span>

<span data-ttu-id="2f00c-323">Дополнительные сведения об этом методе см. в разделе [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-323">For more info about this method, see the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) topic.</span></span>

### <a name="mapinvalidrect"></a><span data-ttu-id="2f00c-324">мапинвалидрект</span><span class="sxs-lookup"><span data-stu-id="2f00c-324">MapInvalidRect</span></span>

<span data-ttu-id="2f00c-325">[Direct2D](./direct2d-portal.md) также вызывает метод [**мапинвалидрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-325">[Direct2D](./direct2d-portal.md) also calls the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) method.</span></span> <span data-ttu-id="2f00c-326">Однако, в отличие от методов [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) и [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) , Direct2D не гарантирует его вызов в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="2f00c-326">However, unlike the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) and [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) methods Direct2D is not guaranteed to call it at any particular time.</span></span> <span data-ttu-id="2f00c-327">Этот метод концептуально определяет, какая часть выходных данных преобразования должна быть повторно подготовлена в ответ на часть или все изменения входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f00c-327">This method conceptually decides what part of a transform's output needs to be re-rendered in response to part or all of its input changing.</span></span> <span data-ttu-id="2f00c-328">Существует три разных сценария для вычисления недопустимого Rect преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-328">There are three different scenarios for which to calculate a transform's invalid rect.</span></span>

### <a name="transforms-with-one-to-one-pixel-mapping"></a><span data-ttu-id="2f00c-329">Преобразование с сопоставлением "один к одному" в пикселях</span><span class="sxs-lookup"><span data-stu-id="2f00c-329">Transforms with one-to-one pixel mapping</span></span>

<span data-ttu-id="2f00c-330">Для преобразований, которые сопоставляют пиксел 1-1, просто передают Недопустимый входной прямоугольник в недопустимый выходной прямоугольник:</span><span class="sxs-lookup"><span data-stu-id="2f00c-330">For transforms that map pixels 1-1, simply pass the invalid input rectangle through to the invalid output rectangle:</span></span>


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



### <a name="transforms-with-many-to-many-pixel-mapping"></a><span data-ttu-id="2f00c-331">Преобразования с сопоставлением "многие ко многим" в пикселях</span><span class="sxs-lookup"><span data-stu-id="2f00c-331">Transforms with many-to-many pixel mapping</span></span>

<span data-ttu-id="2f00c-332">Если выходные точки преобразования зависят от окружающей области, недопустимый входной прямоугольник должен быть развернут соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="2f00c-332">When a transform's output pixels are dependent on their surrounding area, the invalid input rectangle must correspondingly be expanded.</span></span> <span data-ttu-id="2f00c-333">Это необходимо для отражения того, что пиксели вокруг недопустимого прямоугольника ввода также будут затронуты и станут недействительными.</span><span class="sxs-lookup"><span data-stu-id="2f00c-333">This is to reflect that pixels surrounding the invalid input rectangle will also be affected and become invalid.</span></span> <span data-ttu-id="2f00c-334">Например, размытие в 5 пикселей использует следующее вычисление:</span><span class="sxs-lookup"><span data-stu-id="2f00c-334">For example, a five pixel blur uses the following calculation:</span></span>


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a><span data-ttu-id="2f00c-335">Преобразования со сложным сопоставлением пикселей</span><span class="sxs-lookup"><span data-stu-id="2f00c-335">Transforms with complex pixel mapping</span></span>

<span data-ttu-id="2f00c-336">Для преобразований, где входные и выходные Пиксели не имеют простого сопоставления, все выходные данные могут быть помечены как недопустимые.</span><span class="sxs-lookup"><span data-stu-id="2f00c-336">For transforms where input and output pixels do not have a simple mapping, the entire output can be marked as invalid.</span></span> <span data-ttu-id="2f00c-337">Например, если преобразование просто выводит средний цвет входных данных, все выходные данные преобразования преобразуются, если изменяется даже небольшая часть входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f00c-337">For example, if a transform simply outputs the average color of the input, the entire output of the transform changes if even a small part of the input is changed.</span></span> <span data-ttu-id="2f00c-338">В этом случае недопустимый прямоугольник вывода должен быть задан логически бесконечным прямоугольником (как показано ниже).</span><span class="sxs-lookup"><span data-stu-id="2f00c-338">In this case, the invalid output rectangle should be set to a logically infinite rectangle (shown below).</span></span> <span data-ttu-id="2f00c-339">[Direct2D](./direct2d-portal.md) автоматически применяет это к границам выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2f00c-339">[Direct2D](./direct2d-portal.md) automatically clamps this to the bounds of the output.</span></span>


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



<span data-ttu-id="2f00c-340">Дополнительные сведения об этом методе см. в разделе [**мапинвалидрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-340">For more info about this method, see the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) topic.</span></span>

<span data-ttu-id="2f00c-341">После реализации этих методов заголовок преобразования будет содержать следующее:</span><span class="sxs-lookup"><span data-stu-id="2f00c-341">Once these methods have been implemented, your transform's header will contain the following:</span></span>


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



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a><span data-ttu-id="2f00c-342">Добавление шейдера пикселей к пользовательскому преобразованию</span><span class="sxs-lookup"><span data-stu-id="2f00c-342">Adding a pixel shader to a custom transform</span></span>

<span data-ttu-id="2f00c-343">После создания преобразования необходимо предоставить шейдер, который будет манипулировать пикселями изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-343">Once a transform has been created, it needs to provide a shader that will manipulate the image pixels.</span></span> <span data-ttu-id="2f00c-344">В этом разделе описаны шаги по использованию шейдера пикселей с пользовательским преобразованием.</span><span class="sxs-lookup"><span data-stu-id="2f00c-344">This section covers the steps to using a pixel shader with a custom transform.</span></span>

### <a name="implementing-id2d1drawtransform"></a><span data-ttu-id="2f00c-345">Реализация ID2D1DrawTransform</span><span class="sxs-lookup"><span data-stu-id="2f00c-345">Implementing ID2D1DrawTransform</span></span>

<span data-ttu-id="2f00c-346">Для использования шейдера пикселей преобразование должно реализовывать интерфейс [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , который наследуется от интерфейса [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) , описанного в разделе 5.</span><span class="sxs-lookup"><span data-stu-id="2f00c-346">To use a pixel shader, the transform must implement the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, which inherits from the [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface described in section 5.</span></span> <span data-ttu-id="2f00c-347">Этот интерфейс содержит один новый метод для реализации:</span><span class="sxs-lookup"><span data-stu-id="2f00c-347">This interface contains one new method to implement:</span></span>

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a><span data-ttu-id="2f00c-348">Сетдравинфо (ID2D1DrawInfo \* пдравинфо)</span><span class="sxs-lookup"><span data-stu-id="2f00c-348">SetDrawInfo(ID2D1DrawInfo \*pDrawInfo)</span></span>

<span data-ttu-id="2f00c-349">[Direct2D](./direct2d-portal.md) вызывает метод [**сетдравинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) при первом добавлении преобразования к графу преобразования воздействия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-349">[Direct2D](./direct2d-portal.md) calls the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="2f00c-350">Этот метод предоставляет параметр [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) , который управляет отображением преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-350">This method provides an [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="2f00c-351">Методы, доступные здесь, см. в разделе **ID2D1DrawInfo** .</span><span class="sxs-lookup"><span data-stu-id="2f00c-351">See the **ID2D1DrawInfo** topic for the methods available here.</span></span>

<span data-ttu-id="2f00c-352">Если преобразование выбирает сохранение этого параметра в качестве переменной-члена класса, доступ к объекту *дравинфо* можно получить и изменить с других методов, таких как методы задания свойств или [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="2f00c-352">If the transform chooses to store this parameter as a class member variable, the *drawInfo* object can be accessed and changed from other methods such as property setters or [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="2f00c-353">В частности, ее нельзя вызывать из методов [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) или [**мапинвалидрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) в [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="2f00c-353">Notably, it cannot be called from the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) or [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods on [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span>

### <a name="creating-a-guid-for-the-pixel-shader"></a><span data-ttu-id="2f00c-354">Создание идентификатора GUID для шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="2f00c-354">Creating a GUID for the pixel shader</span></span>

<span data-ttu-id="2f00c-355">Затем преобразование должно определить уникальный идентификатор GUID для самого построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="2f00c-355">Next, the transform must define a unique GUID for the pixel shader itself.</span></span> <span data-ttu-id="2f00c-356">Это используется, когда [Direct2D](./direct2d-portal.md) загружает шейдер в память, а также когда преобразование выбирает, какой шейдер пикселей использовать для выполнения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-356">This is used when [Direct2D](./direct2d-portal.md) loads the shader into memory, as well as when the transform chooses which pixel shader to use for execution.</span></span> <span data-ttu-id="2f00c-357">Такие средства, как guidgen.exe, включенные в Visual Studio, можно использовать для создания случайного идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="2f00c-357">Tools such as guidgen.exe, which is included with Visual Studio, can be used to generate a random GUID.</span></span>


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a><span data-ttu-id="2f00c-358">Загрузка построителя текстуры с помощью Direct2D</span><span class="sxs-lookup"><span data-stu-id="2f00c-358">Loading the pixel shader with Direct2D</span></span>

<span data-ttu-id="2f00c-359">Построитель текстуры необходимо загрузить в память, прежде чем его можно будет использовать в преобразовании.</span><span class="sxs-lookup"><span data-stu-id="2f00c-359">A pixel shader must be loaded into memory before it can be used by the transform.</span></span>

<span data-ttu-id="2f00c-360">Чтобы загрузить шейдер пикселей в память, преобразование должно считать скомпилированный байтовый код шейдера из. Файл CSO, созданный Visual Studio (подробные сведения см. в документации по [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ), в массив байтов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-360">To load the pixel shader into memory, the transform should read the compiled shader byte code from the .CSO file generated by Visual Studio (see [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details) into a byte array.</span></span> <span data-ttu-id="2f00c-361">Этот метод подробно описан в [примере D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="2f00c-361">This technique is demonstrated in detail in the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="2f00c-362">После загрузки данных шейдера в массив байтов вызовите метод [**лоадпикселшадер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) объекта [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) результата.</span><span class="sxs-lookup"><span data-stu-id="2f00c-362">Once the shader data has been loaded into a byte array, call the [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) method on the effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object.</span></span> <span data-ttu-id="2f00c-363">[Direct2D](./direct2d-portal.md) игнорирует вызовы **лоадпикселшадер** , если уже загружен шейдер с таким же идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="2f00c-363">[Direct2D](./direct2d-portal.md) ignores calls to **LoadPixelShader** when a shader with the same GUID has already been loaded.</span></span>

<span data-ttu-id="2f00c-364">После загрузки построителя текстуры в память преобразование необходимо выбрать для выполнения, передав его идентификатор GUID методу [**сетпикселшадер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) в параметре [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) , предоставленном в методе [**сетдравинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-364">After a pixel shader has been loaded into memory, the transform needs to select it for execution by passing its GUID to the [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided during the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="2f00c-365">Перед тем как выбрать для выполнения, шейдер пикселей должен быть уже загружен в память.</span><span class="sxs-lookup"><span data-stu-id="2f00c-365">The pixel shader must be already loaded into memory before being selected for execution.</span></span>

### <a name="changing-shader-operation-with-constant-buffers"></a><span data-ttu-id="2f00c-366">Изменение операции шейдера с постоянными буферами</span><span class="sxs-lookup"><span data-stu-id="2f00c-366">Changing shader operation with constant buffers</span></span>

<span data-ttu-id="2f00c-367">Чтобы изменить способ выполнения шейдера, преобразование может передать буфер константы в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="2f00c-367">To change how a shader executes, a transform may pass a constant buffer to the pixel shader.</span></span> <span data-ttu-id="2f00c-368">Для этого преобразование определяет структуру, содержащую нужные переменные в заголовке класса:</span><span class="sxs-lookup"><span data-stu-id="2f00c-368">To do so, a transform defines a struct that contains the desired variables in the class header:</span></span>


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



<span data-ttu-id="2f00c-369">Затем преобразование вызывает метод [**ID2D1DrawInfo:: сетпикселшадерконстантбуффер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) для параметра [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) , указанного в методе [**сетдравинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) , чтобы передать этот буфер шейдеру.</span><span class="sxs-lookup"><span data-stu-id="2f00c-369">The transform then calls the [**ID2D1DrawInfo::SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided in the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method to pass this buffer to the shader.</span></span>

<span data-ttu-id="2f00c-370">[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) также необходимо определить соответствующую структуру, которая представляет буфер констант.</span><span class="sxs-lookup"><span data-stu-id="2f00c-370">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) also needs to define a corresponding struct that represents the constant buffer.</span></span> <span data-ttu-id="2f00c-371">Переменные, содержащиеся в структуре шейдера, должны соответствовать значениям в структуре преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-371">The variables contained in the shader's struct must match those in the transform's struct.</span></span>


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



<span data-ttu-id="2f00c-372">После определения буфера значения, содержащиеся в, могут быть считаны в любом месте шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2f00c-372">Once the buffer has been defined, the values contained within can be read from anywhere within the pixel shader.</span></span>

### <a name="writing-a-pixel-shader-for-direct2d"></a><span data-ttu-id="2f00c-373">Создание построителя текстуры для Direct2D</span><span class="sxs-lookup"><span data-stu-id="2f00c-373">Writing a pixel shader for Direct2D</span></span>

<span data-ttu-id="2f00c-374">Преобразования [Direct2D](./direct2d-portal.md) используют шейдеры, созданные с помощью стандартного [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span><span class="sxs-lookup"><span data-stu-id="2f00c-374">[Direct2D](./direct2d-portal.md) transforms use shaders authored using standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="2f00c-375">Однако существует несколько ключевых концепций для написания шейдера пикселей, выполняемого из контекста преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-375">However, there are a few key concepts to writing a pixel shader that executes from the context of a transform.</span></span> <span data-ttu-id="2f00c-376">Готовый пример полностью функционального шейдера пикселей см. в [примере D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="2f00c-376">For a completed example of a fully functionally pixel shader, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="2f00c-377">[Direct2D](./direct2d-portal.md) автоматически сопоставляет входные данные преобразования с объектами [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) и [**самплерстате**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) в HLSL.</span><span class="sxs-lookup"><span data-stu-id="2f00c-377">[Direct2D](./direct2d-portal.md) automatically maps a transform's inputs to [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) objects in the HLSL.</span></span> <span data-ttu-id="2f00c-378">Первый **Texture2D** находится в папке Register T0, а первый **самплерстате** находится в регистре S0.</span><span class="sxs-lookup"><span data-stu-id="2f00c-378">The first **Texture2D** is located at register t0, and the first **SamplerState** is located at register s0.</span></span> <span data-ttu-id="2f00c-379">Каждый дополнительный вход находится в следующих соответствующих регистрах (например, T1 и S1).</span><span class="sxs-lookup"><span data-stu-id="2f00c-379">Each additional input is located at the next corresponding registers (t1 and s1 for example).</span></span> <span data-ttu-id="2f00c-380">Данные в пикселях для определенных входных данных могут быть выборке путем вызова Sample в объекте **Texture2D** и передачи соответствующего объекта **самплерстате** и координат шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="2f00c-380">Pixel data for a particular input can be sampled by calling Sample on the **Texture2D** object and passing in the corresponding **SamplerState** object and the texel coordinates.</span></span>

<span data-ttu-id="2f00c-381">Пользовательский шейдер пикселей выполняется один раз для каждого отображаемого пикселя.</span><span class="sxs-lookup"><span data-stu-id="2f00c-381">A custom pixel shader is run once for each pixel that is rendered.</span></span> <span data-ttu-id="2f00c-382">При каждом запуске шейдера [Direct2D](./direct2d-portal.md) автоматически предоставляет три параметра, которые обозначают текущее расположение выполнения:</span><span class="sxs-lookup"><span data-stu-id="2f00c-382">Each time the shader is run, [Direct2D](./direct2d-portal.md) automatically provides three parameters that identify its current execution position:</span></span>

-   <span data-ttu-id="2f00c-383">Выходное пространство сцены. Этот параметр представляет текущую точку выполнения с точки зрения общей целевой поверхности.</span><span class="sxs-lookup"><span data-stu-id="2f00c-383">Scene-space output: This parameter represents the current execution position in terms of the overall target surface.</span></span> <span data-ttu-id="2f00c-384">Он определен в пикселях, а его минимальное и максимальное значения соответствуют границам прямоугольника, возвращаемого функцией [**мапинпутректстуутпутрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="2f00c-384">It is defined in pixels and its min/max values correspond to the bounds of the rectangle returned by [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span>
-   <span data-ttu-id="2f00c-385">Выходные данные клипа: этот параметр используется Direct3D и не должен использоваться в шейдере пикселей преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-385">Clip-space output: This parameter is used by Direct3D, and is must not be used in a transform's pixel shader.</span></span>
-   <span data-ttu-id="2f00c-386">Шаг текселя-Space input: этот параметр представляет текущую точку выполнения в определенной текстуре ввода.</span><span class="sxs-lookup"><span data-stu-id="2f00c-386">Texel-space input: This parameter represents the current execution position in a particular input texture.</span></span> <span data-ttu-id="2f00c-387">Шейдер не должен зависеть от того, как вычисляется это значение.</span><span class="sxs-lookup"><span data-stu-id="2f00c-387">A shader should not take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="2f00c-388">Он должен использовать его только для выборки входных шейдеров пикселей, как показано в приведенном ниже коде.</span><span class="sxs-lookup"><span data-stu-id="2f00c-388">It should only use it to sample the pixel shader's input, as shown in the code below:</span></span>


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



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a><span data-ttu-id="2f00c-389">Добавление шейдера вершин к пользовательскому преобразованию</span><span class="sxs-lookup"><span data-stu-id="2f00c-389">Adding a vertex shader to a custom transform</span></span>

<span data-ttu-id="2f00c-390">Шейдеры вершин можно использовать для выполнения различных сценариев работы с образами, чем шейдеры пикселей.</span><span class="sxs-lookup"><span data-stu-id="2f00c-390">You can use vertex shaders to accomplish different imaging scenarios than pixel shaders.</span></span> <span data-ttu-id="2f00c-391">В частности, шейдеры вершин могут выполнять эффекты изображений на основе геометрии путем преобразования вершин, составляющих изображение.</span><span class="sxs-lookup"><span data-stu-id="2f00c-391">In particular, vertex shaders can perform geometry-based image effects by transforming vertices that comprise an image.</span></span> <span data-ttu-id="2f00c-392">Шейдеры вершин можно использовать независимо друг от друга и в сочетании с заданными шейдерами пикселей.</span><span class="sxs-lookup"><span data-stu-id="2f00c-392">Vertex shaders can be used independently of or in conjunction with transform-specified pixel shaders.</span></span> <span data-ttu-id="2f00c-393">Если шейдер вершин не указан, [Direct2D](./direct2d-portal.md) замещает в шейдер вершин по умолчанию для использования с пользовательским шейдером пикселей.</span><span class="sxs-lookup"><span data-stu-id="2f00c-393">If a vertex shader is not specified, [Direct2D](./direct2d-portal.md) substitutes in a default vertex shader for use with the custom pixel shader.</span></span>

<span data-ttu-id="2f00c-394">Процесс добавления шейдера вершин к пользовательскому преобразованию аналогичен построителю построителей текстуры — преобразование реализует интерфейс [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , создает идентификатор GUID и (необязательно) передает буферы константы в шейдер.</span><span class="sxs-lookup"><span data-stu-id="2f00c-394">The process for adding a vertex shader to a custom transform is similar to that of a pixel shader – the transform implements the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, creates a GUID, and (optionally) passes constant buffers to the shader.</span></span> <span data-ttu-id="2f00c-395">Однако существует несколько основных дополнительных шагов, которые являются уникальными для шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="2f00c-395">However, there are a few key additional steps that are unique to vertex shaders:</span></span>

### <a name="creating-a-vertex-buffer"></a><span data-ttu-id="2f00c-396">Создание буфера вершин</span><span class="sxs-lookup"><span data-stu-id="2f00c-396">Creating a vertex buffer</span></span>

<span data-ttu-id="2f00c-397">Шейдер вершин по определению выполняется для переданных вершин, а не для отдельных пикселов.</span><span class="sxs-lookup"><span data-stu-id="2f00c-397">A vertex shader by definition executes on vertices passed to it, not individual pixels.</span></span> <span data-ttu-id="2f00c-398">Чтобы указать вершины для выполнения в шейдере, преобразование создает буфер вершин для передачи шейдеру.</span><span class="sxs-lookup"><span data-stu-id="2f00c-398">To specify the vertices for the shader to execute on, a transform creates a vertex buffer to pass to the shader.</span></span> <span data-ttu-id="2f00c-399">Макет буферов вершин выходит за рамки данного документа.</span><span class="sxs-lookup"><span data-stu-id="2f00c-399">The layout of vertex buffers is beyond the scope of this document.</span></span> <span data-ttu-id="2f00c-400">Дополнительные сведения см. в [справочнике по Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) или [примере D2DCustomEffects SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) для примера реализации.</span><span class="sxs-lookup"><span data-stu-id="2f00c-400">Please see the [Direct3D reference](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) for details, or the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="2f00c-401">После создания буфера вершин в памяти преобразование использует метод [**креатевертексбуффер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) объекта [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) содержащего его результата для передачи этих данных в GPU.</span><span class="sxs-lookup"><span data-stu-id="2f00c-401">After creating a vertex buffer in memory, the transform uses the [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) method on the containing effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object to pass that data to the GPU.</span></span> <span data-ttu-id="2f00c-402">Пример реализации см. в [примере пакета SDK для D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-402">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="2f00c-403">Если преобразование не указывает ни одного буфера вершин, [Direct2D](./direct2d-portal.md) передает буфер вершин по умолчанию, представляющий расположение прямоугольного изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-403">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) passes a default vertex buffer representing the rectangular image location.</span></span>

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a><span data-ttu-id="2f00c-404">Изменение Сетдравинфо для использования шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="2f00c-404">Changing SetDrawInfo to utilize a vertex shader</span></span>

<span data-ttu-id="2f00c-405">Как и в шейдерах пикселей, преобразование должно загрузиться и выбрать шейдер вершин для выполнения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-405">Like with pixel shaders, the transform must load and select a vertex shader for execution.</span></span> <span data-ttu-id="2f00c-406">Чтобы загрузить шейдер вершин, он вызывает метод [**лоадвертексшадер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) для метода [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) , полученного в методе Initialize результата.</span><span class="sxs-lookup"><span data-stu-id="2f00c-406">To load the vertex shader, it calls the [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) method on the [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) method received in the effect's Initialize method.</span></span> <span data-ttu-id="2f00c-407">Чтобы выбрать шейдер вершин для выполнения, он вызывает [**сетвертекспроцессинг**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) в параметре [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) , полученном в методе [**сетдравинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-407">To select the vertex shader for execution, it calls [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter received in the transform's [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="2f00c-408">Этот метод принимает идентификатор GUID для ранее загруженного шейдера вершин, а также (дополнительно) созданного ранее буфера вершин для выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="2f00c-408">This method accepts a GUID for a previously-loaded vertex shader as well as (optionally) a previously-created vertex buffer for the shader to execute on.</span></span>

### <a name="implementing-a-direct2d-vertex-shader"></a><span data-ttu-id="2f00c-409">Реализация шейдера вершин Direct2D</span><span class="sxs-lookup"><span data-stu-id="2f00c-409">Implementing a Direct2D vertex shader</span></span>

<span data-ttu-id="2f00c-410">Преобразование «Рисование» может содержать как шейдер пикселей, так и шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="2f00c-410">A draw transform can contain both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="2f00c-411">Если преобразование определяет и шейдер пикселей, и шейдер вершин, то выходные данные шейдера вершин передаются непосредственно шейдеру пикселей. приложение может настроить возвращаемую сигнатуру шейдера вершин или параметры шейдера пикселей, если они являются единообразными.</span><span class="sxs-lookup"><span data-stu-id="2f00c-411">If a transform defines both a pixel shader and a vertex shader, then the output from the vertex shader is given directly to the pixel shader: the app can customize the return signature of the vertex shader / the parameters of the pixel shader as long as they are consistent.</span></span>

<span data-ttu-id="2f00c-412">С другой стороны, если преобразование содержит только шейдер вершин и полагается на построитель текстуры [Direct2D](./direct2d-portal.md)по умолчанию, он должен вернуть следующий результат по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="2f00c-412">On the other hand, if a transform only contains a vertex shader, and relies on [Direct2D](./direct2d-portal.md)'s default pass-through pixel shader, it must return the following default output:</span></span>


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="2f00c-413">Шейдер вершин сохраняет результат преобразований вершин в выходной переменной построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="2f00c-413">A vertex shader stores the result of its vertex transformations in the shader's Scene-space output variable.</span></span> <span data-ttu-id="2f00c-414">Чтобы вычислить выходные данные в пространстве Clip и шаг текселя переменные, [Direct2D](./direct2d-portal.md) автоматически предоставляет матрицы преобразования в буфере констант:</span><span class="sxs-lookup"><span data-stu-id="2f00c-414">To compute the Clip-space output and the Texel-space input variables, [Direct2D](./direct2d-portal.md) automatically provides conversion matrices in a constant buffer:</span></span>


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



<span data-ttu-id="2f00c-415">Ниже приведен пример кода шейдера вершин, в котором используются матрицы преобразования для вычисления правильных шаг текселя и пробелов, ожидаемых [Direct2D](./direct2d-portal.md):</span><span class="sxs-lookup"><span data-stu-id="2f00c-415">Sample vertex shader code can be found below that uses the conversion matrices to calculate the correct clip and texel spaces expected by [Direct2D](./direct2d-portal.md):</span></span>


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



<span data-ttu-id="2f00c-416">Приведенный выше код можно использовать в качестве отправной точки для шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="2f00c-416">The above code can be used as a starting point for a vertex shader.</span></span> <span data-ttu-id="2f00c-417">Он просто проходит через входной образ без выполнения преобразований.</span><span class="sxs-lookup"><span data-stu-id="2f00c-417">It merely passes through the input image without performing any transforms.</span></span> <span data-ttu-id="2f00c-418">См. [Пример D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) для полностью реализованного преобразования на основе шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="2f00c-418">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a fully-implemented vertex shader-based transform.</span></span>

<span data-ttu-id="2f00c-419">Если в преобразовании не задан буфер вершин, [Direct2D](./direct2d-portal.md) заменяет в буфере вершин по умолчанию, представляющего Прямоугольное расположение изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-419">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) substitutes in a default vertex buffer representing the rectangular image location.</span></span> <span data-ttu-id="2f00c-420">Параметры шейдера вершин заменяются на значения, указанные в выходных данных шейдера по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="2f00c-420">The parameters to the vertex shader are changed to those of the default shader output:</span></span>


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="2f00c-421">Шейдер вершин не может изменять параметры *сценеспацеаутпут* и *клипспацеаутпут* .</span><span class="sxs-lookup"><span data-stu-id="2f00c-421">The vertex shader may not modify its *sceneSpaceOutput* and *clipSpaceOutput* parameters.</span></span> <span data-ttu-id="2f00c-422">Он должен вернуть их без изменений.</span><span class="sxs-lookup"><span data-stu-id="2f00c-422">It must return them unchanged.</span></span> <span data-ttu-id="2f00c-423">Однако это может привести к изменению параметров *текселспацеинпут* для каждого входного изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-423">It may however modify the *texelSpaceInput* parameter(s) for each input image.</span></span> <span data-ttu-id="2f00c-424">Если преобразование также содержит пользовательский шейдер пикселей, шейдер вершин по-прежнему может передавать дополнительные пользовательские параметры непосредственно в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="2f00c-424">If the transform also contains a custom pixel shader, the vertex shader is still able to pass additional custom parameters directly to the pixel shader.</span></span> <span data-ttu-id="2f00c-425">Кроме того, пользовательский буфер матриц преобразования *сценеспаце* (B0) больше не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="2f00c-425">Additionally, the *sceneSpace* conversion matrices custom buffer (b0) is no longer provided.</span></span>

## <a name="adding-a-compute-shader-to-a-custom-transform"></a><span data-ttu-id="2f00c-426">Добавление шейдера вычислений к пользовательскому преобразованию</span><span class="sxs-lookup"><span data-stu-id="2f00c-426">Adding a compute shader to a custom transform</span></span>

<span data-ttu-id="2f00c-427">Наконец, пользовательские преобразования могут использовать шейдеры вычислений для определенных целевых сценариев.</span><span class="sxs-lookup"><span data-stu-id="2f00c-427">Finally, custom transforms may utilize compute shaders for certain targeted scenarios.</span></span> <span data-ttu-id="2f00c-428">Шейдеры вычислений можно использовать для реализации сложных эффектов изображения, требующих произвольного доступа к входным и выходным буферам изображений.</span><span class="sxs-lookup"><span data-stu-id="2f00c-428">Compute shaders can be used to implement complex image effects that require arbitrary access to input and output image buffers.</span></span> <span data-ttu-id="2f00c-429">Например, базовый алгоритм гистограммы не может быть реализован с шейдером пикселей из-за ограничений доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="2f00c-429">For example, a basic histogram algorithm cannot be implemented with a pixel shader due to limitations on memory access.</span></span>

<span data-ttu-id="2f00c-430">Поскольку шейдеры вычислений имеют более высокие требования к оборудованию, чем шейдеры пикселей, следует использовать шейдеры пикселей, если это возможно для реализации данного воздействия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-430">Because compute shaders have higher hardware feature level requirements than pixel shaders, pixel shaders should be used when possible to implement a given effect.</span></span> <span data-ttu-id="2f00c-431">В частности, шейдеры вычислений работают только на большинстве карт на уровне DirectX 10 и выше.</span><span class="sxs-lookup"><span data-stu-id="2f00c-431">Specifically, compute shaders only run on most DirectX 10 level cards and higher.</span></span> <span data-ttu-id="2f00c-432">Если преобразование выбирает использование шейдера вычислений, оно должно проверять наличие соответствующей аппаратной поддержки во время создания экземпляра в дополнение к реализации интерфейса [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-432">If a transform chooses to use a compute shader, it must check for the appropriate hardware support during instantiation in addition to implementing the [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) interface.</span></span>

### <a name="checking-for-compute-shader-support"></a><span data-ttu-id="2f00c-433">Проверка поддержки шейдера вычислений</span><span class="sxs-lookup"><span data-stu-id="2f00c-433">Checking for Compute Shader support</span></span>

<span data-ttu-id="2f00c-434">Если действие использует шейдер вычислений, оно должно проверять поддержку шейдера вычислений во время его создания с помощью метода [**ID2D1EffectContext:: чеккфеатуресуппорт**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-434">If an effect uses a compute shader, it must check for compute shader support during its creation using the [**ID2D1EffectContext::CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) method.</span></span> <span data-ttu-id="2f00c-435">Если GPU не поддерживает шейдеры вычислений, этот результат должен возвращать [**D2DERR \_ недостаточных \_ \_ возможностей устройства**](direct2d-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2f00c-435">If the GPU does not support compute shaders, the effect must return [**D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES**](direct2d-error-codes.md).</span></span>

<span data-ttu-id="2f00c-436">Существует два разных типа шейдеров вычислений, которые может использовать преобразование: Shader Model 4 (DirectX 10) и Shader Model 5 (DirectX 11).</span><span class="sxs-lookup"><span data-stu-id="2f00c-436">There are two different types of compute shaders that a transform can use: Shader Model 4 (DirectX 10) and Shader Model 5 (DirectX 11).</span></span> <span data-ttu-id="2f00c-437">Существуют определенные ограничения шейдера Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="2f00c-437">There are certain limitations to Shader Model 4 shaders.</span></span> <span data-ttu-id="2f00c-438">Дополнительные сведения см. в документации по [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-438">See the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details.</span></span> <span data-ttu-id="2f00c-439">Преобразования могут содержать оба типа шейдеров и могут возвращаться к модели шейдера 4 при необходимости: см. [Пример D2DCUSTOMEFFECTS SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) для реализации этого.</span><span class="sxs-lookup"><span data-stu-id="2f00c-439">Transforms can contain both types of shaders, and can fall back to Shader Model 4 when required: see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for an implementation of this.</span></span>

### <a name="implement-id2d1computetransform"></a><span data-ttu-id="2f00c-440">Реализация ID2D1ComputeTransform</span><span class="sxs-lookup"><span data-stu-id="2f00c-440">Implement ID2D1ComputeTransform</span></span>

<span data-ttu-id="2f00c-441">Этот интерфейс содержит два новых метода для реализации в дополнение к классам в [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="2f00c-441">This interface contains two new methods to implement in addition to the ones in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span></span>

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a><span data-ttu-id="2f00c-442">Сеткомпутеинфо (ID2D1ComputeInfo \* пкомпутеинфо)</span><span class="sxs-lookup"><span data-stu-id="2f00c-442">SetComputeInfo(ID2D1ComputeInfo \*pComputeInfo)</span></span>

<span data-ttu-id="2f00c-443">Как и в шейдерах пикселей и вершин, [Direct2D](./direct2d-portal.md) вызывает метод [**сеткомпутеинфо**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) при первом добавлении преобразования к графу преобразования воздействия.</span><span class="sxs-lookup"><span data-stu-id="2f00c-443">Like with pixel and vertex shaders, [Direct2D](./direct2d-portal.md) calls the [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="2f00c-444">Этот метод предоставляет параметр [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) , который управляет отображением преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f00c-444">This method provides an [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="2f00c-445">Это включает выбор шейдера вычислений для выполнения с помощью метода [**ID2D1ComputeInfo:: сеткомпутешадер**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-445">This includes choosing the compute shader to execute through the [**ID2D1ComputeInfo::SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) method.</span></span> <span data-ttu-id="2f00c-446">Если преобразование выбирает сохранение этого параметра в качестве переменной-члена класса, к нему можно получить доступ и изменить любой метод преобразования или воздействия с исключением методов [**мапаутпутректтоинпутректс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) и [**мапинвалидрект**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="2f00c-446">If the transform chooses to store this parameter as a class member variable, it can be accessed and changed from any transform or effect method with the exception of the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) and [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods.</span></span> <span data-ttu-id="2f00c-447">Другие методы, доступные здесь, см. в разделе **ID2D1ComputeInfo** .</span><span class="sxs-lookup"><span data-stu-id="2f00c-447">See the **ID2D1ComputeInfo** topic for other methods available here.</span></span>

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a><span data-ttu-id="2f00c-448">Калкулатесреадграупс (ID2D1ComputeInfo \* паутпутрект, UInt32 \* ПДИМЕНСИОНКС, UInt32 \* пдименсиони, UInt32 \* пдименсионз)</span><span class="sxs-lookup"><span data-stu-id="2f00c-448">CalculateThreadgroups(ID2D1ComputeInfo \*pOutputRect, UINT32 \*pDimensionX, UINT32 \*pDimensionY, UINT32 \*pDimensionZ)</span></span>

<span data-ttu-id="2f00c-449">В то время как шейдеры пикселей выполняются для каждого отдельного пикселя, а шейдеры вершин выполняются для каждой вершины, шейдеры вычислений выполняются для каждого 'среадграуп.</span><span class="sxs-lookup"><span data-stu-id="2f00c-449">Whereas pixel shaders are executed on a per-pixel basis and vertex shaders are executed on a per-vertex basis, compute shaders are executed on a per-'threadgroup' basis.</span></span> <span data-ttu-id="2f00c-450">Среадграуп представляет собой количество потоков, выполняемых параллельно на GPU.</span><span class="sxs-lookup"><span data-stu-id="2f00c-450">A threadgroup represents a number of threads that execute concurrently on the GPU.</span></span> <span data-ttu-id="2f00c-451">Код HLSLа COMPUTE Shader определяет, сколько потоков должно выполняться для каждого среадграуп.</span><span class="sxs-lookup"><span data-stu-id="2f00c-451">The compute shader HLSL code decides how many threads should be executed per threadgroup.</span></span> <span data-ttu-id="2f00c-452">Этот результат масштабирует количество среадграупс, чтобы шейдер выполнял нужное количество раз, в зависимости от логики шейдера.</span><span class="sxs-lookup"><span data-stu-id="2f00c-452">The effect scales the number of threadgroups so that the shader executes the desired number of times, depending on the shader's logic.</span></span>

<span data-ttu-id="2f00c-453">Метод [**калкулатесреадграупс**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) позволяет преобразованию сообщать [Direct2D](./direct2d-portal.md) о том, сколько групп потоков требуется, в зависимости от размера изображения и собственных знаний о преобразовании шейдера.</span><span class="sxs-lookup"><span data-stu-id="2f00c-453">The [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) method allows the transform to inform [Direct2D](./direct2d-portal.md) how many thread groups are required, based on the size of the image and the transform's own knowledge of the shader.</span></span>

<span data-ttu-id="2f00c-454">Количество раз, когда выполняется шейдер вычислений, — это продукт с указанными здесь счетчиками среадграуп и заметка "numthreads" в [HLSLе](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)COMPUTE Shader.</span><span class="sxs-lookup"><span data-stu-id="2f00c-454">The number of times the compute shader is executed is a product of the threadgroup counts specified here and the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="2f00c-455">Например, если преобразование задает среадграуп измерения (2, 2, 1), то шейдер задаст (3, 3, 1) потоки на среадграуп, затем будет выполняться 4 среадграупс, каждый с 9 потоками в них, всего 36 экземпляров потоков.</span><span class="sxs-lookup"><span data-stu-id="2f00c-455">For example, if the transform sets the threadgroup dimensions to be (2,2,1) the shader specifies (3,3,1) threads per threadgroup, then 4 threadgroups will be executed, each with 9 threads in them, for a total of 36 thread instances.</span></span>

<span data-ttu-id="2f00c-456">Распространенным сценарием является обработка одного выходного пикселя для каждого экземпляра вычислительного шейдера.</span><span class="sxs-lookup"><span data-stu-id="2f00c-456">A common scenario is to process one output pixel for each instance of the compute shader.</span></span> <span data-ttu-id="2f00c-457">Чтобы вычислить количество групп потоков для этого сценария, преобразование делит ширину и высоту изображения на соответствующие измерения x и y заметки "numthreads" в Compute Shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span><span class="sxs-lookup"><span data-stu-id="2f00c-457">To calculate the number of thread groups for this scenario, the transform divides the width and height of the image by the respective x and y dimensions of the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span>

<span data-ttu-id="2f00c-458">Важно! при выполнении этого деления число запрошенных групп потоков должно быть округлено до ближайшего целого числа, в противном случае "остаток" не будет выполняться после.</span><span class="sxs-lookup"><span data-stu-id="2f00c-458">Importantly, if this division is performed, then the number of thread groups requested must always be rounded up to the nearest integer, otherwise the 'remainder' pixels will not be executed upon.</span></span> <span data-ttu-id="2f00c-459">Если шейдер (например) рассчитывает один пиксель с каждым потоком, код метода будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2f00c-459">If a shader (for example) computes a single pixel with each thread, the method's code would appear as follows.</span></span>


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



<span data-ttu-id="2f00c-460">[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) использует следующий код, чтобы указать число потоков в каждой группе потоков:</span><span class="sxs-lookup"><span data-stu-id="2f00c-460">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) uses the following code to specify the number of threads in each thread group:</span></span>


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



<span data-ttu-id="2f00c-461">Во время выполнения текущий индекс потока и текущий среадграуп передаются в качестве параметров в метод шейдера:</span><span class="sxs-lookup"><span data-stu-id="2f00c-461">During execution, the current threadgroup and current thread index are passed as parameters to the shader method:</span></span>


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



### <a name="reading-image-data"></a><span data-ttu-id="2f00c-462">Чтение данных изображения</span><span class="sxs-lookup"><span data-stu-id="2f00c-462">Reading image data</span></span>

<span data-ttu-id="2f00c-463">С помощью шейдеров вычислений доступ к входному изображению преобразования можно получить в виде одной двухмерной текстуры:</span><span class="sxs-lookup"><span data-stu-id="2f00c-463">Compute shaders access the transform's input image as a single two-dimensional texture:</span></span>


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



<span data-ttu-id="2f00c-464">Однако, как и шейдеры пикселей, данные изображения не обязательно должны начинаться с (0,0) на текстуре.</span><span class="sxs-lookup"><span data-stu-id="2f00c-464">However, like pixel shaders, the image's data is not guaranteed to begin at (0, 0) on the texture.</span></span> <span data-ttu-id="2f00c-465">Вместо этого [Direct2D](./direct2d-portal.md) предоставляет системные константы, позволяющие шейдеру компенсировать любое смещение:</span><span class="sxs-lookup"><span data-stu-id="2f00c-465">Instead, [Direct2D](./direct2d-portal.md) provides system constants that allow shaders to compensate for any offset:</span></span>


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



<span data-ttu-id="2f00c-466">После определения приведенного выше буфера констант и вспомогательного метода шейдер может выполнить выборку данных изображения с помощью следующего:</span><span class="sxs-lookup"><span data-stu-id="2f00c-466">Once the above constant buffer and helper method have been defined, the shader can sample image data using the following:</span></span>


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



### <a name="writing-image-data"></a><span data-ttu-id="2f00c-467">Запись данных образа</span><span class="sxs-lookup"><span data-stu-id="2f00c-467">Writing image data</span></span>

<span data-ttu-id="2f00c-468">[Direct2D](./direct2d-portal.md) ожидает шейдер для определения выходного буфера для конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-468">[Direct2D](./direct2d-portal.md) expects a shader to define an output buffer for the resulting image to be placed.</span></span> <span data-ttu-id="2f00c-469">В модели шейдера 4 (DirectX 10) это должен быть одномерный буфер из-за ограничений функций:</span><span class="sxs-lookup"><span data-stu-id="2f00c-469">In Shader Model 4 (DirectX 10), this must be a single-dimensional buffer due to feature constraints:</span></span>


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



<span data-ttu-id="2f00c-470">Текстура вывода индексируется по строкам, чтобы разрешить сохранение всего изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-470">The output texture is indexed row-first to allow the entire image to be stored.</span></span>


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



<span data-ttu-id="2f00c-471">С другой стороны, шейдер Shader Model 5 (DirectX 11) может использовать двухмерные выходные текстуры:</span><span class="sxs-lookup"><span data-stu-id="2f00c-471">On the other hand, Shader Model 5 (DirectX 11) shaders can use two-dimensional output textures:</span></span>


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



<span data-ttu-id="2f00c-472">В шейдере Shader Model 5 [Direct2D](./direct2d-portal.md) предоставляет дополнительный параметр "аутпутоффсет" в буфере констант.</span><span class="sxs-lookup"><span data-stu-id="2f00c-472">With Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) provides an additional 'outputOffset' parameter in the constant buffer.</span></span> <span data-ttu-id="2f00c-473">Вывод шейдера должен быть оффсеттед следующим объемом:</span><span class="sxs-lookup"><span data-stu-id="2f00c-473">The shader's output should be offsetted by this amount:</span></span>


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="2f00c-474">Ниже показана завершенная пошаговая шейдер-передаваемая модель шейдеров 5.</span><span class="sxs-lookup"><span data-stu-id="2f00c-474">A completed pass-through Shader Model 5 compute shader is shown below.</span></span> <span data-ttu-id="2f00c-475">В нем каждый поток шейдера вычислений считывает и записывает один пиксель входного изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00c-475">In it, each of the compute shader threads reads and writes a single pixel of the input image.</span></span>


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



<span data-ttu-id="2f00c-476">В приведенном ниже коде показана эквивалентная версия шейдера модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="2f00c-476">The code below shows the equivalent Shader Model 4 version of the shader.</span></span> <span data-ttu-id="2f00c-477">Обратите внимание, что шейдер теперь преобразуется в одномерный выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="2f00c-477">Notice that the shader now renders into a single-dimensional output buffer.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2f00c-478">См. также</span><span class="sxs-lookup"><span data-stu-id="2f00c-478">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f00c-479">Пример пакета SDK для D2DCustomEffects</span><span class="sxs-lookup"><span data-stu-id="2f00c-479">D2DCustomEffects SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 