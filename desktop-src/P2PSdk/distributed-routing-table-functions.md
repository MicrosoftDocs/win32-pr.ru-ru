---
description: В API таблицы распределенной маршрутизации (DRT) используются следующие функции.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Функции таблиц распределенной маршрутизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663351"
---
# <a name="distributed-routing-table-functions"></a>Функции таблиц распределенной маршрутизации

В API таблицы распределенной маршрутизации (DRT) используются следующие функции.

## <a name="lifetime-management-functions"></a>Функции управления жизненным циклом



| Функция                                           | Описание                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**дртопен**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Создает локальный экземпляр DRT с использованием критериев, заданных в структуре [**\_ параметров DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .  |
| [**дртклосе**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Закрывает и удаляет локальный экземпляр DRT.                                                              |
| [**дртжетевентдата**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Извлекает данные события, связанные с сигнальным событием.                                                         |
| [**дртжетевентдатасизе**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Возвращает размер структуры [**\_ \_ данных события DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) , связанной с сигнальным событием. |



 

## <a name="module-management-functions"></a>Функции управления модулями



| Функция                                                                           | Описание                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**дрткреатепнрпбутстрапресолвер**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Создает сопоставитель начальной загрузки на основе протокола PNRP.                                                                              |
| [**дртделетепнрпбутстрапресолвер**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Удаляет сопоставитель загрузчика на основе протокола PNRP.                                                                              |
| [**дрткреатеднсбутстрапресолвер**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Создает поставщик начальной загрузки, который будет обращаться к хорошо известному узлу по имени.                                                             |
| [**дртделетеднсбутстрапресолвер**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Удаляет поставщик начальной загрузки, который свяжется с известным узлом по имени.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Создает транспорт на основе протокола IPv6 UDP.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Удаляет транспорт на основе протокола IPv6 UDP.                                                                                   |
| [**дрткреатедериведкэйсекуритипровидер**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Создает поставщик безопасности производного ключа для DRT.                                                                                  |
| [**дрткреатедериведкэй**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Создает ключ, который можно использовать с помощью [**дртрегистеркэй**](/windows/desktop/api/drt/nf-drt-drtregisterkey) , когда DRT использует поставщик безопасности производного ключа. |
| [**дртделетедериведкэйсекуритипровидер**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Удаляет производный поставщик безопасности ключа для DRT.                                                                                  |
| [**дрткреатенуллсекуритипровидер**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Создает поставщик безопасности со значением NULL. Этому поставщику безопасности не требуются узлы для проверки подлинности ключей.                                 |
| [**дртделетенуллсекуритипровидер**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Удаляет поставщик безопасности со значением NULL.                                                                                                     |



 

## <a name="registration-functions"></a>Функции регистрации



| Функция                                     | Описание                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**дртрегистеркэй**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Регистрирует ключ в DRT.                                    |
| [**дртупдатекэй**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Обновляет данные приложения, связанные с зарегистрированным ключом. |
| [**дртунрегистеркэй**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Отменяет регистрацию ключа в DRT.                                |



 

## <a name="search-functions"></a>Функции поиска



| Функция                                                 | Описание                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**дртстартсеарч**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Выполняет поиск ключа в DRT, используя критерии, указанные в [**структуре \_ \_ сведений о поиске DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .                                                                                                      |
| [**дртконтинуесеарч**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Возобновляет поиск \_ \_ по пути поиска DRT \_ для ключа в DRT. Эта функция используется только в том случае, если флаг **фитеративе** имеет значение **true** в связанной [**структуре \_ \_ сведений о поиске DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) . |
| [**дртжетсеарчресулт**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Извлекает результаты поиска.                                                                                                                                                                                         |
| [**дртжетсеарчресултсизе**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Возвращает размер следующего доступного результата поиска.                                                                                                                                                                   |
| [**дртжетсеарчпас**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Возвращает список узлов, которые были обращены во время операции поиска.                                                                                                                                                          |
| [**дртжетсеарчпассизе**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Возвращает размер пути поиска, который представляет количество узлов, используемых в операции поиска.                                                                                                             |
| [**дртендсеарч**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Отменяет Поиск ключа в DRT, в результате чего возвращение результатов с помощью [**\_ \_ результатов поиска DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) останавливается. Этот API можно вызвать в любой точке после выполнения поиска.              |



 

## <a name="instance-name-functions"></a>Функции имени экземпляра



| Функция                                                 | Описание                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**дртжетинстанценаме**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Возвращает имя, связанное с экземпляром DRT.                    |
| [**дртжетинстанценамесизе**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Возвращает размер имени экземпляра таблицы распределенной маршрутизации. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Перечисление таблиц распределенной маршрутизации](distributed-routing-table-enumerations.md)
</dt> <dt>

[Структуры таблиц распределенной маршрутизации](distributed-routing-table-structures.md)
</dt> <dt>

[Справочник по распределенной маршрутизации API таблиц](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



