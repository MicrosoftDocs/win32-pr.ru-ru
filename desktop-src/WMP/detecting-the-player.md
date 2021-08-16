---
title: Обнаружение проигрывателя
description: Обнаружение проигрывателя
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- проигрыватель Windows Media интернет-магазинов, обнаружение игроков
- Интернет-магазины, обнаружение игроков
- Тип 1 Интернет-магазины, обнаружение игроков
- Тип 2 Интернет-магазинов, обнаружение игроков
- проигрыватель Windows Media интернет-магазинов, обнаружение игрока
- Интернет-магазины, обнаружение игроков
- Тип 1 Интернет-магазины, обнаружение игрока
- Тип 2 Интернет-магазинов, обнаружение игрока
- Обнаружение игрока
- Обнаружение игроков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d511fc8c14a901c6823715293c5eb621b45762cd5e9fae78d8c4df503a03bf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863514"
---
# <a name="detecting-the-player"></a>Обнаружение проигрывателя

при создании веб-страницы для интернет-магазина вы можете решить, что пользователи должны иметь возможность просматривать страницу в браузере или в проигрыватель Windows Media. Вы можете использовать сценарий ASP, чтобы определить, размещена ли веб-страница в проигрывателе.

следующий пример кода извлекает параметр version из строки запроса URL-адреса, чтобы определить, размещена ли страница в проигрыватель Windows Media:


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



обратите внимание, что в приведенном выше коде предполагается, что параметр version существует в строке запроса при размещении в проигрыватель Windows Media. Это справедливо для страниц, открытых пользователем, но может быть неверно для страниц, открытых с помощью **External. навигатетаскпанеурл**. Чтобы строка запроса версии была создана при программном переходе по, необходимо добавить параметр Version в вызов метода или динамически добавить версию к базовому URL-адресу элемента **navigate** в документе serviceInfo.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Динамическое создание документа ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External. Навигатетаскпанеурл**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Сведения, общие для типа 1 и 2 Интернет-магазинов**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




