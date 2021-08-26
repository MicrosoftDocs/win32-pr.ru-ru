---
title: Общие сведения о DWriteCore
description: двритекоре — это DirectWrite реализация пакета SDK для приложений Windows.
keywords:
- DirectWrite Центральный
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: bfa23ef41ac2de77901f8601fa0a68f650730403e4dc0bee2f9bbf69d6e1bc9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902883"
---
# <a name="dwritecore-overview"></a>Общие сведения о DWriteCore

двритекоре — это [Windows реализация пакета SDK для приложений](/windows/apps/windows-app-sdk/) [DirectWrite](./direct-write-portal.md) (DirectWrite является API DirectX для высококачественной отрисовки текста, независимыми от разрешения шрифтов, а также полной поддержкой текста и макета в юникоде). двритекоре — это форма DirectWrite, которая работает в версиях Windows Windows 10, версия 1809 (10,0; Сборка 17763) и открывает дверцу для использования кросс-платформенной платформы.

В этом вводном разделе описывается, что такое Двритекоре, и показано, как установить его в среду разработки и программировать вместе с ней.

> [!TIP]
> Описание и ссылки на компоненты DirectX в активной разработке см. на [странице размещения DirectX](https://devblogs.microsoft.com/directx/landing-page/)в записи блога.

## <a name="the-value-proposition-of-dwritecore"></a>Ценность Двритекоре

сам по себе [DirectWrite](./direct-write-portal.md) поддерживает обширный набор функций, который делает его средством визуализации шрифтов, которое выбирается в Windows для большинства приложений, &mdash; будь это через прямые вызовы или через [Direct2D](../direct2d/direct2d-portal.md). DirectWrite содержит независимую от устройства систему разметки текста, высококачественную подсистему [Microsoft ClearType](/typography/cleartype/) text rendering, текст с аппаратным ускорением, многоформатный текст, расширенные функции оформления [OpenType®](/typography/opentype/) , языковую поддержку и макет и отрисовку, совместимые с [GDI](../gdi/windows-gdi.md). DirectWrite был доступен с момента выпуска Windows Vista с пакетом обновления 2 (SP2), а также в течение нескольких лет, чтобы включить более сложные функции, такие как переменные шрифты, позволяющие применять стили, веса и другие атрибуты к шрифту с одним ресурсом шрифта.

однако из-за длительного времени существования DirectWrite в разработке были внесены старые версии Windows. кроме того, состояние DirectWrite в качестве технологии отрисовки текста уровня premier ограничено только Windows, то есть межплатформенные приложения должны либо писать собственный стек для отрисовки текста, либо полагаться на сторонние решения.

Двритекоре решает фундаментальные проблемы, связанные с признаком версии и межплатформенной совместимостью, удаляя библиотеку из системы и нацеливание на все возможные Поддерживаемые конечные точки. для этого мы интегрированы двритекоре в пакет SDK для приложений Windows.

основное значение, которое двритекоре предоставляет разработчику в качестве разработчика в пакете SDK для приложений Windows, заключается в том, что он предоставляет доступ ко многим (и, в конечном итоге, всем) DirectWrite функциям. Все функции Двритекоре будут работать одинаково во всех версиях нижнего уровня без какого-либо нарушения связи с тем, какие функции могут работать с этими версиями.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>Демонстрационное приложение Двритекоре &mdash; двритекорегаллери

Двритекоре демонстрируется в примере приложения [двритекорегаллери](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) , которое доступно для загрузки и изучения.

## <a name="get-started-with-dwritecore"></a>Начало работы с Двритекоре

двритекоре входит в состав [пакета SDK для приложений Windows 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0). В этом разделе описывается настройка среды разработки для программирования с помощью Двритекоре.

### <a name="install-the-windows-app-sdk-08-vsix"></a>установка пакета SDK для Windows приложений 0,8 VSIX

в Visual Studio щелкните **расширения**  >  **управление расширениями**, найдите *пакет sdk для Windows приложений* и скачайте расширение пакета sdk для приложений Windows. закройте и снова откройте Visual Studio и следуйте инструкциям по установке расширения.

дополнительные сведения см. в разделе [Windows пакет SDK для приложений 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) и [настройка среды разработки](/windows/apps/windows-app-sdk/set-up-your-development-environment#3-install-the-windows-app-sdk-extension-for-visual-studio).

### <a name="create-a-new-project"></a>Создание нового проекта

в Visual Studio создайте новый проект из шаблона проекта **пустое приложение, упакованное (винуи 3 в рабочем столе)** . Чтобы найти шаблон проекта, выберите язык: *C++*. platform: *пакет SDK для Windows приложений*; Тип проекта: *Рабочий стол*.

дополнительные сведения см. в разделе [шаблоны Project для винуи 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>установка пакета NuGet Microsoft. прожектреунион. дврите

в Visual Studio щелкните **Project** \> **управление пакетами NuGet...** \> **обзор**, введите или вставьте **Microsoft. прожектреунион. дврите** в поле поиска, выберите элемент в результатах поиска, а затем нажмите кнопку **установить** , чтобы установить пакет для этого проекта.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>Кроме того, начнем с примера приложения Двритекорегаллери.

Кроме того, можно программировать с помощью Двритекоре, начиная с проекта примера приложения [двритекорегаллери](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) , и основывать разработку на этом проекте. После этого можно удалить любой существующий исходный код (или файлы) из этого примера проекта, а также добавить в проект новый исходный код (или файлы).

### <a name="use-dwritecore-in-your-project"></a>Использование Двритекоре в проекте

Дополнительные сведения о программировании с помощью Двритекоре см. в подразделе [программирование с помощью двритекоре](#programming-with-dwritecore) далее в этом разделе.

## <a name="the-release-phases-of-dwritecore"></a>Фазы выпуска Двритекоре

перенос DirectWrite в двритекоре — достаточно большой проект, охватывающий несколько Windows циклов выпусков. Этот проект делится на этапы, каждый из которых соответствует блоку функциональности, предоставленному в выпуске.

### <a name="features-in-the-current-release-of-dwritecore"></a>Функции в текущем выпуске Двритекоре

версия двритекоре, доступная в настоящее время, входит в состав [пакета SDK для приложений Windows 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0). Он содержит основные инструменты, которые вы, как разработчик, должны использовать Двритекоре, включая следующие функции.

- Перечисление шрифтов.
- API шрифтов.
- Упростить.
- API-интерфейсы низкого уровня отрисовки. Это частично на текущем этапе &mdash; двритекоре не взаимодействуют с [Direct2D](../direct2d/direct2d-portal.md), но можно использовать [**идвритеглифрунаналисис**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) и [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).
- Основные функции макета текста.
- Интерфейсы API отрисовки текста.
- Целевой объект прорисовки битовой карты.
- Цветовые шрифты.
- Различные оптимизации (очистка кэша шрифта, загрузчик шрифтов в памяти и т. д.).
- Поддержка подчеркивания &mdash; см. в разделе [**идвритетекстлайаут:: Черкивания**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) и [**идвритетекстлайаут:: сетундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline).
- Поддержка зачеркнутый &mdash; см. в разделе [**идвритетекстлайаут:: зачеркнуть**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getstrikethrough) и [**идвритетекстлайаут:: сетстрикесраугх**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setstrikethrough).
- Поддержка вертикального текста с помощью [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) &mdash; см. в разделе [вертикальный текст](/windows/win32/directwrite/vertical-text).
- Реализуются все методы интерфейсов [**идвритетекстанализер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) и [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) .

Баннер — это цветовые шрифты. Цветовые шрифты позволяют отображать шрифты с более сложными цветовыми возможностями, чем простые одиночные цвета. например, цветовые шрифты заключаются в возможности отображения шрифтов эмодзи и значков панели инструментов (второй из которых используется Office, например). цветовые шрифты впервые появились в Windows 8.1, но функция была значительно расширена в Windows 10, версии 1607 (годовщина обновления).

Работа по очистке кэша шрифтов и загрузчику шрифтов в памяти позволяет ускорить загрузку шрифтов и улучшения памяти.

с помощью этих функций можно сразу приступить к работе с некоторыми современными основными функциями DirectWrite, &mdash; такими как переменные шрифты. переменные шрифты являются одной из наиболее важных функций для DirectWrite клиентов.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>наше приглашение в качестве разработчика DirectWrite

двритекоре, а также другие компоненты пакета SDK для приложений Windows, будут разработаны с открытой откликом для разработчиков. мы приглашаем вас начать исследование двритекоре, а также предоставить ценные сведения или запросы на разработку функций в [GitHub репозитории пакета SDK для приложений Windows](https://github.com/microsoft/ProjectReunion/).

## <a name="programming-with-dwritecore"></a>Программирование с помощью Двритекоре

как и в случае с [DirectWrite](./direct-write-portal.md), вы двритекоре с помощью API-интерфейса COM через интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

Чтобы использовать Двритекоре, необходимо включить `dwrite_core.h` заголовочный файл.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

`dwrite_core.h`Сначала файл заголовка определяет маркер *DWRITE_CORE*, а затем включает `dwrite_3.h` файл заголовка. маркер *DWRITE_CORE* важен, так как он направляет все последующие включенные заголовки, чтобы сделать доступными все DirectWrite api. После включения проекта `dwrite_core.h` можно выполнить написание кода, сборку и запуск.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>Новые или разные API для Двритекоре

Поверхность API Двритекоре в основном такая же, как и для [DirectWrite](/windows/win32/api/_directwrite/). Но существует небольшое количество новых API, которые доступны только в Двритекоре.

#### <a name="create-a-factory-object"></a>Создание объекта фабрики

Функция [**двритекорекреатефактори**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) Free создает объект фабрики, который используется для последующего создания отдельных объектов двритекоре.

**Двритекорекреатефактори** функционирует так же, как функция [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , экспортируемая системной версией DirectWrite. Функция Двритекоре имеет другое имя, чтобы избежать неоднозначности.

#### <a name="create-a-restricted-factory-object"></a>Создание объекта ограниченной фабрики

Перечисление [**DWRITE_FACTORY_TYPE**](/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type) содержит новую константную &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, обозначающую ограниченную фабрику. Ограниченная фабрика больше заблокирована, чем изолированная фабрика. Он не взаимодействует с межпроцессным или постоянным кэшем шрифтов каким-либо образом. Кроме того, системная коллекция шрифтов, возвращаемая из этой фабрики, включает только хорошо известные шрифты. Ниже показано, как можно использовать **DWRITE_FACTORY_TYPE_ISOLATED2** для создания объекта ограниченной фабрики при вызове функции Free [**двритекорекреатефактори**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) .

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

при передаче **DWRITE_FACTORY_TYPE_ISOLATED2** в более старую версию DirectWrite, которая не поддерживается, **двритекреатефактори** возвращает **E_INVALIDARG**.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Рисование глифов в битовой карте системной памяти

DirectWrite имеет целевой интерфейс прорисовки изображения, который поддерживает отображение глифов в битовую карту в системной памяти. Однако в настоящее время единственный способ получить доступ к базовым данным о пикселях — использовать GDI, поэтому API не может использоваться на разных платформах. Это легко исправлено, добавив метод для получения данных о точках.

Поэтому Двритекоре вводит интерфейс [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata) и его метод [**IDWriteBitmapRenderTarget2::**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata). Этот метод принимает параметр типа (указатель на) [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32), который является новой структурой.

Приложение создает целевой объект прорисовки растрового изображения путем вызова [идвритегдиинтероп:: креатебитмапрендертаржет](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). в Windows целевой объект отрисовки растрового изображения инкапсулирует контроллер домена памяти gdi с выбранным в нем точечным рисунком gdi (dib). [Идвритебитмапрендертаржет::D равглифрун](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) преобразует глифы в DIB. DirectWrite отображает сами глифы без помощи GDI. Приложение может получить **HDC** из целевого объекта прорисовки растрового изображения и использовать [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) для копирования пикселов в окно **HDC**.

на платформах, отличных от Windows, приложение по-прежнему может создавать целевой объект прорисовки битовой карты, но он просто инкапсулирует массив системной памяти без **HDC** и не имеет DIB. Без **HDC** для приложения должен быть другим способом получения пикселей точечного рисунка, чтобы он мог скопировать их, или иным образом использовать их. Даже в Windows, иногда бывает полезно получить фактические данные о пикселях, и мы покажем текущий способ сделать это в приведенном ниже примере кода.

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Другие различия API между Двритекоре и DirectWrite

существует несколько интерфейсов api, которые являются заглушками, или они работают несколько иначе на платформах, отличных от Windows. например, [идвритегдиинтероп:: креатефонтфацефромхдк](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) возвращает **E_NOTIMPL** на платформах, отличных от Windows, так как не существует такого объекта, как **HDC** без [GDI](../gdi/windows-gdi.md).

и, наконец, существуют некоторые другие Windows интерфейсы api, которые обычно используются вместе с DirectWrite (Direct2D является важным примером). Однако в настоящее время Direct2D и Двритекоре не взаимодействуют. Например, если создать [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью двритекоре и передать его в [**D2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), то вызов завершится ошибкой.
