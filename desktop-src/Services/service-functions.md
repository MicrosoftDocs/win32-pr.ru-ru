---
description: Следующие функции используются или реализуются службами.
ms.assetid: 63666848-cbac-4853-8b91-89303f9854c0
title: Функции службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55553e29b2ae9fb8e60db2f421fd8aa68cee1c6b79542c7d3d61ef5bcef490f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888966"
---
# <a name="service-functions"></a>Функции службы

Следующие функции используются или реализуются службами.



| Функция                                                             | Описание                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Обработке**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)                                           | Определяемая приложением функция обратного вызова, используемая с функцией [**регистерсервицектрлхандлер**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) .     |
| [**хандлерекс**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)                                       | Определяемая приложением функция обратного вызова, используемая с функцией [**регистерсервицектрлхандлерекс**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) . |
| [**регистерсервицектрлхандлер**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     | Регистрирует функцию для обработки запросов управления службами.                                                                              |
| [**регистерсервицектрлхандлерекс**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) | Регистрирует функцию для обработки расширенных запросов управления службами.                                                                     |
| [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)                                   | Определяемая приложением функция, которая выступает в качестве отправной точки для службы.                                                      |
| [**сетсервицебитс**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits)                             | Регистрирует тип службы с помощью диспетчера управления службами и службы сервера.                                                     |
| [**Сбой SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)                         | Обновляет сведения о состоянии диспетчера управления службами для вызывающей службы.                                                     |
| [**Сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)     | Подключает основной поток процесса службы к диспетчеру управления службами.                                                         |



 

Следующие функции используются программами, которые контролируют, настраивают или взаимодействуют со службами.



| Функция                                                                 | Описание                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)                       | Изменяет параметры конфигурации службы.                                                                                          |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)                     | Изменяет необязательные параметры конфигурации службы.                                                                                 |
| [**клосесервицехандле**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)                         | Закрывает указанный маркер объекту диспетчера управления службами или объекту службы.                                                        |
| [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)                                 | Отправляет управляющий код в службу.                                                                                                          |
| [**контролсервицеекс**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)                             | Отправляет управляющий код в службу.                                                                                                          |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)                                   | Создает объект службы и добавляет его в указанную базу данных диспетчера управления службами.                                                     |
| [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice)                                   | Помечает указанную службу для удаления из базы данных диспетчера управления службами.                                                         |
| [**енумдепендентсервицес**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa)                   | Извлекает имя и состояние каждой службы, зависящей от указанной службы.                                                        |
| [**енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)                     | Перечисляет службы в указанной базе данных диспетчера управления службами на основе указанного уровня информации.                             |
| [**жетсервицедисплайнаме**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)                   | Извлекает отображаемое имя указанной службы.                                                                                        |
| [**жетсервицекэйнаме**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea)                           | Возвращает имя службы указанной службы.                                                                                        |
| [**нотифибутконфигстатус**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                 | Сообщает состоянию загрузки диспетчеру управления службами.                                                                                     |
| [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea)           | Позволяет приложению принимать уведомления при создании или удалении указанной службы или изменении ее состояния.                 |
| [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)                                   | Устанавливает соединение с диспетчером управления службами на указанном компьютере и открывает указанную базу данных диспетчера управления службами. |
| [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)                                       | Открывает существующую службу.                                                                                                                  |
| [**куерисервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga)                         | Извлекает параметры конфигурации указанной службы.                                                                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)                       | Извлекает необязательные параметры конфигурации указанной службы.                                                                   |
| [**куерисервицединамиЦинформатион**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation) | Получает динамические сведения, связанные с запуском текущей службы.                                                                         |
| [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)    | Извлекает копию дескриптора безопасности, связанного с объектом службы.                                                               |
| [**куерисервицестатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)                     | Получает текущее состояние указанной службы на основе указанного уровня информации.                                             |
| [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity)        | Задает дескриптор безопасности объекта службы.                                                                                           |
| [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)                                     | Запускает службу.                                                                                                                           |



 

## <a name="obsolete-functions"></a>Устаревшие функции

Следующие функции являются устаревшими.<dl>

[**енумсервицесстатус**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa)  
[**локксервицедатабасе**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)  
[**куерисервицелоккстатус**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)  
[**куерисервицестатус**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)  
[**унлокксервицедатабасе**](/windows/desktop/api/Winsvc/nf-winsvc-unlockservicedatabase)  
</dl>

 

 
