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
ms.openlocfilehash: 51383770b8eb0c5dca5efbb5f1756bee81ece506c0e92337e9df9a60eb0a8aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726734"
---
# <a name="inkd2drenderer-class"></a>Класс InkD2DRenderer

Реализует интерфейс [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .

объект [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) обеспечивает отрисовку рукописных штрихов в назначенном Direct2Dном контексте устройства универсального Windowsного приложения вместо элемента управления [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) по умолчанию.

## <a name="members"></a>Элементы

Класс **InkD2DRenderer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkD2DRenderer** также имеет следующие типы членов:

- [Методы](#methods)

### <a name="methods"></a>Методы

Класс **InkD2DRenderer** содержит следующие методы.

| Метод                              | Описание                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Преобразует рукописный штрих в назначенный контекст устройства Direct2D приложения.<br/> |

## <a name="creationaccess-functions"></a>\\Функции доступа для создания

Вызовите [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса <strong>InkD2DRenderer</strong> , чтобы получить ссылку на объект.

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Примеры

Этот фрагмент кода из файла "Сценекомпосер. cpp" в [примере сложного](/samples/microsoft/windows-universal-samples/complexink/) рукописного ввода демонстрирует отрисовку коллекции рукописных штрихов в контексте устройства Direct2D.

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

В этом фрагменте кода из файла "Инкрендерер. cpp" в [образце сложных рукописных](/samples/microsoft/windows-universal-samples/complexink/) данных показан метод Render (вызванный в предыдущем фрагменте), который вызывает метод [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) для отрисовки штрихов.

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

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                  |
| Заголовок<br/>                   | <dl> <dt>Инкрендерер. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Инкрендерер. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer определен как 4044e60c-7b01-4671-a97c-04e0210a07a5<br/>         |

## <a name="related-topics"></a>Связанные темы

Модуль [подготовки рукописного ввода](ink-renderer.md), [перо и](/windows/uwp/design/input/pen-and-stylus-interactions)перо, [Пример "анализ рукописного ввода](/samples/microsoft/windows-universal-samples/inkanalysis/)", [простой пример](/samples/microsoft/windows-universal-samples/simpleink/)с рукописным вводом, [Пример сложной](/samples/microsoft/windows-universal-samples/complexink/) формы
