---
title: Улучшения в Direct3D 9Ex
description: в этом разделе описано, как в Windows 7 добавлена поддержка режима перелистывания и связанной с ним статистики в Direct3D 9Ex и диспетчер окон рабочего стола.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3221b805f07408b27e19a00a42ca0c4733ea725bd32a51b5b3e340b48d2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796996"
---
# <a name="direct3d-9ex-improvements"></a>Улучшения в Direct3D 9Ex

в этом разделе описано, как в Windows 7 добавлена поддержка режима перелистывания и связанной с ним статистики в Direct3D 9Ex и диспетчер окон рабочего стола. Целевые приложения включают приложения для показа видео или частоты кадров. Приложения, использующие режим отражения Direct3D 9Ex, предоставляют возможность снизить нагрузку на системные ресурсы при включенном DWM. Предоставление улучшений статистики, связанных с режимом отражения, позволяет приложениям Direct3D 9Ex лучше управлять скоростью презентации, предоставляя механизмы обратной связи и исправления в режиме реального времени. Включены подробные пояснения и указатели на примеры ресурсов.

В этом разделе содержатся следующие подразделы.

-   [новые возможности Direct3D 9Ex для Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Представление режима отражения Direct3D 9EX](#direct3d-9ex-flip-mode-presentation)
-   [Модель программирования и API](#programming-model-and-apis)
    -   [Как принять участие в модели отражения Direct3D 9Ex](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Рекомендации по проектированию для приложений модели 9Ex для отражения Direct3D](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Синхронизация кадров для приложений модели перелистывания Direct3D 9Ex](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Синхронизация кадров для оконных приложений при отключенном DWM](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Пошаговое руководство по модели перелистывания Direct3D 9Ex и представлению статистики](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [сводка по программированию Рекомендации для синхронизации кадров](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Заключение об улучшениях Direct3D 9Ex](#conclusion-about-direct3d-9ex-improvements)
-   [Вызов действия](#call-to-action)
-   [Связанные темы](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>новые возможности Direct3D 9Ex для Windows 7

режим отражения представления direct3d 9Ex является улучшенным режимом представления изображений в direct3d 9Ex, которые эффективно выводят изображения в Windows 7 диспетчер окон рабочего стола (DWM) для композиции. начиная с Windows Vista DWM формирует весь настольный компьютер. Когда DWM включен, приложения с оконным режимом представляют свое содержимое на рабочем столе с помощью метода с именем БЛТ Mode, представленного DWM (или БЛТ Model). При использовании модели БЛТ DWM сохраняет копию поверхности визуализации Direct3D 9Ex для композиции рабочего стола. При обновлении приложения новое содержимое копируется на поверхность DWM через БЛТ. Для приложений, содержащих Direct3D и GDI, данные GDI также копируются на поверхность DWM.

режим перелистывания, доступный в Windows 7, включен в DWM (или отражение модели), — это новый метод представления, который, по сути, позволяет передавать дескрипторы областей приложений между приложениями оконного режима и DWM. Помимо сохранения ресурсов, модель отражения поддерживает улучшенную текущую статистику.

Эта статистика представляет собой сведения о времени кадров, которые приложения могут использовать для синхронизации видеопотоков и звуковых потоков, а также для восстановления после сбоев воспроизведения видео. Сведения о времени кадров в представленной статистике позволяют приложениям настраивать скорость показа видеокадров для более гладких презентаций. в Windows Vista, где DWM поддерживает соответствующую копию области кадров для композиции рабочего стола, приложения могут использовать представленную статистику, предоставляемую DWM. этот метод получения текущей статистики будет по-прежнему доступен в Windows 7 для существующих приложений.

в Windows 7 приложения на основе Direct3D 9Ex, использующие модель отражения, должны использовать интерфейсы api D3D9Ex для получения текущей статистики. Когда DWM включен, в оконном режиме и полноэкранном режиме монопольного режима Direct3D 9Ex приложения могут рассчитывать на одни и те же данные статистики при использовании модели перелистывания. Модель перелистывания Direct3D 9Ex, имеющая статистику. позволяет приложениям запрашивать статистические данные в режиме реального времени, а не после отображения кадра на экране; одни и те же данные статистики доступны для приложений с оконным режимом Flip-Model с поддержкой приложений в полноэкранном режиме. добавленный флаг в интерфейсах API D3D9Ex позволяет приложениям-шаблонам эффективно удалять последние кадры во время презентации.

модель перелистывания Direct3D 9Ex должна использоваться новыми приложениями для показа видео или кадров, которые предназначены для Windows 7. Из-за синхронизации между DWM и средой выполнения Direct3D 9Ex в приложениях, использующих модель перелистывания, необходимо указать от 2 до 4 обратных буферов, чтобы обеспечить плавную презентацию. Для приложений, использующих данные о статистике, будет выгодно использовать улучшенную статистику.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Представление режима отражения Direct3D 9EX

Повышение производительности в режиме зеркального отражения Direct3D 9Ex имеет большое значение в системе, когда DWM включен и приложение находится в оконном режиме, а не в полноэкранном режиме монопольного доступа. В следующей таблице и иллюстрации показано упрощенное Сравнение использования пропускной способности памяти и операций чтения и записи в приложениях с окнами, которые выбирают отразить модель относительно модели использования по умолчанию БЛТ.



| Режим БЛТ, представленный в DWM                                                                                                 | Режим перелистывания D3D9Ex, представленный в DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. приложение обновляет свой кадр (Write).<br/>                                                                 | 1. приложение обновляет свой кадр (Write).<br/>                     |
| 2. Среда выполнения Direct3D копирует содержимое поверхности в поверхность перенаправления DWM (чтение, запись).<br/>                       | 2. Среда выполнения Direct3D передает поверхность приложения в DWM<br/>        |
| 3. После завершения копирования в общей области DWM отображает на экране область приложения (чтение, запись).<br/> | 3. DWM отображает поверхность приложения на экране (чтение, запись).<br/> |



 

![Иллюстрация сравнения модели БЛТ и модели перелистывания](images/blt-flip-mode-present.png)

Режим перелистывания представляет собой сокращение использования системной памяти за счет сокращения числа операций чтения и записи средой выполнения Direct3D для композиции оконных кадров с помощью DWM. Это снижает энергопотребление системы и общее использование памяти.

Приложения могут воспользоваться преимуществами режима перелистывания Direct3D 9Ex, который предоставляет расширенные статистические данные, когда DWM включен, независимо от того, находится ли приложение в оконном режиме или в полноэкранном режиме монопольного доступа.

## <a name="programming-model-and-apis"></a>Модель программирования и API

новая частота видео или кадров. определении приложения, использующие api Direct3D 9Ex на Windows 7, могут использовать преимущества памяти и энергосбережения и улучшенную презентацию, предлагаемую режимом отражения при работе в Windows 7. (при запуске в предыдущих версиях Windows среда выполнения Direct3D по умолчанию использует приложение в режиме блт.)

Режим отражения подразумевает, что приложение может воспользоваться преимуществами отзывов и исправлений статистики в реальном времени, когда DWM включен. Однако приложения, использующие режим перелистывания, должны иметь представление об ограничениях при использовании параллельной отрисовки API GDI.

Можно изменить существующие приложения, чтобы воспользоваться преимуществами режима перелистывания, с теми же преимуществами и предостережениями, что и у вновь разработанных приложений.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Как принять участие в модели отражения Direct3D 9Ex

приложения Direct3D 9Ex, предназначенные для Windows 7, могут выбрать модель перелистывания путем создания цепочки буферов с помощью значения перечисления [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) . Чтобы принять участие в переворачивании модели, приложения определяют структуру [**\_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) , а затем передают указатель на эту структуру при вызове API [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) . в этом разделе описано, как приложения, предназначенные для Windows 7, использовать **IDirect3D9Ex:: креатедевицеекс** для выбора модели перелистывания. Дополнительные сведения об API **IDirect3D9Ex:: креатедевицеекс** см. в разделе **IDirect3D9Ex:: креатедевицеекс на сайте MSDN**.

Для удобства синтаксис [**\_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) и [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) повторяется здесь.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

при изменении 9Ex приложений Direct3D для Windows 7 для выбора модели перелистывания следует учитывать следующие элементы об указанных членах [**\_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):

<dl> <dt>

**баккбуфферкаунт**
</dt> <dd>

(только Windows 7)

Если для **SwapEffect** задан новый \_ тип эффектов цепочки замены D3DSWAPEFFECT флипекс, то число задних буферов должно быть больше или равно 2, чтобы предотвратить снижение производительности приложения в результате ожидания освобождения предыдущего текущего буфера диспетчером DWM.

Если приложение также использует представленную статистику, связанную с D3DSWAPEFFECT \_ флипекс, рекомендуется установить для счетчика задних буферов значение от 2 до 4.

использование D3DSWAPEFFECT \_ флипекс в Windows Vista или предыдущих версиях операционной системы вернет ошибку [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

**SwapEffect**
</dt> <dd>

(только Windows 7)

Новый \_ тип эффектов цепочки D3DSWAPEFFECT флипекс swap определяет, когда приложение использует режим перелистывания, представленный в DWM. Это позволяет приложению более эффективно использовать память и мощь, а также позволяет приложению воспользоваться преимуществами полноэкранного представления статистики в оконном режиме. Поведение полноэкранного приложения не затрагивается. Если для параметра windowd задано значение **true** , а для **SwapEffect** задано значение D3DSWAPEFFECT \_ флипекс, среда выполнения создает один лишний обратный буфер и поворачивает каждый из них в буфер, который становится передним буфером во время презентации.

</dd> <dt>

**Флаги**
</dt> <dd>

(только Windows 7)

Не удается установить флаг [D3DPRESENTFLAG \_ БЛОКИРУЕМого \_ буфера](/windows/desktop/direct3d9/d3dpresentflag) обмена, если для **SwapEffect** задан новый тип воздействия на цепочку замены [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) .

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Рекомендации по проектированию для приложений модели 9Ex для отражения Direct3D

Используйте рекомендации, приведенные в следующих разделах, чтобы разработать приложения модели отражения 9Ex Direct3D.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Использование режима отражения в отдельном HWND из режима БЛТ

Приложения должны использовать режим перелистывания Direct3D 9Ex, имеющийся в HWND, который не предназначен для других API, включая режим БЛТ, который представляет Direct3D 9Ex, другие версии Direct3D или GDI. Режим отражения может использоваться для представления дочерним окнам; Таким образом, приложения могут использовать модель перелистывания, если она не смешана с моделью БЛТ в том же HWND, как показано на следующих иллюстрациях.

![Иллюстрация родительского окна Direct3D и дочернего окна GDI, каждый из которых имеет собственный HWND](images/parent-d3d.png)

![Иллюстрация родительского окна GDI и дочернего окна Direct3D, каждый из которых имеет собственный HWND](images/parent-gdi.png)

Так как модель БЛТ поддерживает дополнительную копию поверхности, GDI и другие содержимое Direct3D можно добавить в один и тот же HWND через поэтапные обновления из Direct3D и GDI. С помощью модели перелистывания можно увидеть только содержимое Direct3D 9Ex в цепочках подкачки [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) , которые передаются в DWM. Все остальные обновления БЛТ модели Direct3D или GDI будут игнорироваться, как показано на следующих иллюстрациях.

![Иллюстрация текста GDI, который может не отображаться, если используется модель перелистывания, а содержимое Direct3D и GDI находятся в одном HWND](images/d3d-gdi-same-hwnd.png)

![Иллюстрация содержимого Direct3D и GDI, в котором включены DWM и приложение находится в режиме с окнами](images/d3d-gdinotext-same-hwnd.png)

Поэтому модель отражения должна быть включена для буферов цепочки подкачки, где только модель перелистывания Direct3D 9Ex отрисовывается во весь HWND.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>Не используйте модель перелистывания с Скроллвиндов или Скроллвиндовекс GDI

Некоторые приложения Direct3D 9Ex используют функции Скроллвиндов или Скроллвиндовекс GDI для обновления содержимого окна при активации события прокрутки пользователем. Скроллвиндов и Скроллвиндовекс выполняют блтс содержимое окна на экране при прокрутке окна. Эти функции также нуждаются в обновлениях модели БЛТ для содержимого GDI и Direct3D 9Ex. Приложения, использующие какую-либо функцию, не обязательно будут отображать видимое содержимое окна при прокрутке экрана, когда приложение находится в оконном режиме, а DWM включен. Мы не рекомендуем использовать интерфейсы API Скроллвиндов и Скроллвиндовекс GDI в приложениях, а затем перерисовывать их содержимое на экране в ответ на прокрутку.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Использовать одну \_ цепь перекачки D3DSWAPEFFECT флипекс на HWND

Приложения, использующие модель перелистывания, не должны использовать несколько цепочек переключения моделей перелистывания, предназначенных для одного и того же HWND.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Синхронизация кадров для приложений модели перелистывания Direct3D 9Ex

Текущая статистика — это сведения о времени кадров, которые используются приложениями мультимедиа для синхронизации видео и звуковых потоков, а затем восстанавливаются после сбоев воспроизведения видео. Чтобы обеспечить доступность статистики, приложение Direct3D 9Ex должно гарантировать, что параметр *бехавиорфлагс* , который приложение передает в [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) , содержит флаг поведения устройства [D3DCREATE \_ включить \_ пресентстатс](/windows/desktop/direct3d9/d3dcreate).

Для удобства синтаксис [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) повторяется здесь.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

Модель перелистывания Direct3D 9Ex добавляет флаг презентации [ \_ форцеиммедиате D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) , обеспечивающий [ \_ \_ мгновенное](/windows/desktop/direct3d9/d3dpresent) поведение флага D3DPRESENT. Приложение Direct3D 9Ex указывает эти флаги презентации в параметре *dwFlags* , который приложение передает в [**IDirect3DDevice9Ex::P ресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), как показано ниже.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

при изменении приложения Direct3D 9Ex для Windows 7 следует учитывать следующие сведения об указанных флагах презентации [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) :

<dl> <dt>

[D3DPRESENT \_ донотфлип](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Этот флаг доступен только в полноэкранном режиме или

(только Windows 7)

Когда приложение задает член **SwapEffect** [**\_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) в [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) в вызове [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

[D3DPRESENT \_ форцеиммедиате](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(только Windows 7)

Этот флаг можно указать только в том случае, если приложение  задает для члена [**SwapEffect \_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) значение [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) в вызове [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex). Приложение может использовать этот флаг, чтобы немедленно обновить поверхность с несколькими кадрами позже в очереди DWM Present, по сути пропуская промежуточные кадры.

Оконные приложения с поддержкой Флипекс могут использовать этот флаг для немедленного обновления поверхности с кадром, который позже находится в очереди DWM, пропуская промежуточные кадры. Это особенно полезно для мультимедийных приложений, которые хотят отбросить фреймы, которые были обнаружены как последние и представлять последующие кадры во время составления. [**IDirect3DDevice9Ex::P ресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) возвращает ошибку недопустимого параметра, если этот флаг указан неправильно.

</dd> </dl>

Чтобы получить данные статистики, приложение получает структуру [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) , вызывая API [**IDirect3DSwapChain9Ex:: жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .

Структура [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) содержит статистику о вызовах [**IDirect3DDevice9Ex::P ресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) . Устройство должно быть создано с помощью вызова [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) с флагом [D3DCREATE \_ Enable \_ пресентстатс](/windows/desktop/direct3d9/d3dcreate) . В противном случае данные, возвращаемые функцией [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) , не определены. Цепочка подкачки Direct3D 9Ex с поддержкой отражения предоставляет данные статистики в оконном и полноэкранном режимах.

Для цепочек переключения БЛТ 9Ex Direct3D с поддержкой моделей в оконном режиме все значения структуры [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) будут обнулены.

Для Флипекс представлена статистика [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) возвращает D3DERR представления о несвязанной \_ \_ статистике \_ в следующих ситуациях:

-   Первый вызов [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) когда-либо, что означает начало последовательности
-   Выход из рабочего стола из состояния "вкл."
-   Изменение режима: в оконном режиме на весь экран или из полноэкранного режима до полноэкранных переходов

Для удобства синтаксис [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) повторяется здесь.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

Метод [**IDirect3DSwapChain9Ex:: жетластпресенткаунт**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) возвращает последнюю пресенткаунт, то есть текущий идентификатор последнего успешного вызова, который был создан устройством отображения, связанным с цепочкой буферов обмена. Этот идентификатор представляет собой значение элемента **пресенткаунт** структуры [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) . Для цепочек переключения БЛТ 9Ex Direct3D с поддержкой модели в оконном режиме все значения структуры **D3DPRESENTSTATS** будут обнулены.

Для удобства синтаксис [**IDirect3DSwapChain9Ex:: жетластпресенткаунт**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) повторяется здесь.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

при изменении приложения Direct3D 9Ex для Windows 7 следует учитывать следующие сведения о структуре [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :

-   Значение Пресенткаунт, возвращаемое [**жетластпресенткаунт**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) , не обновляется, когда вызов [**пресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) с D3DPRESENT \_ донотваит, указанным в параметре *dwFlags* , возвращает ошибку.
-   Когда [**пресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) вызывается с помощью D3DPRESENT \_ Донотфлип, вызов [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) выполняется, но не возвращает обновленную структуру [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) , когда приложение находится в оконном режиме.
-   **Пресентрефрешкаунт** и **синкрефрешкаунт** в [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):
    -   **Пресентрефрешкаунт** равно **синкрефрешкаунт** , когда приложение представлено на каждом вертикальной синхронизации.
    -   **Синкрефрешкаунт** получается в интервале вертикальной синхронизации, когда предпринята передача, **синккпктиме** приблизительно соответствует времени, связанному с интервалом вертикальной синхронизации.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Синхронизация кадров для оконных приложений при отключенном DWM

Когда DWM отключается, оконные приложения отображаются непосредственно на экране монитора, не пробегая цепочки зеркального отражения. в Windows Vista не поддерживается получение статистических данных о кадрах для оконных приложений, когда DWM выключен. чтобы поддерживать API, где приложениям не требуется использовать dwm, Windows 7 будет возвращать сведения о статистике кадров для оконных приложений, когда DWM выключен. Статистика кадра, возвращаемая при отключенном DWM, является только оценкой.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through модели отражения Direct3D 9Ex и представление статистики — пример

**Чтобы принять участие в презентации Флипекс для примера Direct3D 9Ex**

1.  убедитесь, что пример приложения работает в Windows 7 или более поздней версии операционной системы.
2.  Задайте для элемента **SwapEffect** в [**\_ параметрах D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) значение [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) в вызове [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



**Чтобы выбрать Флипекс, связанную с этой статистикой для примера 9Ex Direct3D**

-   Задайте [D3DCREATE \_ Enable \_ пресентстатс](/windows/desktop/direct3d9/d3dcreate) в параметре *бехавиорфлагс* [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



**Чтобы избежать проблем, выявление и восстановление после сбоев**

1.  Вызовы, представленные в очереди: Рекомендуемое число буферов в диапазоне от 2 до 4.
2.  В примере Direct3D 9Ex добавляется неявный Недопустимый буфер, фактически Текущая длина очереди — число незаполненных буферов + 1.
3.  Класс Helper предоставляет структуру очереди для хранения всех успешно отправленных ИДЕНТИФИКАТОРов представления (Пресенткаунт) и связанных, вычисляемых или ожидаемых Пресентрефрешкаунт.
4.  Чтобы обнаружить возникновение сбоя, выполните следующие действия:

    -   Вызовите [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).
    -   Получите текущий идентификатор (Пресенткаунт) и число вертикальной синхронизации, где отображается кадр (Пресентрефрешкаунт) кадра, для которого получена статистика.
    -   Извлеките ожидаемый Пресентрефрешкаунт (Таржетрефреш в образце кода), связанный с текущим ИДЕНТИФИКАТОРом.
    -   Если фактический Пресентрефрешкаунт позже, чем ожидалось, произошла ошибка.

5.  Для восстановления после сбоя выполните следующие действия.

    -   Вычислите количество пропускаемых кадров (g \_ ииммедиатес Variable в образце кода).
    -   Представьте пропущенные кадры с интервалом D3DPRESENT \_ форцеиммедиате.

**Рекомендации по обнаружению и восстановлению сбоев**

1.  Восстановление после сбоя принимает N (g \_ икуеуеделай Variable в образце кода) число существующих вызовов, где N (g \_ икуеуеделай) равно g \_ Ииммедиатес плюс длина текущей очереди, то есть:

    -   Пропуск кадров с текущим интервалом D3DPRESENT \_ форцеиммедиате, плюс
    -   В поставленных в очередь представление, которое необходимо обработать

2.  Установите ограничение на длину сбоя ( \_ \_ в примере — предельное число аварийных восстановлений). Если пример приложения не может выполнить восстановление после слишком длинного сбоя (например, 1 секунда или 60 всинкс для монитора 60 Гц), можно переключиться на временную анимацию и сбросить текущую вспомогательную очередь.


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



**Пример сценария**

-   На следующем рисунке показано приложение с количеством буферов в 4. Фактически Текущая длина очереди равна 5.

    ![Иллюстрация отображаемых кадров аппликас и представление очереди](images/sample-scenario.png)

    Кадр а предназначен для перехода на экран с числом интервалов синхронизации, равным 1, но было обнаружено, что оно отображается в интервале синхронизации, равном 4. Поэтому произошел сбой. Последующие 3 кадра представлены с D3DPRESENT \_ интервалом \_ форцеиммедиате. Сбой должен занять до 8 вызовов до восстановления. следующий кадр будет отображаться в соответствии со значением интервала синхронизации.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>сводка по программированию Рекомендации для синхронизации кадров

-   Создайте резервный список всех идентификаторов Ластпресенткаунт (полученных через [**жетластпресенткаунт**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) и связанных с ними оценочных пресентрефрешкаунт всех предоставленных данных.
    > [!Note]  
    > Когда приложение вызывает [**пресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) с помощью D3DPRESENT \_ Донотфлип, вызов [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) выполняется, но не возвращает обновленную структуру [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) , когда приложение находится в оконном режиме.

     

-   Вызовите [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) , чтобы получить фактический пресентрефрешкаунт, связанный с каждым ПРЕДСТАВЛЕНным идентификатором отображаемых кадров, чтобы убедиться, что приложение обрабатывает ошибку, возвращенную из вызова.
-   Если фактический Пресентрефрешкаунт является более поздней, чем оценка Пресентрефрешкаунт, обнаруживается сбой. Компенсация за счет отправки кадров задержкойа, имеющихся в D3DPRESENT \_ форцеиммедиате.
-   Когда один кадр отображается в текущей очереди в конце, все последующие кадры в очереди будут представлены позднее. D3DPRESENT \_ форцеиммедиате будет исправлять только следующий кадр, который будет представлен после всех кадров в очереди. Таким образом, Текущая очередь или число буферов небольшого размера не должны быть слишком длинными, так что при этом возникает меньше сбоев кадров. Оптимальное число походящих буферов в диапазоне от 2 до 4.
-   Если предполагаемый Пресентрефрешкаунт позже, чем фактический Пресентрефрешкаунт, может произойти регулирование DWM. Возможны следующие решения.

    -   сокращение длины текущей очереди
    -   уменьшение требований к памяти GPU с помощью других средств, помимо уменьшения числа существующих очередей (т. е. снижения качества, удаления эффектов и т. д.)
    -   Указание [**двменаблеммксс**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) для предотвращения регулирования DWM в целом

-   Проверьте работоспособность представления приложения и производительность статистики кадров в следующих сценариях:

    -   Включение и отключение DWM
    -   полноэкранные и оконные режимы
    -   оборудование с более низким уровнем возможностей

-   Когда приложения не могут восстановиться из большого числа кадров с ошибкой с D3DPRESENT \_ форцеиммедиате, они потенциально могут выполнять следующие операции:

    -   Сократите использование ЦП и GPU, выполнив визуализацию с меньшей рабочей нагрузкой.
    -   в случае кодирования видео ускоряет декодирование, уменьшая качество и, следовательно, использование ЦП и GPU.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Заключение об улучшениях Direct3D 9Ex

в Windows 7 приложения, отображающие частоту кадров видео или датчика во время презентации, могут отражать модель перелистывания. Представленные в статистике усовершенствования, связанные с отражением модели Direct3D 9Ex, могут использовать приложения, которые синхронизируют презентацию на частоту кадров, а также отзывы в реальном времени для обнаружения и восстановления сбоев. Разработчикам, использующим модель перелистывания Direct3D 9Ex, следует ориентироваться на отдельный HWND из содержимого GDI и синхронизацию частот кадров в учетной записи. Дополнительные сведения см. в этой статье и в документации MSDN. Дополнительную документацию см. [в центре разработчиков DirectX на сайте MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).

## <a name="call-to-action"></a>Призыв к действию

мы рекомендуем использовать модель перелистывания Direct3D 9Ex и ее текущую статистику на Windows 7 при создании приложений, которые пытаются синхронизировать частоту кадров в презентации или восстановить после сбоев отображения.

## <a name="related-topics"></a>Связанные темы

[Центр разработчиков DirectX на MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>