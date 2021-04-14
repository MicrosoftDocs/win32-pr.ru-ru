---
title: DPI_AWARENESS_CONTEXTный маркер (виндеф. h)
description: Определяет контекст осведомленности для окна.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340750"
---
# <a name="dpi_awareness_context-handle"></a>\_Описатель контекста осведомленности о dpi \_

Определяет контекст осведомленности для окна.

## <a name="syntax"></a>Синтаксис

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Константы

**Независимый \_ контекст осведомленности о dpi \_ \_**<dl> DPI не расзнается. Это окно не масштабируется для изменения DPI и всегда предполагается, что коэффициент масштабирования составляет 100% (96 точек на дюйм). Она будет автоматически масштабироваться системой при любом другом параметре DPI.  
</dl>

**\_ \_ система контекста осведомленности \_ \_ об уровне dpi**<dl> Учитывать DPI системы. Это окно не масштабируется для изменения DPI. Он будет запрашивать разрешение DPI один раз и использовать это значение в течение времени существования процесса. Если значение DPI меняется, процесс не будет скорректирован до нового значения DPI. Она будет автоматически масштабироваться по системе, когда значение DPI меняется со значения System.  
</dl>

**\_ \_ Отслеживание контекста с \_ \_ учетом dpi на монитор \_**<dl> Отслеживание DPI для каждого монитора. Это окно проверяет наличие DPI при его создании и корректирует коэффициент масштабирования при изменении DPI. Эти процессы не масштабируются автоматически системой.  
</dl>

**\_ \_ Контекст осведомленности \_ о dpi на \_ монитор \_ \_ версии 2**<dl> Также известен **для каждого монитора версии 2**. Переносится к исходному режиму поддержки DPI для каждого монитора, который позволяет приложениям получать доступ к новому поведению масштабирования, связанному с DPI, для каждого окна верхнего уровня.  
На монитор версии 2 был сделан доступным в обновлении для дизайнеров Windows 10 и недоступен в более ранних версиях операционной системы.  
Ниже представлены дополнительные варианты поведения.

-   **Уведомления об изменении dpi дочернего окна** . в контексте каждого монитора версии 2 все дерево окна уведомляется о любых произошедших изменениях dpi.
-   **Масштабирование неклиентской области** . все окна автоматически будут иметь неклиентскую область, отрисованную с учетом dpi. Вызовы [**енабленонклиентдпискалинг**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) не нужны.
-   **Масштабирование меню Win32** . все меню NTuser, созданные в контекстах Monitor 2, будут масштабироваться в соответствии с мониторингом.
-   **Масштабирование диалоговых окон** . диалоговые окна Win32, созданные в каждом контексте монитора версии 2, автоматически реагируют на изменения dpi.
-   **Улучшенное масштабирование элементов управления Comctl32** . различные элементы управления Comctl32 имеют улучшенное масштабирование DPI в контекстах монитора версии 2.
-   **Улучшенное поведение** . дескрипторы укссеме, открытые в контексте каждого окна монитора версии 2, будут действовать с точки зрения dpi, связанного с этим окном.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

Неосведомленность DPI с улучшенным качеством содержимого на основе GDI. Этот режим работает аналогично DPI_AWARENESS_CONTEXT_UNAWARE, но также позволяет системе автоматически улучшать качество отрисовки текста и других примитивов на основе GDI, когда окно отображается на мониторе с высоким разрешением.

Дополнительные сведения см. в разделе [улучшение возможностей высокого DPI в классических приложениях на основе GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED была введена в Октябрь 2018 обновления Windows 10 октября (также известной как версия 1809).


## <a name="requirements"></a>Требования

| Требование | Значение |
|----|-----------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1607\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается <br/>  |
| Header<br/>                   | <dl> <dt>виндеф. h</dt> </dl> |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аредпиаваренессконтекстсекуал**](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[**жетаваренессфромдпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[**жетдпифромдпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[**жетсреаддпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[**жетвиндовдпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[**исвалиддпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[**сетпроцессдпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[**сетсреаддпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
