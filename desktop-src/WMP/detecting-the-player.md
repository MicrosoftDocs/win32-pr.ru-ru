---
title: Обнаружение проигрывателя
description: Обнаружение проигрывателя
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Интернет-магазины проигрывателя Windows Media, обнаружение игроков
- Интернет-магазины, обнаружение игроков
- Тип 1 Интернет-магазины, обнаружение игроков
- Тип 2 Интернет-магазинов, обнаружение игроков
- Интернет-магазины проигрывателя Windows Media, обнаружение игрока
- Интернет-магазины, обнаружение игроков
- Тип 1 Интернет-магазины, обнаружение игрока
- Тип 2 Интернет-магазинов, обнаружение игрока
- Обнаружение игрока
- Обнаружение игроков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986553"
---
# <a name="detecting-the-player"></a>Обнаружение проигрывателя

При создании веб-страницы для Интернет-магазина вы можете решить, что пользователи должны иметь возможность просматривать страницу в браузере или проигрывателе Windows Media. Вы можете использовать сценарий ASP, чтобы определить, размещена ли веб-страница в проигрывателе.

Следующий пример кода извлекает параметр version из строки запроса URL-адреса, чтобы определить, размещена ли страница в проигрывателе Windows Media.


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



Обратите внимание, что в приведенном выше коде предполагается, что параметр version существует в строке запроса при размещении в проигрывателе Windows Media. Это справедливо для страниц, открытых пользователем, но может быть неверно для страниц, открытых с помощью **External. навигатетаскпанеурл**. Чтобы строка запроса версии была создана при программном переходе по, необходимо добавить параметр Version в вызов метода или динамически добавить версию к базовому URL-адресу элемента **navigate** в документе serviceInfo.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Динамическое создание документа ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External. Навигатетаскпанеурл**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Сведения, общие для типа 1 и 2 Интернет-магазинов**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




