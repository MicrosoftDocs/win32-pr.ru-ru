---
description: Объекты потоковой передачи мультимедиа
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Объекты потоковой передачи мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfefd7d16c832dc168204df771ff8f925bec3f1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471950"
---
# <a name="multimedia-streaming-objects"></a>Объекты потоковой передачи мультимедиа

> [!Note]  
> Это нерекомендуемый API. Новые приложения не должны использовать его.

 

В следующей таблице описаны объекты потоковой передачи мультимедиа.




| CLSID | Описание | Поддерживаемые интерфейсы | 
|-------|-------------|----------------------|
| CLSID_AMMediaTypeStream | может создавать образцы мультимедиа для любого типа данных, поддерживаемого DirectShow | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>иаммедиастреам</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>имедиастреам</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></li></ul> | 
| CLSID_AMAudioData | Реализация объекта <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>иаудиодата</strong></a> Audio Container. | <ul><li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>иаудиодата</strong></a></li></ul> | 
| CLSID_AMDirectDrawStream | поток мультимедиа DirectDraw, который можно добавить в поток мультимедиа DirectShow. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>иаммедиастреам</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>имедиастреам</strong></a></li><li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>идиректдравмедиастреам</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></li></ul> | 
| CLSID_AMMultiMediaStream | DirectShow реализации потока мультимедиа. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>иаммултимедиастреам</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>имултимедиастреам</strong></a></li></ul> | 
| CLSID_MediaStreamFilter | Предоставляет функции потоковой передачи мультимедиа для объекта CLSID_AMMultiMediaStream через интерфейс <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>иаммултимедиастреам</strong></a> . | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></li></ul> | 
| Недоступно | Примеры, созданные объектом CLSID_AMMediaTypeStream. | <ul><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>истреамсампле</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>имедиасампле</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li></ul> | 
| Недоступно | Примеры, созданные потоком DirectDraw. | <ul><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>истреамсампле</strong></a></li><li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>идиректдравстреамсампле</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>имедиасампле</strong></a></li></ul> | 




 

 

 



