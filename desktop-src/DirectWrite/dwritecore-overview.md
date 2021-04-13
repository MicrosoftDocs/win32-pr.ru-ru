---
title: Общие сведения о DWriteCore
description: Двритекоре — это реализация DirectWrite для Реюньон проекта.
keywords:
- Ядро DirectWrite
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351035"
---
# <a name="dwritecore-overview"></a>Общие сведения о DWriteCore

Двритекоре — это реализация [DirectWrite](./direct-write-portal.md)для [Реюньон проекта](/windows/apps/project-reunion/) . DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.

В этом вводном разделе описывается, что такое Двритекоре, и показано, как установить его в среду разработки и программировать вместе с ней.

## <a name="the-value-proposition-of-dwritecore"></a>Ценность Двритекоре

Сам по себе [DirectWrite](./direct-write-portal.md) поддерживает обширный набор функций, который делает его средством визуализации шрифтов в Windows для большинства приложений, &mdash; будь это через прямые вызовы или через [Direct2D](../direct2d/direct2d-portal.md). DirectWrite содержит независимую от устройства систему разметки текста, высококачественную подсистему [Microsoft ClearType](/typography/cleartype/) Text Rendering, текст с аппаратным ускорением, многоформатный текст, расширенные функции оформления [OpenType®](/typography/opentype/) , языковую поддержку и макет и отрисовку, совместимые с [GDI](../gdi/windows-gdi.md). DirectWrite был доступен с момента выпуска пакета обновления 2 (SP2) для Windows Vista и был изменен в течение нескольких лет для включения более сложных функций, таких как переменные шрифты, позволяющие разработчикам применять стили, веса и другие атрибуты к шрифту с одним ресурсом шрифта.

Однако из-за длительного времени существования DirectWrite усовершенствования в разработке приходили бы оставлять старые версии Windows. Кроме того, состояние DirectWrite в качестве технологии отрисовки текста уровня Premier ограничено только Windows, в результате чего межплатформенные приложения должны либо записывать собственный стек отрисовки текста, либо полагаться на сторонние решения.

Двритекоре решает фундаментальные проблемы, связанные с признаком версии и межплатформенной совместимостью, удаляя библиотеку из системы и нацеливание на все возможные Поддерживаемые конечные точки. В конце концов, мы интегрированы в проект Двритекоре с общедоступным API, который поддерживается на всех конечных точках Windows до Windows 8, и открывает дверцу для использования кросс-платформенной платформы.

Основное значение, которое Двритекоре предоставляет разработчику в качестве разработчика, — это то, что оно предоставляет доступ ко всем текущим DirectWrite функциям на всех уровнях до Windows 8. Все функции Двритекоре будут работать одинаково для всех версий нижнего уровня; другими словами, все текущие функции будут работать в Windows 8, 8,1 и всех версиях Windows 10 без каких бы то ни было ошибок, касающихся того, какие функции могут работать с какими версиями.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>Демонстрационное приложение Двритекоре &mdash; двритекорегаллери

Двритекоре демонстрируется в примере приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , которое доступно для загрузки и изучения.

## <a name="get-started-with-dwritecore"></a>Начало работы с Двритекоре

В настоящее время в предварительном выпуске Project Реюньон 0,1 мы не поддерживаем установку пакета NuGet для повторного объединения проектов в собственные проекты. Вместо этого в настоящее время поддерживается возможность собственного программирования с помощью Двритекоре, которая начинается с проекта [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) Sample App и основывается на разработке проекта.

