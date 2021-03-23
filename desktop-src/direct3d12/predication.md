---
title: Затенения
description: Затенения — это функция, которая позволяет GPU, а не ЦП определять, что не может рисовать, копировать или отправлять объект.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2020
ms.locfileid: "104549013"
---
# <a name="predication"></a>Затенения

Затенения — это функция, которая позволяет GPU, а не ЦП определять, чтобы не рисовать, копировать или отправлять объект.

-   [Обзор](#overview)
-   [сетпредикатион](#setpredication)
-   [Связанные темы](#related-topics)

## <a name="overview"></a>Обзор

Обычно затенения используется с перекрытия; если ограничивающий прямоугольник нарисован и является перекрыто, то, очевидно, нет точки в рисовании самого объекта. В этом случае рисование объекта может быть «predicateed», что позволяет его удалить из фактической отрисовки графическим процессором.

На первый взгляд это может показаться редудантм и более поздним стандартным тестом глубины и более ранним этапом. Но затенения может устранять издержки самого состояния команды рисования, а также растрирования. Хотя ранний этап прохода удаляет ненужные пикселы, он по-прежнему может выполнять шейдеры вершин, поверхности, доменов и геометрии и вызывать входной ассемблер, тесселатор и средство программной прорисовки с фиксированной функцией. Путем рисования простого ограничивающего прямоугольника или аналогичного ограничивающего тома, &mdash; который проще обрабатывать и растрирование, чем реальная модель &mdash; , можно избежать ненужного растрирования и обработки.

В отличие от Direct3D 11, затенения отделяется от запросов и расширяется в Direct3D 12, чтобы позволить приложению выполнять предикаты для объектов на основе любой причины, по которой разработчик приложения может принять решение (не только перекрытия).

## <a name="setpredication"></a>сетпредикатион

Затенения можно задать на основе значения 64-разрядов в буфере (см. [**D3D12 \_ затенения \_ Op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).

Когда GPU выполняет команду [**сетпредикатион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , он привязывает значение в буфере. Будущие изменения данных в буфере не задним числом влияют на состояние затенения.

Если входной буфер параметров имеет значение NULL, затенения отключен.

Указания затенения отсутствуют в API Direct3D 12. и затенения разрешены в списках команд Direct, COMPUTE и Copy. Исходный буфер может находиться в любом типе кучи (по умолчанию, upload, реадбакк, Custom).

Основная среда выполнения будет проверять следующее:

-   *Алигнедбуффероффсет* имеет размер, кратный 8 байтам
-   Ресурс является буфером.
-   Операция является допустимым членом перечисления
-   [**Сетпредикатион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) не может быть вызван из пакета
-   Тип списка команд поддерживает затенения
-   Смещение не превышает размер буфера

Отладочный слой выдаст ошибку, если исходный буфер не находится в [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (который совпадает с [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)и просто псевдонимом).

Набор операций, которые могут быть предикатами:

-   [**дравинстанцед**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [**дравиндексединстанцед**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**копибуфферрегион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**копиресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**копитилес**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ресолвесубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**клеарунордередакцессвиевуинт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**клеарунордередакцессвиевфлоат**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ексекутеиндирект**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

[**Ексекутебундле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) не является самим предикатом. Вместо этого отдельные операции из приведенного выше списка, содержащиеся в конце пакета, объединяются в предикате.

Методы ID3D12GraphicsCommandList [**ресолвекуеридата**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**бегинкуери**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) и [**ендкуери**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) не являются предикатами.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Счетчики и запросы](counters-and-queries.md)
</dt> <dt>

[Измерение производительности](performance-measurement.md)
</dt> <dt>

[Пошаговые инструкции по запросам затенения](predication-queries.md)
</dt> </dl>

 

 




