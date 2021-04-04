---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Строка браузера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999749"
---
# <a name="user-agent-string"></a>Строка браузера

*Строка агента пользователя* содержит сведения об удостоверении браузера. Строка агента пользователя передается на веб-сервер как заголовок HTTP каждый раз, когда браузер выполняет запрос к веб-серверу. Вы также можете получить доступ к нему через клиентский сценарий. Например, можно отобразить строку агента пользователя, введя следующий URL-адрес в адресную строку Windows Internet Explorer 8: "JavaScript: Alert (Navigator. userAgent)". На следующем рисунке показано типичное результирующее диалоговое окно из Internet Explorer 8, работающее под Windows 7.

![снимок экрана окна Internet Explorer диаог со строкой агента пользователя](images/useragent-alert.png)

Как правило, строка агента пользователя анализируется специально для подстроки MSIE. На основе сообщаемой версии браузера логика программирования на стороне клиента или на стороне сервера выполняет другое действие. Дополнительные сведения о строке агента пользователя см. в разделе [что будет отображаться в отчете Windows Internet Explorer как строка User-Agent?](/previous-versions/cc817582(v=msdn.10)) в библиотеке MSDN.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устранение проблем совместимости в веб-приложениях с помощью представления совместимости](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