После этого можно удалить любой существующий исходный код (или файлы) из этого примера проекта, а также добавить в проект новый исходный код (или файлы). Дополнительные сведения о программировании с помощью Двритекоре см. в подразделе [программирование с помощью двритекоре](#programming-with-dwritecore) далее в этом разделе.

## <a name="the-release-phases-of-dwritecore"></a>Фазы выпуска Двритекоре

Перенос DirectWrite в Двритекоре является достаточно большим проектом, охватывающим несколько циклов выпуска Windows. Этот проект делится на этапы, каждый из которых соответствует блоку функциональности, предоставленному в выпуске.

### <a name="features-in-the-current-release-of-dwritecore"></a>Функции в текущем выпуске Двритекоре

Версия Двритекоре, доступная в настоящее время, содержит базовые инструменты, которые вы, как разработчик, должны использовать Двритекоре, включая следующие функции.

- Перечисление шрифтов.
- API шрифтов.
- Упростить.
- API-интерфейсы низкого уровня отрисовки. Это частично на текущем этапе &mdash; двритекоре не взаимодействуют с [Direct2D](../direct2d/direct2d-portal.md), но можно использовать [**идвритеглифрунаналисис**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) и [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).
- Основные функции макета текста.
- Интерфейсы API отрисовки текста.
- Целевой объект прорисовки битовой карты.
- Цветовые шрифты.
- Различные оптимизации (очистка кэша шрифта, загрузчик шрифтов в памяти и т. д.).

Баннер на этом этапе — цветовые шрифты. Цветовые шрифты позволяют отображать шрифты с более сложными цветовыми возможностями, чем простые одиночные цвета. Например, цветовые шрифты определяют возможность отображения шрифтов эмодзи и значков панели инструментов (второй из которых используется в Office, например). Цветовые шрифты впервые появились в Windows 8.1, но эта функция была в значительной степени расширена в Windows 10, версии 1607 (годовщина обновления).

Работа по очистке кэша шрифтов и загрузчику шрифтов в памяти позволяет ускорить загрузку шрифтов и улучшения памяти.

С помощью этих функций можно сразу приступить к работе с некоторыми современными основными функциями DirectWrite, &mdash; такими как переменные шрифты &mdash; нижнего уровня до Windows 8. Эту итерацию библиотеки также можно использовать в [Android](https://www.android.com/)и **Linux**. Переменные шрифты являются одной из наиболее важных функций для клиентов DirectWrite. они появились в Windows 10, версия 1709 (обновления для авторов обновлений), поэтому доступ к ним в предыдущих версиях является огромным boonом для разработчика.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Наше приглашение в качестве разработчика DirectWrite

Двритекоре, а также другие компоненты для повторного объединения проектов, будут разработаны с открытой откликом для разработчиков. Мы приглашаем вас начать изучать Двритекоре, а также предоставить подробные сведения или запросы на разработку функций в нашем [репозитории GitHub](https://github.com/microsoft/ProjectReunion/)для нашего проекта.

## <a name="programming-with-dwritecore"></a>Программирование с помощью Двритекоре

Как уже упоминалось, в предварительном выпуске Project Реюньон 0,1 параметр, поддерживаемый в настоящее время для собственного программирования с помощью Двритекоре, начинается с проекта [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) Sample App.

Как и в случае с [DirectWrite](./direct-write-portal.md), вы запрограммироване с помощью двритекоре с помощью API-интерфейса COM через интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

**Двритекорегаллери** уже включает `dwrite_core.h` файл заголовка. Этот заголовок сначала определяет маркер *DWRITE_CORE*, а затем включает `dwrite_3.h` . Маркер *DWRITE_CORE* важен, так как он направляет все последующие включенные заголовки, чтобы сделать доступными все API-интерфейсы DirectWrite. После включения проекта `dwrite_core.h` можно выполнить написание кода, сборку и запуск.

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>Новые или разные API для Двритекоре

Поверхность API Двритекоре в основном та же самая, что и для [DirectWrite](/windows/win32/api/_directwrite/). Но существует небольшое количество новых API, которые доступны только в Двритекоре.

#### <a name="create-a-restricted-factory-object"></a>Создание объекта ограниченной фабрики

Перечисление [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) содержит новую константную &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED**. Ограниченная фабрика больше заблокирована, чем изолированная фабрика. Он не взаимодействует с межпроцессным или постоянным кэшем шрифтов каким-либо образом. Кроме того, системная коллекция шрифтов, возвращаемая из этой фабрики, включает только хорошо известные шрифты. Ниже показано, как можно использовать **DWRITE_FACTORY_TYPE_RESTRICTED** для создания объекта ограниченной фабрики при вызове функции Free [**двритекреатефактори**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

При передаче **DWRITE_FACTORY_TYPE_RESTRICTED** в более старую версию DirectWrite, которая не поддерживается, **двритекреатефактори** возвращает **E_INVALIDARG**.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Рисование глифов в битовой карте системной памяти

DirectWrite имеет целевой интерфейс прорисовки растрового изображения, который поддерживает отображение глифов в битовую карту в системной памяти. Однако в настоящее время единственный способ получить доступ к базовым данным о пикселях — использовать GDI, поэтому API не может использоваться на разных платформах. Это легко исправлено, добавив метод для получения данных о точках.

Поэтому Двритекоре вводит интерфейс [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) и его метод [**IDWriteBitmapRenderTarget2::**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md). Этот метод принимает параметр типа (указатель на) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), который является новой структурой.

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