---
title: Использование параметра context
description: Использование параметра context
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media Format SDK, параметр контекста
- Windows Media Format SDK, параметр Пвконтекст
- Пвконтекст, параметр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133475"
---
# <a name="using-the-context-parameter"></a>Использование параметра context

Некоторые обратные вызовы, используемые пакетом SDK для формата Windows Media, принимают параметр с именем *пвконтекст*. Вызывающие объекты проходят по значению, указанному в методе, который начал асинхронного действия. Например, при вызове [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)можно передать значение для *пвконтекст*. Когда метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) вызывается объектом Reader для уведомления приложения о том, что файл был открыт, он передает любое значение, использованное в вызове **, в качестве параметра** *пвконтекст* в **OnStatus**. Этот параметр контекста предоставляется для использования, и его можно использовать любым способом.

Параметр *пвконтекст* чаще всего используется, если несколько объектов должны совместно использовать один и тот же обратный вызов. Например, несколько объектов используют метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . *Пвконтекст* можно использовать, чтобы разрешить различным объектам совместно использовать одну реализацию **OnStatus** , передав другое значение для *пвконтекст* в исходном вызове. В реализации **OnStatus** логику обработки сообщений можно создать с учетом значения *пвконтекст*.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование методов обратного вызова**](using-the-callback-methods.md)
</dt> </dl>

 

 




