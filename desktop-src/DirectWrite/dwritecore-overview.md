---
title: Общие сведения о DWriteCore
description: Двритекоре — это реализация DirectWrite пакета SDK для приложений Windows.
keywords:
- Ядро DirectWrite
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: a537d26f6aca4e2be64b61fd41da91e1f8829894
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587773"
---
# <a name="dwritecore-overview"></a>Общие сведения о DWriteCore

Двритекоре — это реализация [DirectWrite](./direct-write-portal.md) [пакета SDK для приложений Windows](/windows/apps/windows-app-sdk/) (DirectWrite — это API DirectX для высококачественной отрисовки текста, независимых от разрешения шрифтов, а также полная поддержка текста и макета в Юникоде). Двритекоре — это форма DirectWrite, которая работает в версиях Windows до Windows 10, версия 1809 (10,0; Сборка 17763) и открывает дверцу для использования кросс-платформенной платформы.

В этом вводном разделе описывается, что такое Двритекоре, и показано, как установить его в среду разработки и программировать вместе с ней.

> [!TIP]
> Описание и ссылки на компоненты DirectX в активной разработке см. на [странице размещения DirectX](https://devblogs.microsoft.com/directx/landing-page/)в записи блога.

## <a name="the-value-proposition-of-dwritecore"></a>Ценность Двритекоре

Сам по себе [DirectWrite](./direct-write-portal.md) поддерживает обширный набор функций, который делает его средством визуализации шрифтов в Windows для большинства приложений, &mdash; будь это через прямые вызовы или через [Direct2D](../direct2d/direct2d-portal.md). DirectWrite содержит независимую от устройства систему разметки текста, высококачественную подсистему [Microsoft ClearType](/typography/cleartype/) Text Rendering, текст с аппаратным ускорением, многоформатный текст, расширенные функции оформления [OpenType®](/typography/opentype/) , языковую поддержку и макет и отрисовку, совместимые с [GDI](../gdi/windows-gdi.md). DirectWrite был доступен с момента выпуска пакета обновления 2 (SP2) для Windows Vista и был изменен в течение нескольких лет для включения более сложных функций, таких как переменные шрифты, которые позволяют применять стили, весовые коэффициенты и другие атрибуты к шрифту с одним ресурсом шрифта.

Однако из-за длительного времени существования DirectWrite усовершенствования в разработке приходили бы оставлять старые версии Windows. Кроме того, состояние DirectWrite в качестве технологии отрисовки текста уровня Premier ограничено только Windows, в результате чего межплатформенные приложения должны либо записывать собственный стек отрисовки текста, либо полагаться на сторонние решения.

Двритекоре решает фундаментальные проблемы, связанные с признаком версии и межплатформенной совместимостью, удаляя библиотеку из системы и нацеливание на все возможные Поддерживаемые конечные точки. Для этого мы интегрированы Двритекоре в пакет SDK для приложений Windows.

Основное значение, которое Двритекоре предоставляет разработчику в пакете SDK для приложений Windows, заключается в том, что он предоставляет доступ ко многим (и, в конечном итоге, всем) функциям DirectWrite. Все функции Двритекоре будут работать одинаково во всех версиях нижнего уровня без какого-либо нарушения связи с тем, какие функции могут работать с этими версиями.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>Демонстрационное приложение Двритекоре &mdash; двритекорегаллери

Двритекоре демонстрируется в примере приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , которое доступно для загрузки и изучения.

## <a name="get-started-with-dwritecore"></a>Начало работы с Двритекоре

Двритекоре является частью [пакета SDK для приложений Windows 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0). В этом разделе описывается настройка среды разработки для программирования с помощью Двритекоре.

### <a name="install-the-windows-app-sdk-08-vsix"></a>Установка пакета SDK для приложений Windows 0,8 VSIX

В Visual Studio щелкните **расширения**  >  **Управление расширениями**, найдите *пакет SDK для приложений Windows* и скачайте расширение пакета SDK для приложений Windows. Закройте и снова откройте Visual Studio и следуйте инструкциям по установке расширения.

Дополнительные сведения см. в статье [пакет SDK для приложений Windows 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) и [Настройка среды разработки](/windows/apps/windows-app-sdk/set-up-your-development-environment#3-install-the-windows-app-sdk-extension-for-visual-studio).

### <a name="create-a-new-project"></a>Создание нового проекта

В Visual Studio создайте новый проект из шаблона проекта " **пустое приложение", упакованное (винуи 3 в рабочем столе)** . Чтобы найти шаблон проекта, выберите язык: *C++*. Platform: *пакет SDK для приложений Windows*; Тип проекта: *Рабочий стол*.

Дополнительные сведения см. в разделе [шаблоны проектов для винуи 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>Установка пакета NuGet Microsoft. Прожектреунион. Дврите

В Visual Studio щелкните **проект** \> **Управление пакетами NuGet...** \> **Обзор**, введите или вставьте **Microsoft. прожектреунион. дврите** в поле поиска, выберите элемент в результатах поиска и нажмите кнопку **установить** , чтобы установить пакет для этого проекта.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>Кроме того, начнем с примера приложения Двритекорегаллери.

Кроме того, можно программировать с помощью Двритекоре, начиная с проекта примера приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , и основывать разработку на этом проекте. После этого можно удалить любой существующий исходный код (или файлы) из этого примера проекта, а также добавить в проект новый исходный код (или файлы).

### <a name="use-dwritecore-in-your-project"></a>Использование Двритекоре в проекте

Дополнительные сведения о программировании с помощью Двритекоре см. в подразделе [программирование с помощью двритекоре](#programming-with-dwritecore) далее в этом разделе.

## <a name="the-release-phases-of-dwritecore"></a>Фазы выпуска Двритекоре

Перенос DirectWrite в Двритекоре является достаточно большим проектом, охватывающим несколько циклов выпуска Windows. Этот проект делится на этапы, каждый из которых соответствует блоку функциональности, предоставленному в выпуске.

### <a name="features-in-the-current-release-of-dwritecore"></a>Функции в текущем выпуске Двритекоре

Версия Двритекоре, доступная в настоящее время, является частью [пакета SDK для приложений Windows 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0). Он содержит основные инструменты, которые вы, как разработчик, должны использовать Двритекоре, включая следующие функции.

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

Баннер — это цветовые шрифты. Цветовые шрифты позволяют отображать шрифты с более сложными цветовыми возможностями, чем простые одиночные цвета. Например, цветовые шрифты определяют возможность отображения шрифтов эмодзи и значков панели инструментов (второй из которых используется в Office, например). Цветовые шрифты впервые появились в Windows 8.1, но эта функция была в значительной степени расширена в Windows 10, версии 1607 (годовщина обновления).

Работа по очистке кэша шрифтов и загрузчику шрифтов в памяти позволяет ускорить загрузку шрифтов и улучшения памяти.

С помощью этих функций можно сразу приступить к работе с некоторыми современными основными функциями DirectWrite, &mdash; такими как переменные шрифты. Переменные шрифты являются одной из наиболее важных функций для клиентов DirectWrite.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Наше приглашение в качестве разработчика DirectWrite

Двритекоре, наряду с другими компонентами пакета SDK для приложений Windows, будет разрабатываться с открытой откликом для разработчиков. Мы приглашаем вас начать изучать Двритекоре, а также предоставить ценные сведения или запросы на разработку функций в [репозитории GitHub пакета SDK для приложений Windows](https://github.com/microsoft/ProjectReunion/).

## <a name="programming-with-dwritecore"></a>Программирование с помощью Двритекоре

Как и в случае с [DirectWrite](./direct-write-portal.md), вы запрограммироване с помощью двритекоре с помощью API-интерфейса COM через интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

Чтобы использовать Двритекоре, необходимо включить `dwrite_core.h` заголовочный файл.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

`dwrite_core.h`Сначала файл заголовка определяет маркер *DWRITE_CORE*, а затем включает `dwrite_3.h` файл заголовка. Маркер *DWRITE_CORE* важен, так как он направляет все последующие включенные заголовки, чтобы сделать доступными все API-интерфейсы DirectWrite. После включения проекта `dwrite_core.h` можно выполнить написание кода, сборку и запуск.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>Новые или разные API для Двритекоре

Поверхность API Двритекоре в основном та же самая, что и для [DirectWrite](/windows/win32/api/_directwrite/). Но существует небольшое количество новых API, которые доступны только в Двритекоре.

#### <a name="create-a-factory-object"></a>Создание объекта фабрики

Функция [**двритекорекреатефактори**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) Free создает объект фабрики, который используется для последующего создания отдельных объектов двритекоре.

**Двритекорекреатефактори** функционально совпадает с функцией [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , экспортируемой с помощью системной версии DirectWrite. Функция Двритекоре имеет другое имя, чтобы избежать неоднозначности.

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

При передаче **DWRITE_FACTORY_TYPE_ISOLATED2** в более старую версию DirectWrite, которая не поддерживается, **двритекреатефактори** возвращает **E_INVALIDARG**.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Рисование глифов в битовой карте системной памяти

DirectWrite имеет целевой интерфейс прорисовки растрового изображения, который поддерживает отображение глифов в битовую карту в системной памяти. Однако в настоящее время единственный способ получить доступ к базовым данным о пикселях — использовать GDI, поэтому API не может использоваться на разных платформах. Это легко исправлено, добавив метод для получения данных о точках.

Поэтому Двритекоре вводит интерфейс [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata) и его метод [**IDWriteBitmapRenderTarget2::**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata). Этот метод принимает параметр типа (указатель на) [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32), который является новой структурой.

Приложение создает целевой объект прорисовки растрового изображения путем вызова [идвритегдиинтероп:: креатебитмапрендертаржет](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). В Windows целевой объект прорисовки растрового изображения инкапсулирует контроллер домена памяти GDI с выбранным в него точечным рисунком GDI (DIB). [Идвритебитмапрендертаржет::D равглифрун](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) преобразует глифы в DIB. DirectWrite отображает сами глифы без помощи GDI. Приложение может получить **HDC** из целевого объекта прорисовки растрового изображения и использовать [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) для копирования пикселов в окно **HDC**.

На платформах, отличных от Windows, приложение по-прежнему может создавать целевой объект прорисовки битовой карты, но он просто Инкапсулирует массив системной памяти без **HDC** и не имеет DIB. Без **HDC** для приложения должен быть другим способом получения пикселей точечного рисунка, чтобы он мог скопировать их, или иным образом использовать их. Даже в Windows иногда бывает полезно получить фактические данные о пикселях, и мы покажем текущий способ сделать это в приведенном ниже примере кода.

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

Существует несколько интерфейсов API, являющихся только заглушками, или они работают несколько иначе на платформах, отличных от Windows. Например, [идвритегдиинтероп:: креатефонтфацефромхдк](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) возвращает **E_NOTIMPL** на платформах, отличных от Windows, поскольку параметр **HDC** без [GDI](../gdi/windows-gdi.md)отсутствует.

И, наконец, существуют некоторые другие API Windows, которые обычно используются вместе с DirectWrite (Direct2D является важным примером). Однако в настоящее время Direct2D и Двритекоре не взаимодействуют. Например, если создать [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью двритекоре и передать его в [**D2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), то вызов завершится ошибкой.
