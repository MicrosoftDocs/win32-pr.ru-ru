---
title: Функции Bluetooth
description: Функции в этом разделе используются для управления устройствами и службами Bluetooth.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, ссылки, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5343f0d609185f3bb472570b8454931fc6a18b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487784"
---
# <a name="bluetooth-functions"></a>Функции Bluetooth

Функции в этом разделе используются для управления устройствами и службами Bluetooth.

Bluetooth также поддерживается с помощью программного интерфейса сокетов Windows. Дополнительные сведения о программировании Bluetooth с помощью интерфейса сокетов Windows см. в разделе [Поддержка сокетов Windows для Bluetooth](windows-sockets-support-for-bluetooth.md).



| Section                                                                                | Содержимое                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**блуетусаусентикатедевице**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | Отправляет запрос на проверку подлинности на удаленное устройство Bluetooth.                                                                                                                                 |
| [**блуетусаусентикатедевицеекс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | Отправляет запрос на проверку подлинности на удаленное устройство Bluetooth. Кроме того, эта функция позволяет передавать нестандартные данные в вызов функции для устройства, для которого выполняется проверка подлинности. |
| [**блуетусаусентикатемултипледевицес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | Позволяет вызывающему объекту запрашивать проверку подлинности нескольких устройств в рамках одного экземпляра мастера подключения Bluetooth.                                                            |
| [**блуетусдисплайдевицепропертиес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Вызывает вкладку свойств сведений об устройстве панели управления.                                                                                                                                  |
| [**блуетусенабледисковери**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | Изменяет состояние обнаружения для локального радиомодуля Bluetooth или радиостанций.                                                                                                                             |
| [**блуетусенаблеинкомингконнектионс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | Изменяет, принимает ли локальный радиомодуль Bluetooth входящие подключения.                                                                                                                        |
| [**блуетусенумератеинсталледсервицес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | Перечисляет идентификаторы GUID (глобальные уникальные идентификаторы) служб, включенных на устройстве Bluetooth.                                                                                    |
| [**блуетусфинддевицеклосе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Закрывает маркер перечисления, связанный с запросом устройства.                                                                                                                          |
| [**блуетусфиндфирстдевице**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | Начинает перечисление локальных устройств Bluetooth.                                                                                                                                            |
| [**блуетусфиндфирстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | Начинает перечисление локальных радиостанций Bluetooth.                                                                                                                                             |
| [**блуетусфинднекстдевице**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | Поиск следующего устройства Bluetooth.                                                                                                                                                              |
| [**блуетусфинднекстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | Поиск следующего радиомодуля Bluetooth.                                                                                                                                                               |
| [**блуетусфиндрадиоклосе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | Закрывает маркер перечисления, связанный с поиском радиомодулей Bluetooth.                                                                                                               |
| [**блуетусжетдевицеинфо**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | Извлекает сведения об удаленном устройстве Bluetooth. Устройство Bluetooth должно быть ранее определено с помощью успешного вызова функции запроса устройства.                           |
| [**блуетусжетрадиоинфо**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | Получение сведений о радиомодуле Bluetooth.                                                                                                                                                  |
| [**блуетусисконнектабле**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | Определяет, подключается ли радиостанции Bluetooth или радиоприемники.                                                                                                                                |
| [**блуетусисдисковерабле**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | Определяет, является ли радиомодуль Bluetooth или радиоприемники обнаруживаемыми.                                                                                                                               |
| [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | Регистрирует функцию обратного вызова, которая вызывается, когда конкретное устройство Bluetooth запрашивает проверку подлинности.                                                                                      |
| [**блуетусрегистерфораусентикатионекс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Регистрирует приложение для запроса ПИН-кода, числового сравнения и функции обратного вызова.                                                                                                         |
| [**блуетусремоведевице**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | Удаляет проверку подлинности между устройством Bluetooth и компьютером, удаляя все кэшированные данные об устройстве.                                                                          |
| [**блуетуссдпенуматтрибутес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Выполняет перечисление потока записи SDP и вызывает функцию обратного вызова для каждого атрибута в записи.                                                                                    |
| [**блуетуссдпжетаттрибутевалуе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Возвращает значение атрибута для идентификатора атрибута.                                                                                                                                    |
| [**блуетуссдпжетконтаинерелементдата**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Выполняет перебор потока контейнера и возвращает каждый элемент, содержащийся в элементе Container.                                                                                     |
| [**блуетуссдпжетелементдата**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Извлекает и анализирует один элемент из потока SDP.                                                                                                                                     |
| [**блуетуссдпжетстринг**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Преобразует необработанную строку, внедренную в запись SDP, в строку в Юникоде.                                                                                                               |
| [**блуетусселектдевицес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | Включает выбор устройств Bluetooth.                                                                                                                                                           |
| [**блуетусселектдевицесфри**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Освобождает ресурсы, связанные с предыдущим вызовом функции [**блуетусселектдевицес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices) .                                                                     |
| [**блуетуссендаусентикатионреспонсе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Вызывается при получении запроса на проверку подлинности для отправки ответа на ключ доступа.                                                                                                               |
| [**блуетуссендаусентикатионреспонсикс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Вызывается при получении запроса на проверку подлинности для отправки ответа на ключ или числового сравнения.                                                                                         |
| [**блуетуссетлокалсервицеинфо**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | Задает сведения о локальной службе для конкретного радиомодуля Bluetooth.                                                                                                                                |
| [**блуетуссетсервицестате**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | Включает или отключает службы для устройства Bluetooth.                                                                                                                                          |
| [**блуетусунрегистераусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Удаляет регистрацию для подпрограммы обратного вызова, которая ранее была зарегистрирована при вызове функции [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .      |
| [**блуетусупдатедевицерекорд**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | Обновляет кэш локального компьютера об устройстве Bluetooth.                                                                                                                                    |



 

 

 