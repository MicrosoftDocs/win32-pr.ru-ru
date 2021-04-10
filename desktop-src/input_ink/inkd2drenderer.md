---
description: Реализует интерфейс IInkD2DRenderer.
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
title: Класс InkD2DRenderer
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkD2DRenderer
api_type:
- COM
api_location:
- Inkrenderer.idl
ms.openlocfilehash: 1649d52c2e9098513c115daaf295c4005e890b8e
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104273219"
---
# <a name="inkd2drenderer-class"></a><span data-ttu-id="97d0e-103">Класс InkD2DRenderer</span><span class="sxs-lookup"><span data-stu-id="97d0e-103">InkD2DRenderer class</span></span>

<span data-ttu-id="97d0e-104">Реализует интерфейс [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .</span><span class="sxs-lookup"><span data-stu-id="97d0e-104">Implements the [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) interface.</span></span>

<span data-ttu-id="97d0e-105">Объект [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) обеспечивает отрисовку рукописных штрихов в назначенном Direct2Dном контексте универсального приложения Windows вместо элемента управления [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97d0e-105">An [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="members"></a><span data-ttu-id="97d0e-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="97d0e-106">Members</span></span>

<span data-ttu-id="97d0e-107">Класс **InkD2DRenderer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="97d0e-107">The **InkD2DRenderer** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="97d0e-108">**InkD2DRenderer** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="97d0e-108">**InkD2DRenderer** also has these types of members:</span></span>

- [<span data-ttu-id="97d0e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="97d0e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97d0e-110">Методы</span><span class="sxs-lookup"><span data-stu-id="97d0e-110">Methods</span></span>

<span data-ttu-id="97d0e-111">Класс **InkD2DRenderer** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="97d0e-111">The **InkD2DRenderer** class has these methods.</span></span>

| <span data-ttu-id="97d0e-112">Метод</span><span class="sxs-lookup"><span data-stu-id="97d0e-112">Method</span></span>                              | <span data-ttu-id="97d0e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="97d0e-113">Description</span></span>                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="97d0e-114">**Draw**</span><span class="sxs-lookup"><span data-stu-id="97d0e-114">**Draw**</span></span>](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | <span data-ttu-id="97d0e-115">Преобразует рукописный штрих в назначенный контекст устройства Direct2D приложения.</span><span class="sxs-lookup"><span data-stu-id="97d0e-115">Renders the ink stroke to the designated Direct2D device context of the app.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="97d0e-116">\\Функции доступа для создания</span><span class="sxs-lookup"><span data-stu-id="97d0e-116">Creation\\Access Functions</span></span>

<span data-ttu-id="97d0e-117">Вызовите [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса <strong>InkD2DRenderer</strong> , чтобы получить ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="97d0e-117">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkD2DRenderer</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a><span data-ttu-id="97d0e-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="97d0e-118">Examples</span></span>

<span data-ttu-id="97d0e-119">Этот фрагмент кода из файла "Сценекомпосер. cpp" в [примере сложного](/samples/microsoft/windows-universal-samples/complexink/) рукописного ввода демонстрирует отрисовку коллекции рукописных штрихов в контексте устройства Direct2D.</span><span class="sxs-lookup"><span data-stu-id="97d0e-119">This snippet from the "SceneComposer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) demonstrates the rendering of a collection of ink strokes to a Direct2D device context.</span></span>

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

<span data-ttu-id="97d0e-120">В этом фрагменте кода из файла "Инкрендерер. cpp" в [образце сложных рукописных](/samples/microsoft/windows-universal-samples/complexink/) данных показан метод Render (вызванный в предыдущем фрагменте), который вызывает метод [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) для отрисовки штрихов.</span><span class="sxs-lookup"><span data-stu-id="97d0e-120">This snippet from the "InkRenderer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) shows the Render method (called in the previous snippet) that calls the [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) method for rendering the strokes.</span></span>

```C++
void InkRenderer::Render(
    Platform::Collections::Vector<
        Windows::UI::Input::Inking::InkStroke^>^ strokes,
        Microsoft::WRL::ComPtr<ID2D1DeviceContext> d2dContext)
{
    HRESULT hr = S_OK;
    if (_spInkD2DRenderer != nullptr)
    {
        if (strokes != nullptr && strokes->Size > 0)
        {
            // Cast the stroke collection into IUnknown to call Inkd2dRenderer
            ComPtr<IUnknown> spUnkStrokes = 
                reinterpret_cast<IUnknown*>(reinterpret_cast<__abi_IUnknown*>(strokes));
            hr = _spInkD2DRenderer->Draw(d2dContext.Get(), spUnkStrokes.Get(), false);
            if (FAILED(hr))
            {
                DX::ThrowIfFailed(hr);
            }
        }
    }
}
```

## <a name="requirements"></a><span data-ttu-id="97d0e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="97d0e-121">Requirements</span></span>

| <span data-ttu-id="97d0e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="97d0e-122">Requirement</span></span> | <span data-ttu-id="97d0e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="97d0e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="97d0e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97d0e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97d0e-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="97d0e-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="97d0e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97d0e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97d0e-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="97d0e-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="97d0e-128">Header</span><span class="sxs-lookup"><span data-stu-id="97d0e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="97d0e-129"><dt>Инкрендерер. h</dt></span><span class="sxs-lookup"><span data-stu-id="97d0e-129"><dt>Inkrenderer.h</dt></span></span> </dl>   |
| <span data-ttu-id="97d0e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="97d0e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97d0e-131"><dt>Инкрендерер. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97d0e-131"><dt>Inkrenderer.idl</dt></span></span> </dl> |
| <span data-ttu-id="97d0e-132">IID</span><span class="sxs-lookup"><span data-stu-id="97d0e-132">IID</span></span><br/>                      | <span data-ttu-id="97d0e-133">IID \_ IInkD2DRenderer определен как 4044e60c-7b01-4671-a97c-04e0210a07a5</span><span class="sxs-lookup"><span data-stu-id="97d0e-133">IID\_IInkD2DRenderer is defined as 4044e60c-7b01-4671-a97c-04e0210a07a5</span></span><br/>         |

## <a name="related-topics"></a><span data-ttu-id="97d0e-134">См. также</span><span class="sxs-lookup"><span data-stu-id="97d0e-134">Related topics</span></span>

<span data-ttu-id="97d0e-135">Модуль [подготовки рукописного ввода](ink-renderer.md), [перо и](/windows/uwp/design/input/pen-and-stylus-interactions)перо, [Пример "анализ рукописного ввода](/samples/microsoft/windows-universal-samples/inkanalysis/)", [простой пример](/samples/microsoft/windows-universal-samples/simpleink/)с рукописным вводом, [Пример сложной](/samples/microsoft/windows-universal-samples/complexink/) формы</span><span class="sxs-lookup"><span data-stu-id="97d0e-135">[Ink renderer](ink-renderer.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
