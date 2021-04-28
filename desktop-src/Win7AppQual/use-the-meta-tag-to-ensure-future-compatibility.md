---
description: Использование тега meta для обеспечения совместимости в будущем
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Использование тега meta для обеспечения совместимости в будущем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a69180470c60dffc772f20fe6c515ba3803cbf2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084172"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Использование тега meta для обеспечения совместимости в будущем

Windows Internet Explorer 8 позволяет управлять режимами совместимости документов, позволяя обозревателю отображать веб-страницы таким же образом, как и старые версии браузера. Вы также можете выбрать время обновления веб-страницы, в то время как она будет использоваться и правильно работать.

## <a name="setting-the-meta-element"></a>Установка элемента meta

Элемент **meta** включает атрибут **Content** , который позволяет указать режим отображения содержимого для веб-страницы, как показано в следующей таблице.



| Значение | Режим рендеринга                                                 |
|-------|----------------------------------------------------------------|
| IE = 9  | Использовать режим отображения стандартов Windows Internet Explorer 9   |
| IE = 8  | Использовать режим отображения стандартов Internet Explorer 8           |
| IE = 7  | Использовать режим отображения стандартов Windows Internet Explorer 7   |
| IE=5  | Использовать режим отображения стандартов Microsoft Internet Explorer 5 |



 

Дополнительные сведения о совместимости и заголовке X-UA-Compatible см. в разделе [Определение совместимости документов](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) в библиотеке MSDN.

В следующем примере кода показано, как принудительно отобразить веб-страницу в режиме Internet Explorer 8.


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a>Использование заголовка HTTP

Многие веб-сайты содержат тысячи (или десятки тысяч) отдельных веб-страниц, поэтому установка элемента **meta** в каждом документе непрактична. Если вы хотите задать элемент **meta** для всех страниц или коллекцию страниц, выбранных в папке, можно настроить конфигурацию сервера и добавить метаданные X-UA-Compatible в [заголовок HTTP](/previous-versions/cc817572(v=msdn.10)).

Для сайтов, которым требуются разные значения **мета** -элементов для страниц на том же сервере, существует несколько средств, которые автоматически создают и вставляют соответствующий элемент **meta** . Например, служебная программа [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) из Aggiorno вставляет и удаляет функцию тега совместимости Internet Explorer 8 и может помочь вашему сайту соответствовать определенным стандартам совместимости.

## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[Устранение проблем совместимости в веб-приложениях с помощью представления совместимости](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
