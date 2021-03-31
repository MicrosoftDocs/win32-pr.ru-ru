---
title: Функции обратного вызова клиентских приложений
description: Два типа сигнатур обратного вызова.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411251"
---
# <a name="client-application-callback-functions"></a>Функции обратного вызова клиентских приложений

Биометрическая платформа Windows поддерживает два типа сигнатур ответного вызова. Начиная с Windows 8, поддерживается следующий обратный вызов. Рекомендуется реализовать этот обратный вызов для всех новых приложений. Однако этот обратный вызов не может использоваться в Windows 7.



| Обратный вызов                                                                                     | Описание                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ обратный вызов асинхронного завершения пвинбио \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Уведомляет клиентское приложение о том, что асинхронная операция, запущенная с помощью [**винбиоасинкопенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) или [**винбиоасинкопенфрамеворк**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) , завершилась.<br/> |



 

В Windows 7 появились следующие функции обратного вызова. Не рекомендуется реализовывать их для новых приложений, предназначенных для операционных систем Windows 8 и более поздних версий.



| Обратный вызов                                                                                 | Описание                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ обратный вызов записи пвинбио**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Возвращает результаты асинхронной функции [**винбиокаптуресамплевискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .<br/> |
| [**\_ \_ обратный вызов записи регистрации пвинбио \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Возвращает результаты асинхронной функции [**винбиоенроллкаптуревискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .<br/> |
| [**\_ \_ обратный вызов события пвинбио**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Возвращает результаты асинхронной функции [**винбиорегистеревентмонитор**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .<br/>           |
| [**\_ \_ обратный вызов пвинбио Identify**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Возвращает результаты асинхронной функции [**винбиоидентифивискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .<br/>           |
| [**ПВИНБИОный \_ \_ \_ обратный вызов датчика**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Возвращает результаты асинхронной функции [**винбиолокатесенсорвискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .<br/>   |
| [**\_ \_ обратный вызов пвинбио проверки**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Возвращает результаты асинхронной функции [**винбиоверифивискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .<br/>               |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по клиентскому приложению](client-application-reference.md)
</dt> </dl>

 

 





