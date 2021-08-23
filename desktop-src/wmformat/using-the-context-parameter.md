---
title: Использование параметра context
description: Использование параметра context
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Пакет SDK для формата мультимедиа, параметр контекста
- Windows Пакет SDK для формата мультимедиа, параметр Пвконтекст
- Пвконтекст, параметр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102315470243910158fd3bf474a209fa1e0888536671e3ede3764be519c672f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585204"
---
# <a name="using-the-context-parameter"></a>Использование параметра context

некоторые обратные вызовы, используемые пакетом SDK Windows Media Format, принимают параметр с именем *пвконтекст*. Вызывающие объекты проходят по значению, указанному в методе, который начал асинхронного действия. Например, при вызове [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)можно передать значение для *пвконтекст*. Когда метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) вызывается объектом Reader для уведомления приложения о том, что файл был открыт, он передает любое значение, использованное в вызове **, в качестве параметра** *пвконтекст* в **OnStatus**. Этот параметр контекста предоставляется для использования, и его можно использовать любым способом.

Параметр *пвконтекст* чаще всего используется, если несколько объектов должны совместно использовать один и тот же обратный вызов. Например, несколько объектов используют метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . *Пвконтекст* можно использовать, чтобы разрешить различным объектам совместно использовать одну реализацию **OnStatus** , передав другое значение для *пвконтекст* в исходном вызове. В реализации **OnStatus** логику обработки сообщений можно создать с учетом значения *пвконтекст*.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Использование методов обратного вызова**](using-the-callback-methods.md)
</dt> </dl>

 

 




