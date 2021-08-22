---
description: Сводка по потокам фильтров
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Сводка по потокам фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c151ed5fe69eea4cb0c81d01f43e97790b7223970791d3717adb9e15bea41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951743"
---
# <a name="summary-of-filter-threading"></a>Сводка по потокам фильтров

В потоке потоковой передачи вызываются следующие методы:

-   [**Имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**Имеминпутпин:: Рецеивемултипле**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**Ипин:: Невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [**Имемаллокатор:: buffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

В потоке приложения вызываются следующие методы:

-   Изменения состояния: [**ибасефилтер:: жоинфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**имедиафилтер::P Аусе**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**имедиафилтер:: останавливаться**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**икуалитиконтрол:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).
-   Ссылочное время: [**имедиафилтер:: жетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**Имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).
-   операции с закреплением: [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**ипин:: Подключение**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**ипин:: коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).
-   Функции распределителя: [**имеминпутпин:: распределителе**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**Имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).
-   Идет сброс: [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).

Этот список не является исчерпывающим. При реализации фильтра необходимо определить, какие методы изменяют состояние фильтра, и какие методы выполняют потоковые операции.

 

 



