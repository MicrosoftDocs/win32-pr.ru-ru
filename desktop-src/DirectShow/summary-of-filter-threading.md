---
description: Сводка по потокам фильтров
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Сводка по потокам фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a7c4ce19c46a0f7b05db3cb4d82e8f2aa0beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674338"
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
-   Операции закрепления: [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**Ипин:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**Ипин:: Коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**Ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).
-   Функции распределителя: [**имеминпутпин:: распределителе**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**Имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).
-   Идет сброс: [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).

Этот список не является исчерпывающим. При реализации фильтра необходимо определить, какие методы изменяют состояние фильтра, и какие методы выполняют потоковые операции.

 

 



