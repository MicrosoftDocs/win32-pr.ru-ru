---
title: Использование DirectX с дисплеями с широким динамическим диапазоном и расширенным управлением цветами
description: В этом разделе представлен технический обзор визуализации содержимого Direct3D 11 и Direct3D 12 с высоким динамическим диапазоном на HDR10 дисплеи с помощью расширенной поддержки цветов Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104558900"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a>Использование DirectX с высоким динамическим отображением диапазона и расширенным цветом

В этом разделе представлен технический обзор содержимого Direct3D 11 и Direct3D 12 с высоким динамическим диапазоном (HDR) на HDR10 дисплее с помощью расширенной поддержки цветов Windows 10. В нем приведены основные концептуальные различия между выводом в HDR10 в сравнении с отображаемыми традиционными стандартными динамическими диапазонами (SDR). Он также охватывает ключевые технические требования для приложения, чтобы обеспечить правильную поддержку расширенного цвета Windows, а также рекомендации и рекомендации.

## <a name="introduction"></a>Введение

Windows 10 поддерживает HDR и другие расширенные экраны цвета, которые обеспечивают значительно более высокую качество цветопередачи по сравнению с традиционными дисплеями SDR. Вы можете использовать Direct3D, Direct2D и другие графические API для отображения HDR-содержимого в пригодном для просмотра виде.

Расширенный цвет Windows относится к нескольким связанным технологиям, впервые представленным в Windows 10 версии 1703, которые обеспечивают поддержку для отображения, превышающих возможности цветового отображения традиционных стандартных динамических диапазонов (SDR). Ниже описаны три основные расширенные возможности. Наиболее распространенный тип расширенного представления цвета, HDR10, поддерживает все три расширенные возможности.

### <a name="high-dynamic-range"></a>Высокий динамический диапазон

Динамический диапазон — это разница между максимальной и минимальной яркостью в сцене; часто это измеряется в НИТС (Канделас на квадратный сантиметр). Реальные сцены, такие как этот закат, часто имеют динамические диапазоны из 10 заказов на величину освещенности. человеческий глаз может назначить еще больший диапазон после адаптации.

![изображение заката с ярко-темными точками в сцене с пометкой](images/HDR-HDR.jpg)

За пререшениями Direct3D 9 обработчики графики могут внутреннно визуализировать свои сцены на уровне физической точности. Однако типичный стандарт динамического отображения диапазона может воспроизводить всего более 3 заказов на степень освещенности, поэтому все содержимое, визуализированное HDR, должно быть тонемаппед (сжато) в ограниченный диапазон отображения. Новые HDR-отображения, в том числе те, которые соответствуют стандарту HDR10 (BT. 2100), нарушают это ограничение.

### <a name="wide-color-gamut-with-automatic-system-color-management"></a>Широкая цветовая палитра с автоматическим управлением системой управления цветом

Цветовая палитра относится к диапазону и насыщенности оттенков, которые может воспроизводить изображение. Самый насыщенный естественный цвет, который может воспринимать человеческим глазом, — чистый, монохромный, например, то, что создается лазером. Однако основная часть отображения потребителей часто может воспроизводить цвета только в пределах палитры sRGB, что представляет примерно 35% всех цветов воспринимаемого. На приведенной ниже схеме представлено представление Спектрал очага или всех цветов воспринимаемого (на определенном уровне освещенности), где маленький треугольник — это цвет sRGB.

![Схема цветового охвата Спектрал очага и sRGB](images/HDR-WCG.jpg)

В верхней части на профессиональном компьютере отображаются длинные поддерживаемые цветовые палитры, которые значительно шире, чем sRGB, например Adobe RGB и D65-P3. И эти широкие экранные палитры становятся более распространенными. Однако до расширенного цвета Windows не выполняло Управление цветом на уровне системы для приложений. Это означало, что при отрисовке приложения DirectX, например чистого красного цвета или RGB (1,0, 0,0, 0,0) в цепочку буферов, Windows будет просто просканировать наиболее насыщенный красный цвет, который может воспроизводить дисплей, независимо от фактической палитры цветов на дисплее.

