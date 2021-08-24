---
description: После того как вы разрабатываете исходный HTML-документ со страницей ссылки на события (ERP), необходимо присвоить ему имя, прежде чем сетевой монитор сможет отобразить его в Просмотр событий.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Именование страницы ссылки на события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569991c5e5ac24e18476fe27727f4fad1c310c8fd4e9439062fdf91bfb344005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799694"
---
# <a name="naming-an-event-reference-page"></a>Именование страницы ссылки на события

После того как вы разрабатываете исходный HTML-документ со страницей ссылки на события (ERP), необходимо присвоить ему имя, прежде чем сетевой монитор сможет отобразить его в Просмотр событий.

Файлы мониторинга имен и файловые ERP экспертов в следующем формате:

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**експертнаме**
</dt> <dd>

Имя файла DLL, за исключением расширения имени файла.

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**евентидент**
</dt> <dd>

Идентификатор события экспертного ERP.

Идентификатор события также находится в элементе **евентидент** структуры **нмевентдата** .

</dd> </dl>

Дополнительные сведения о создании ERP см. в следующих разделах:

-   [Создание страниц со ссылками на события экспертов и мониторинга](creating-expert-and-monitor-event-reference-pages.md)
-   [Создание страницы ссылки на событие](writing-an-event-reference-page.md)
-   [Тестирование страницы ссылки на событие](testing-an-event-reference-page.md)

 

 



