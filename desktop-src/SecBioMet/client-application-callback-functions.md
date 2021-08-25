---
title: Функции обратного вызова клиентских приложений
description: Два типа сигнатур обратного вызова.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3e052df1821a5fd85bbba4ebbea3e6672d9e625b7d4258110fb19a5c234f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977104"
---
# <a name="client-application-callback-functions"></a>Функции обратного вызова клиентских приложений

биометрическая платформа Windows поддерживает два типа сигнатур ответного вызова. начиная с Windows 8, поддерживается следующий обратный вызов. Рекомендуется реализовать этот обратный вызов для всех новых приложений. однако этот обратный вызов не может использоваться в Windows 7.



| Обратный вызов                                                                                     | Описание                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ обратный вызов асинхронного завершения пвинбио \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Уведомляет клиентское приложение о том, что асинхронная операция, запущенная с помощью [**винбиоасинкопенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) или [**винбиоасинкопенфрамеворк**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) , завершилась.<br/> |



 

в Windows 7 появились следующие функции обратного вызова. не рекомендуется реализовывать их для новых приложений, предназначенных для Windows 8 и более поздних операционных систем.



| Обратный вызов                                                                                 | Описание                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ обратный вызов записи пвинбио**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Возвращает результаты асинхронной функции [**винбиокаптуресамплевискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .<br/> |
| [**\_ \_ обратный вызов записи регистрации пвинбио \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Возвращает результаты асинхронной функции [**винбиоенроллкаптуревискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .<br/> |
| [**\_ \_ обратный вызов события пвинбио**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Возвращает результаты асинхронной функции [**винбиорегистеревентмонитор**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .<br/>           |
| [**\_ \_ обратный вызов пвинбио Identify**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Возвращает результаты асинхронной функции [**винбиоидентифивискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .<br/>           |
| [**ПВИНБИОный \_ \_ \_ обратный вызов датчика**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Возвращает результаты асинхронной функции [**винбиолокатесенсорвискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .<br/>   |
| [**\_ \_ обратный вызов пвинбио проверки**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Возвращает результаты асинхронной функции [**винбиоверифивискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .<br/>               |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по клиентскому приложению](client-application-reference.md)
</dt> </dl>

 

 