Приложения, которым требовалась высокая точность цвета, могут запрашивать цветовые возможности экрана (например, с помощью ICC-профилей), а также выполнять собственные функции управления цветом, чтобы правильно ориентироваться в цветовой палитре экрана. Однако подавляющее большинство приложений и визуального содержимого предполагает, что дисплей имеет значение sRGB, и для выполнения этого предположений используются операционные системы.

Расширенный цвет Windows добавляет автоматическое управление цветом на уровне системы. Диспетчер окон рабочего стола (DWM) является компоновщиком Windows. Если включен расширенный цвет, DWM выполняет явное преобразование цвета из колорспаце визуального содержимого приложения в каноническое цветовое пространство композиции, которое является scRGB. Windows, затем цвет преобразует составное содержимое буфера кадров в собственное цветовое пространство экрана. Таким образом, традиционное содержимое sRGB автоматически получает точную цветопередачу, в то время как расширенные приложения, поддерживающие цвета, могут использовать возможности полного цветового представления.

### <a name="deep-precisionbit-depth"></a>Глубокая точность или глубина бита

Числовая точность или битовая глубина означает представление или различение похожих, но различных цветов без чередования и артефактов. Основной компьютер отображает 8 бит на цветовой канал, в то время как человеческий глаз требует не менее 10-12 бит точности, чтобы избежать воспринимаемого искажений, не прибегая к таким методам, как дизеринг или в зависимости от условий просмотра.

![Рисунок Виндмиллс в смоделированных двух битах на цветовой канал и 8 бит на канал](images/HDR-bitdepth.jpg)

До расширенного цвета оконное приложение DWM ограничило вывод содержимого только по 8 битам на цветовой канал, даже если дисплей поддерживает более высокую глубину. Если включен расширенный цвет, DWM выполняет свою композицию с использованием IEEE половинной точности с плавающей запятой (FP16), устраняя узкие места и позволяя использовать полную точность экрана.

## <a name="system-requirements"></a>Требования к системе

### <a name="operating-system-os"></a>Операционная система (ОС)

Расширенная поддержка цветов впервые поставляется с Windows 10, версия 1703 и значительно улучшена при каждом обновлении. В этом разделе предполагается, что ваше приложение предназначено для Windows 10, версии 1903 или более поздней.

### <a name="display"></a>Отображение

