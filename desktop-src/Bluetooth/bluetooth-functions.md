---
title: Bluetooth Функции
description: функции в этом разделе используются для управления Bluetooth устройствами и службами.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, ссылки, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e8d945355b0bc25df4d91a96c30a4d20491eb3b0e86c3542e30c0f2b470833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701414"
---
# <a name="bluetooth-functions"></a>Bluetooth Функции

функции в этом разделе используются для управления Bluetooth устройствами и службами.

Bluetooth также поддерживается с помощью программного интерфейса сокетов Windows. дополнительные сведения о программировании Bluetooth с помощью интерфейса сокетов Windows см. в разделе [поддержка Windows сокетов для Bluetooth](windows-sockets-support-for-bluetooth.md).



| Section                                                                                | Содержимое                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**блуетусаусентикатедевице**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | отправляет запрос на проверку подлинности на удаленное устройство Bluetooth.                                                                                                                                 |
| [**блуетусаусентикатедевицеекс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | отправляет запрос на проверку подлинности на удаленное устройство Bluetooth. Кроме того, эта функция позволяет передавать нестандартные данные в вызов функции для устройства, для которого выполняется проверка подлинности. |
| [**блуетусаусентикатемултипледевицес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | позволяет вызывающему объекту запрашивать проверку подлинности нескольких устройств в рамках одного экземпляра мастера подключения Bluetooth.                                                            |
| [**блуетусдисплайдевицепропертиес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Вызывает вкладку свойств сведений об устройстве панели управления.                                                                                                                                  |
| [**блуетусенабледисковери**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | изменяет состояние обнаружения локальных Bluetooth радио или радио.                                                                                                                             |
| [**блуетусенаблеинкомингконнектионс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | изменяет, принимает ли локальный Bluetooth радио входящие подключения.                                                                                                                        |
| [**блуетусенумератеинсталледсервицес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | перечисляет идентификаторы guid (глобальные уникальные идентификаторы) служб, включенных на Bluetooth устройстве.                                                                                    |
| [**блуетусфинддевицеклосе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Закрывает маркер перечисления, связанный с запросом устройства.                                                                                                                          |
| [**блуетусфиндфирстдевице**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | начинает перечисление локальных Bluetooth устройств.                                                                                                                                            |
| [**блуетусфиндфирстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | начинает перечисление локальных Bluetooth радио.                                                                                                                                             |
| [**блуетусфинднекстдевице**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | поиск следующего устройства Bluetooth.                                                                                                                                                              |
| [**блуетусфинднекстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | поиск следующего Bluetooth радио.                                                                                                                                                               |
| [**блуетусфиндрадиоклосе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | закрывает маркер перечисления, связанный с поиском Bluetooth радио.                                                                                                               |
| [**блуетусжетдевицеинфо**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | извлекает сведения об удаленном Bluetooth устройстве. устройство Bluetooth должно быть ранее определено с помощью успешного вызова функции запроса устройства.                           |
| [**блуетусжетрадиоинфо**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | получение сведений о Bluetooth радио.                                                                                                                                                  |
| [**блуетусисконнектабле**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | определяет, подключается ли Bluetooth радио или радио.                                                                                                                                |
| [**блуетусисдисковерабле**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | определяет, будет ли обнаружено Bluetooth радио или радио.                                                                                                                               |
| [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | регистрирует функцию обратного вызова, которая вызывается, когда конкретное Bluetooth устройство запрашивает проверку подлинности.                                                                                      |
| [**блуетусрегистерфораусентикатионекс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Регистрирует приложение для запроса ПИН-кода, числового сравнения и функции обратного вызова.                                                                                                         |
| [**блуетусремоведевице**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | удаляет проверку подлинности между устройством Bluetooth и компьютером, удаляя все кэшированные данные об устройстве.                                                                          |
| [**блуетуссдпенуматтрибутес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Выполняет перечисление потока записи SDP и вызывает функцию обратного вызова для каждого атрибута в записи.                                                                                    |
| [**блуетуссдпжетаттрибутевалуе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Возвращает значение атрибута для идентификатора атрибута.                                                                                                                                    |
| [**блуетуссдпжетконтаинерелементдата**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Выполняет перебор потока контейнера и возвращает каждый элемент, содержащийся в элементе Container.                                                                                     |
| [**блуетуссдпжетелементдата**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Извлекает и анализирует один элемент из потока SDP.                                                                                                                                     |
| [**блуетуссдпжетстринг**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Преобразует необработанную строку, внедренную в запись SDP, в строку в Юникоде.                                                                                                               |
| [**блуетусселектдевицес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | позволяет выбрать Bluetooth устройства.                                                                                                                                                           |
| [**блуетусселектдевицесфри**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Освобождает ресурсы, связанные с предыдущим вызовом функции [**блуетусселектдевицес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices) .                                                                     |
| [**блуетуссендаусентикатионреспонсе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Вызывается при получении запроса на проверку подлинности для отправки ответа на ключ доступа.                                                                                                               |
| [**блуетуссендаусентикатионреспонсикс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Вызывается при получении запроса на проверку подлинности для отправки ответа на ключ или числового сравнения.                                                                                         |
| [**блуетуссетлокалсервицеинфо**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | задает сведения о локальной службе для конкретного Bluetooth радио.                                                                                                                                |
| [**блуетуссетсервицестате**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | включает или отключает службы для устройства Bluetooth.                                                                                                                                          |
| [**блуетусунрегистераусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Удаляет регистрацию для подпрограммы обратного вызова, которая ранее была зарегистрирована при вызове функции [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .      |
| [**блуетусупдатедевицерекорд**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | обновляет кэш локального компьютера о Bluetooth устройстве.                                                                                                                                    |



 

 

 