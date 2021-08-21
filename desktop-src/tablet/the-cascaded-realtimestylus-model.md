---
description: Общие сведения о каскадной модели для класса RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Модель каскадного RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a69d7bb348485b1b53b04663faeaf9d4b38e1e6952b8b8305e755ff8d32677d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715474"
---
# <a name="the-cascaded-realtimestylus-model"></a>Модель каскадного RealTimeStylus

Каскадная модель [**RealTimeStylus**](realtimestylus-class.md) позволяет использовать два объекта **RealTimeStylus** , каждый из которых выполняется в другом потоке. В этой модели вы подключаете дополнительный объект **RealTimeStylus** к основному объекту **RealTimeStylus** . Дополнительный объект **RealTimeStylus** присоединяется как единственный асинхронный подключаемый модуль в асинхронной коллекции подключаемых модулей объекта **RealTimeStylus** .

Каскадная модель [**RealTimeStylus**](realtimestylus-class.md) может быть полезна в следующих сценариях.

-   Вы можете добавить определенные задачи, которые могут быть необходимы для вычисления, но по-прежнему требуют доступа в режиме реального времени к потоку данных пера планшета, такому как распознавание жестов многоштриха, в синхронную коллекцию подключаемых модулей объекта [**RealTimeStylus**](realtimestylus-class.md) .
-   Вычислительную нагрузку на синхронные подключаемые модули можно распределить по двум потокам, уменьшая задержки в сборе рукописных данных на некоторых планшетных ПК.

На следующей схеме показан поток данных пера планшета через два каскадных объекта [**RealTimeStylus**](realtimestylus-class.md) и их коллекции подключаемых модулей.

![Иллюстрация, показывающая каскадный поток данных RealTimeStylus](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

На этой схеме круг с буквой "A" представляет данные пера планшета, которые уже обработаны как в первичном, так и во вторичном объектах [**RealTimeStylus**](realtimestylus-class.md) и были помещены в очередь вывода дополнительного объекта **RealTimeStylus** . Кружок с буквой "B" представляет данные пера планшета, которые уже были обработаны основным объектом **RealTimeStylus** и добавлены в очередь **вывода основного объекта RealTimeStylus и** еще не отправлены в дополнительный объект **RealTimeStylus** . Кружок с буквой "C" представляет данные пера планшета, которые в настоящее время обрабатывает основной объект **RealTimeStylus** . Он отправляется в коллекцию синхронных подключаемых модулей и помещается в очередь вывода. Пустой кружок представляет позицию в очереди вывода, в которой добавляются будущие данные пера планшета.

## <a name="constraints"></a>Ограничения

При использовании конструктора [**RealTimeStylus**](realtimestylus-class.md) по умолчанию создается объект **RealTimeStylus** , который может принимать только входные данные другого объекта **RealTimeStylus** .

В следующем списке описаны ограничения, связанные с использованием каскадной модели [**RealTimeStylus**](realtimestylus-class.md) .

-   Можно использовать только два объекта [**RealTimeStylus**](realtimestylus-class.md) **: основной и дополнительный объекты** **RealTimeStylus** .
-   Основной объект [**RealTimeStylus**](realtimestylus-class.md) должен быть создан с помощью конструктора, использующего параметр **аттачедконтрол** или *Handle* . Дополнительный объект **RealTimeStylus** должен быть создан с помощью конструктора без аргументов.
-   Дополнительный объект [**RealTimeStylus**](realtimestylus-class.md) должен быть единственным асинхронным подключаемым модулем в асинхронной коллекции подключаемых модулей объекта **RealTimeStylus** .
-   Дополнительный объект [**RealTimeStylus**](realtimestylus-class.md) может быть присоединен только к одному первичному объекту **RealTimeStylus** за раз. Если он добавляется во второй Первичный объект **RealTimeStylus** , метод [Add](/previous-versions/ms824814(v=msdn.10)) создает исключение, а дополнительный объект **RealTimeStylus** не присоединяется к второму основному объекту **RealTimeStylus** .
-   Происходит изменение поведения некоторых членов объекта [**RealTimeStylus**](realtimestylus-class.md) . В следующей таблице описывается измененное поведение этих элементов.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Член</th>
    <th>Поведение</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><a href="/previous-versions/ms825905(v=msdn.10)">жетдесиредпаккетдескриптион</a></td>
    <td>Этот метод возвращает сведения из основного объекта <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> .<br/> Если дополнительный объект <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> не присоединен к основному объекту <strong>RealTimeStylus</strong> , этот метод возвращает значение по умолчанию.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms826041(v=msdn.10)">сетдесиредпаккетдескриптион</a></td>
    <td>Этот метод вызывает исключение <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .<br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms825913(v=msdn.10)">Перо</a></td>
    <td>Этот метод возвращает сведения из основного объекта <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> .<br/> Если дополнительный объект <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> не присоединен к основному объекту <strong>RealTimeStylus</strong> , этот метод возвращает пустой массив.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms824832(v=msdn.10)">Включен</a></td>
    <td>Получение этого свойства возвращает сведения из основного объекта <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> .<br/> Если дополнительный объект <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> не присоединен к основному объекту <strong>RealTimeStylus</strong> , то получение этого свойства возвращает значение по умолчанию.<br/>
    <blockquote>
    [!Note]<br />
Задание этого свойства вызывает исключение <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms824834(v=msdn.10)">виндовинпутректангле</a></td>
    <td>Получение этого свойства возвращает сведения из основного объекта <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> .<br/> Если дополнительный объект <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> не присоединен к основному объекту <strong>RealTimeStylus</strong> , то получение этого свойства возвращает значение по умолчанию.<br/>
    <blockquote>
    [!Note]<br />
Задание этого свойства вызывает исключение <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   Родительский объект [**RealTimeStylus**](realtimestylus-class.md) должен перестать работать при удалении дочернего объекта **RealTimeStylus** .

 

 