Чтобы воспользоваться преимуществами высокого динамического диапазона, необходимо иметь дисплей, поддерживающий стандарт HDR10. Windows лучше работает с дисплеями, [сертифицированными](https://displayhdr.org/)по стандарту VESA дисплайхдр.

### <a name="graphics-processor-gpu"></a>Графический процессор (GPU)

Требуется недавний GPU. Для поддержки HDR10 отображения Windows 10 требуется один из следующих способов.

* NVIDIA GeForce 1000 Series (Pascal) или более поздней версии
* AMD Radeon RX 400 (Поларис) или более поздней версии
* Выбранная серия Intel Core 7 (Каби Lake) или более поздняя версия

Обратите внимание, что в зависимости от сценариев применяются дополнительные требования к оборудованию, включая аппаратное ускорение (10 бит HEVC, 10 бит VP9 и т. д.) и поддержку PlayReady (SL3000). Для получения более подробной информации обратитесь к поставщику GPU.

### <a name="graphics-driver-wddm"></a>Драйвер графики (WDDM)

Самый последний доступный графический драйвер настоятельно рекомендуется в Центр обновления Windows или у поставщика GPU или на веб-сайте производителя ПК. Для Windows 10, версии 1903 и более поздних версий рекомендуется использовать драйверы, поддерживающие по крайней мере Windows (WDDM) версии 2,6.

## <a name="supported-rendering-apis"></a>Поддерживаемые API-интерфейсы подготовки к просмотру

Windows 10 поддерживает разнообразные API-интерфейсы и платформы для подготовки к просмотру. Расширенная поддержка цветов в основном зависит от приложения, которое может выполнять современные презентации с помощью DXGI или API визуального уровня.

* [Графическая инфраструктура DirectX (DXGI)](../direct3ddxgi/dx-graphics-dxgi.md)
* [Визуальный слой (Windows. UI. композиция)](/windows/uwp/composition/visual-layer)

Таким образом, любой API отрисовки, который может выводить в один из этих методов, может поддерживать расширенный цвет. К ним относятся, но не ограничиваются.

* [Direct3D 11](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [Direct3D 12](../direct3d12/direct3d-12-graphics.md)
* [Direct2D](../direct2d/direct2d-portal.md)
* [Win2D](https://github.com/Microsoft/Win2D)
  * Требует использования API-интерфейсов нижнего уровня **канвассвапчаин** или **канвассвапчаинпанел** .
* [**Windows.UI.Input.Inking**](/uwp/api/Windows.UI.Input.Inking)
  * Поддерживает собственную отрисовку рукописного ввода с помощью DirectX.
* [XAML](/windows/uwp/xaml-platform/)
  * Поддерживает воспроизведение HDR-видео с помощью **медиаплайерелемент**.
  * Поддерживает декодирование изображений XR JPEG с помощью элемента **Image** .
  * Поддерживает взаимодействие DirectX с помощью **SwapChainPanel**.

## <a name="handling-dynamic-display-capabilities"></a>Обработка возможностей динамического просмотра

Windows 10 поддерживает огромные разнообразные дисплеи с поддержкой цветов, от эффективных интегрированных панелей до высокопроизводительных игровых мониторов и телевизоров. Пользователи Windows предполагают, что ваше приложение будет беспрепятственно работать со всеми этими вариациями, включая повсеместно существующие экраны SDR.

Windows 10 предоставляет пользователю возможность управлять HDR и расширенными возможностями цвета. Приложение должно определить конфигурацию текущего экрана и динамически реагировать на любые изменения в возможности. Это может произойти по многим причинам, например, если пользователь включил или отключил функцию или переместил приложение между разными дисплеями или изменилось состояние электропитания системы.

### <a name="universal-windows-platform-uwp-apps"></a>Приложения универсальной платформы Windows (UWP)

Если вы создаете приложение UWP, независимо от используемого API графической отрисовки, используйте [**адванцедколоринфо**](/uwp/api/windows.graphics.display.advancedcolorinfo) , чтобы получить возможности отображения. Получите экземпляр **адванцедколоринфо** из [**DisplayInformation:: жетадванцедколоринфо**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).

Чтобы проверить, какой расширенный тип цвета активен в данный момент, используйте свойство [**куррентадванцедколоркинд**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) . В Windows 10 версия 1903 и более поздние версии возвращают одно из трех возможных значений: **SDR**, **ВКГ** или **HDR**. Это наиболее важное свойство, которое необходимо проверить, и вы должны настроить конвейер отрисовки и представления в ответ на активный вид.

Чтобы проверить, какие расширенные виды цветов поддерживаются, но не обязательно являются активными, вызовите [**исадванцедколоркиндаваилабле**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable). Эти сведения можно использовать, например, чтобы запросить у пользователя возможность перехода к приложению "Параметры Windows", чтобы они могли включить HDR или ВКГ.

Другие члены **адванцедколоринфо** предоставляют количественную информацию о том физическом цвете (светимость и чроминанце), соответствующий SMPTE St. 2086 статические метаданные HDR. Эти сведения следует использовать для настройки сопоставления тонемаппинг и цветового охвата приложения.

Чтобы обрабатывались изменения в расширенных возможностях цвета, зарегистрируйте событие [**адванцедколоринфочанжед**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) . Это событие возникает, если любой из причин изменяется любой параметр расширенных возможностей цвета экрана.

Обработайте это событие, получив новый экземпляр **адванцедколоринфо**, и проверив, какие значения были изменены.

### <a name="desktop-win32-directx-apps"></a>Приложения DirectX для Desktop (Win32)

Если вы создаете приложение Win32 и используете DirectX для подготовки к просмотру, используйте [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) , чтобы получить возможности отображения. Получите экземпляр этой структуры с помощью [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).

Чтобы проверить, какой расширенный тип цвета активен в данный момент, используйте свойство **колорспаце** , которое имеет тип [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), и содержит одно из следующих значений:

* **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR
* **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR

> [!Note]
> Другие расширенные типы цветов, например ВКГ, обрабатываются как SDR с помощью DXGI. Вы не можете использовать DXGI для обнаружения ВКГ дисплея.

> [!Note]
> DXGI не позволяет проверить, какие расширенные виды цветов поддерживаются, но не активны в данный момент.

Большинство других членов **DXGI_OUTPUT_DESC1** предоставляют количественную информацию о физическом цветовом томе (светимости и чроминанце) панели, соответствующей статическим МЕТАДАННЫМ SMPTE St. 2086. Эти сведения следует использовать для настройки сопоставления тонемаппинг и цветового охвата приложения.

Приложения Win32 не имеют собственного механизма для реагирования на расширенные изменения возможностей цвета. Вместо этого, если приложение использует цикл подготовки к просмотру, необходимо запросить [**IDXGIFactory1::-Current**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) для каждого кадра. Если он возвращает **значение false**, то следует получить новый **DXGI_OUTPUT_DESC1** и проверить, какие значения были изменены.

Кроме того, конвейер сообщений Win32 должен обменяться сообщением [**WM_SIZE**](../winmsg/wm-size.md) , которое указывает, что приложение могло перемещаться между разными дисплеями.

> [!Note]
> Чтобы получить новый **DXGI_OUTPUT_DESC1**, необходимо получить текущее отображение. Однако не следует вызывать метод **идксгисвапчаин:: жетконтаинингаутпут**. Это обусловлено тем, что цепочки переключения будут возвращать устаревшие выходные данные DXGI, когда **дксгифактори:: Current** имеет значение false, и повторное создание цепочки буферов для получения текущих выходных данных приводит к временному черному экрану. Вместо этого рекомендуется перечислить границы всех выходов DXGI и определить, какая из них имеет наибольшее пересечение с границами окна приложения.

Следующий пример кода взят из [репозитория DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a>Настройка цепочки буфера обмена DirectX

После определения того, что в настоящее время в дисплее поддерживаются дополнительные возможности цвета, настройте цепочку подкачки следующим образом.

### <a name="use-a-flip-presentation-model-effect"></a>Использование эффектов "перевернуть модель представления"

При создании цепочки подкачки с помощью **креатесвапчаинфор [HWND | Композиция | CoreWindow]** методы, необходимо использовать модель перелистывания DXGI, выбрав параметр **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** или **DXGI_SWAP_EFFECT_FLIP_DISCARD** , который делает цепочку подкачки доступной для расширенной цветовой обработки из DWM и различных оптимизаций на весь экран. Дополнительные сведения см. в разделе [для достижения оптимальной производительности используйте модель перелистывания DXGI](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a>Вариант 1. Использовать формат пикселей FP16 и цветовое пространство scRGB

Windows 10 поддерживает два основных сочетания формата пикселей и цветового пространства для расширенного цвета. Выберите один из них в зависимости от конкретных требований приложения.

Для приложений общего назначения при создании цепочки подкачки рекомендуется указывать [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Это также называется *FP16* в [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). По умолчанию цепочка буферов, созданная с помощью формата пикселей с плавающей точкой, обрабатывается так, как если бы она использовала [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) цветовое пространство, которое также называется *ScRGB*.

Это сочетание предоставляет числовой диапазон и точность для указания практически любого физического цвета и выполнения произвольной обработки, включая смешивание. Кроме того, если вы используете Direct2D, Win2D или Windows. UI. композиция, это единственное поддерживаемое сочетание для любой цепочки буферов или промежуточного целевого объекта, содержащего расширенное содержимое цвета. 

Основным компромиссом этого варианта является то, что он потребляет 64 бит на пиксель, что удваивает пропускную способность GPU и потребление памяти по сравнению с традиционными форматами точек SDR в формате UINT8. Кроме того, scRGB использует числовые значения, находящиеся за пределами нормализованного диапазона [0, 1], для представления цветов, находящихся за пределами палитры sRGB и/или более 80 НИТС светимости. Например, scRGB (1,0, 1,0, 1,0) кодирует стандартный белый D65 в 80 НИТС; Однако scRGB (12,5, 12,5, 12,5) кодирует тот же белый D65 с более ярким НИТС 1000. Для некоторых графических операций требуется нормализованный числовой диапазон, и необходимо либо изменить операцию, либо повторно нормализовать значения цвета.

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a>Вариант 2. Использование формата пикселей UINT10/RGB10 и HDR10/BT. 2100. цветовое пространство

Для приложений, использующих HDR10-кодированное содержимое, например проигрывателей мультимедиа или приложений, которые должны использоваться в основном в полноэкранных сценариях, таких как игры, при создании цепочки подкачки следует рассмотреть возможность указания [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) в [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). По умолчанию это рассматривается как использование цветового пространства sRGB. Поэтому необходимо явно вызвать [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)и задать в качестве цветового пространства [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), также известного как HDR10/BT. 2100.

Это сочетание имеет более строгие ограничения, чем FP16. Его можно использовать только с Direct3D 11 или Direct3D 12. Кроме того, UINT10/HDR10 имеет ограничения в виде промежуточного формата, поскольку в нем используется функция ST. 2084 ЕОТФ ("гамма"), которая является очень нелинейной и оптимизирована в виде сетевого формата, и потому, что она предлагает только 2 бита альфа-канала.

Однако это сочетание может обеспечить эффективную оптимизацию производительности при использовании в окончательном выводе приложения. Он потребляет один и тот же 32 бит на пиксель в виде традиционных форматов пикселей SDR в формате UINT8. Кроме того, в некоторых полноэкранных сценариях операционная система может оптимизировать производительность, напрямую проверяя поверхность HDR10.

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a>Использование расширенной цепочки цветовой подкачки, когда дисплей находится в режиме SDR

Можно использовать расширенную цепочку цветовой подкачки, даже если дисплей не поддерживает некоторые или все дополнительные возможности цвета, необходимые для содержимого. В таких случаях диспетчер окон рабочего стола (DWM) будет довнконверт содержимое в соответствии с возможностями экрана. В Windows 10 версии 1903 и более поздних выводятся вырезание чисел. Например, если вы готовитесь к просмотру в цепочке FP16 scRGB, то все, что находится за пределами числового диапазона [0, 1], обрезается.

Это поведение довнконверсион также возникает, если окно приложения находится на двух или более экранах с различными расширенными возможностями цвета. **Адванцедколоринфо** и **IDXGIOutput6** являются абстрактными, чтобы сообщить только о характеристиках экрана "Main" (определенных как дисплей, содержащий центр окна).

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a>Правильная визуализация содержимого SDR с белым уровнем ссылки SDR

Во многих случаях приложение будет отображать содержимое SDR и HDR. Например, отображение субтитров или элементов управления транспорта в HDR-видео или пользовательского интерфейса в игровой сцене. Важно понимать концепцию *белого уровня ссылок SDR* , чтобы убедиться, что содержимое SDR выглядит правильно на HDR-дисплее.

Windows рассматривает HDR-содержимое как _упоминаемое_, что означает, что определенное значение цвета должно отображаться на уровне яркости. Например, scRGB (1,0, 1,0, 1,0) и HDR10 (497, 497, 497) кодируются точно D65 белого по 80 НИТС светимости. В то же время, содержимое SDR обычно _выводится_ на экран (или отображается на экране), что означает, что его светимость остается для пользователя или устройства. Например, sRGB (1,0, 1,0, 1,0) кодирует белый D65 как в HDR-примерах, но с любой максимальной яркостью, для которой настроено отображение. Windows позволяет пользователю изменить _уровень ссылки SDR на белый_ по своему усмотрению. Это светимость, которую Windows будет отображать sRGB (1,0, 1,0, 1,0) по адресу. На настольных мониторах в режиме HDR ссылки на уровне ссылок SDR обычно устанавливаются в около 200 НИТС.

> [!Note]
> На дисплее, поддерживающем управление яркостью, например на ноутбуке, Windows также регулирует светимость содержимого HDR (на основе сцены), чтобы соответствовать желаемому уровню яркости пользователя, но это невидимо для приложения. Если вы не пытаетесь гарантировать точное воспроизведение сигнала HDR, вы можете игнорировать это.

Если приложение всегда отображает SDR и HDR в отдельных поверхностях и использует композицию ОС, Windows автоматически выполнит правильную корректировку для увеличения содержимого SDR до нужного белого уровня. Например, если приложение использует XAML и Преобразовывает содержимое HDR в собственный **SwapChainPanel**.

Однако если приложение выполняет собственную композицию SDR и HDR-содержимого в одну поверхность, вы несете ответственность за выполнение корректировки белого уровня на уровне SDR. В противном случае содержимое SDR может показаться слишком темным, предполагая типичные условия просмотра рабочего стола. Сначала необходимо получить текущий белый уровень ссылки SDR, а затем изменить значения цвета для любого содержимого SDR, которое вы готовите к просмотру.

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a>Шаг 1. Получение белого уровня ссылки на текущий контрольное значение SDR

Сейчас только приложения UWP могут получить текущий белый уровень ссылки SDR через [**адванцедколоринфо. сдрвхителевелиннитс**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits). Для этого API требуется [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

### <a name="step-2-adjust-color-values-of-sdr-content"></a>Шаг 2. Настройка цветовых значений SDR Content

Windows определяет номинальный или используемый по умолчанию белый уровень ссылок в 80 НИТС; Поэтому, если бы в цепочке FP16 swap отображалось стандартное значение sRGB (1,0, 1,0, 1,0), оно будет воссоздано при 80 НИТС светимости. Чтобы обеспечить соответствие фактического уровня ссылки, определяемого пользователем, необходимо настроить содержимое SDR с 80 НИТС на уровень, указанный с помощью **адванцедколоринфо. сдрвхителевелиннитс**.

При отрисовке с использованием FP16 и ScRGB или любого цветового пространства, которое использует линейную гамму (1,0), можно просто умножить значение цвета SDR на _адванцедколоринфо. сдрвхителевелиннитс_  /  _80_. Если вы используете Direct2D, то существует предопределенная константа [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), которая имеет значение 80.

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

При отрисовке с использованием нелинейного цветового пространства, такого как HDR10, выполнение корректировки белого уровня SDR более сложно; При написании собственного шейдера пикселей следует рассмотреть возможность преобразования в линейную гамму для применения коррекции.

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a>Адаптация HDR-содержимого к возможностям дисплея с помощью тонемаппинг

HDR и дополнительные цвета могут сильно различаться с точки зрения их возможностей. Например, минимальная и максимальная светимость и цветовой охват, которые они могут воссоздавать. Во многих случаях содержимое HDR будет содержать цвета, превышающие возможности экрана. Для наилучшего качества изображения это важно для выполнения тонемаппинг HDR, по сути сжимают диапазон цветов в соответствии с отображением, позволяя лучше сохранить визуальную цель содержимого.

Самым важным единственным параметром, который следует адаптировать для, является максимальная светимость, также известная как Максклл (уровень содержимого Light); более сложные тонемапперс также адаптируют минимальные светимости (Минклл) и (или) цветовые первичные цвета.

### <a name="step-1-get-the-displays-color-volume-capabilities"></a>Шаг 1. Получить возможности цветового тома экрана

#### <a name="universal-windows-platform-uwp-apps"></a>Приложения универсальной платформы Windows (UWP)

Используйте [**адванцедколоринфо**](/uwp/api/windows.graphics.display.advancedcolorinfo) для получения цветового тома экрана.

#### <a name="win32-desktop-directx-apps"></a>Приложения DirectX (для настольных систем)

Для получения цветового тома экрана используйте [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) .

### <a name="step-2-get-the-contents-color-volume-information"></a>Шаг 2. Получение сведений о цветовых томах содержимого

В зависимости от того, откуда поступило HDR-содержимое, существует несколько потенциальных способов определить его светимость и цветовую палитру. В определенных HDR-видео и файлах изображений содержатся метаданные SMPTE ST. 2086. Если содержимое было подготовлено к просмотру динамически, возможно, вы сможете извлечь сведения о сцене из внутренних стадий отрисовки, например самый светлый источник освещения в сцене.

Более общим, но дорогостоящим решением является выполнение гистограммы или другого этапа анализа для отображаемого кадра. В [примере пакета SDK Direct2D Advanced Color Images](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) показано, как это сделать с помощью Direct2D. Ниже приведены наиболее подходящие фрагменты кода.

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a>Шаг 3. Выполнение операции HDR тонемаппинг

Тонемаппинг по своей природе является процессом потери данных и может быть оптимизирован для ряда искусственного или объективных метрик, поэтому нет ни одного стандартного алгоритма. Windows предоставляет встроенный [тонемапперный результат HDR](../direct2d/hdr-tone-map-effect.md) в составе Direct2D, а также в конвейере воспроизведения видео Media Foundation HDR. Некоторые другие часто используемые алгоритмы включают в себя элементы управления "пленка", "Реинхард" и ITU-R BT. 2390-3 ИТФ (функция электрической электрической пересылки).

Ниже показан упрощенный оператор Реинхард тонемаппер.

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a>Запись содержимого HDR и ВКГ

Интерфейсы API, которые поддерживают указание форматов пикселей, например, в пространстве имен [**Windows. Graphics. Capture**](/uwp/api/windows.graphics.capture) и метод [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , предоставляют возможность захвата содержимого HDR и ВКГ без потери сведений о точках. Обратите внимание, что после получения кадров содержимого требуется дополнительная обработка. Например, сопоставление тонов HDR-to-SDR (например, снимок экрана SDR для общего доступа к Интернету) и сохранение содержимого в правильном формате (например, JPEG XR).

## <a name="additional-resources"></a>Дополнительные ресурсы

* *Использование визуализации HDR с набором средств DirectX* для DirectX [11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering). Пошаговое руководство по добавлению поддержки HDR в приложение DirectX с помощью набора средств DirectX (Директкстк).
* [Пример пакета SDK для расширенных цветовых изображений Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages). Пример пакета SDK для UWP, который реализует расширенное средство просмотра изображений HDR и ВКГ с поддержкой цветов с помощью Direct2D. Демонстрирует полный спектр рекомендаций для приложений UWP, включая реагирование на изменения возможностей дисплея и настройку для белого уровня SDR.
* [Пример Direct3D 12 для рабочего стола HDR](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR). Пример пакета SDK для Desktop реализует базовую сцену HDR с Direct3D 12.
* [Пример HDR UWP для Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR). Набор UWP, эквивалентный приведенному выше примеру.
* [Пример для Xbox АТГ СИМПЛЕХДР PC](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC). Пример пакета SDK для Desktop, реализующий базовую сцену HDR с Direct3D 11.
