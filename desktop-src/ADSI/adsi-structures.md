---
title: Структуры ADSI
description: Интерфейсы служб Active Directory (ADSI) определяют и используют структуры, перечисленные в следующей таблице.
ms.assetid: 3ee0e469-9932-4135-8798-27d318011786
ms.tgt_platform: multiple
keywords:
- Интерфейсы ADSI ADSI, ссылки, структуры
- структуры ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f35ba74f0334e8b66329d8f526266c315056af9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132810"
---
# <a name="adsi-structures"></a>Структуры ADSI

Интерфейсы служб Active Directory (ADSI) определяют и используют структуры, перечисленные в следующей таблице.



| Структура                                                                      | Описание                                                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**AD \_ attr, \_ DEF**](/windows/desktop/api/Iads/ns-iads-ads_attr_def)<br/>                              | Описывает набор определений атрибутов объекта **attributeSchema** .<br/>                          |
| [**\_ \_ сведения о attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)<br/>                            | Содержит значение именованного атрибута и указывает операции для изменения атрибута.<br/>              |
| [**ADS \_ посмотрите**](/windows/win32/api/iads/ns-iads-ads_backlink)<br/>                               | Представляет представление ADSI атрибута **ссылки назад** .<br/>                                   |
| [**\_список ADS касеигноре \_**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)<br/>                | Представляет представление в ADSI атрибута **списка игнорируемых вариантов** .<br/>                            |
| [**\_класс ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_class_def)<br/>                            | Описывает данные схемы для объекта.<br/>                                                                |
| [**\_DN AD \_ с \_ двоичными данными**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)<br/>                 | Структура, определяемая интерфейсом ADSI, которая сопоставляет различающееся имя с **идентификатором GUID** объекта.<br/>                     |
| [**\_DN AD \_ со \_ строкой**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)<br/>                 | Структура, определяемая интерфейсом ADSI, которая сопоставляет различающееся имя объекта с неизменяемым строковым значением.<br/> |
| [**\_Электронная почта ADS**](/windows/win32/api/iads/ns-iads-ads_email)<br/>                                     | Представляет представление ADSI атрибута **электронной почты** .<br/>                                       |
| [**ADS \_ факснумбер**](/windows/win32/api/iads/ns-iads-ads_faxnumber)<br/>                             | Представляет представление ADSI атрибута **телефонного номера факса** .<br/>                  |
| [**\_удержание рекламы**](/windows/win32/api/iads/ns-iads-ads_hold)<br/>                                       | Представляет представление ADSI атрибута **удержания** .<br/>                                        |
| [**ADS \_ нетаддресс**](/windows/win32/api/iads/ns-iads-ads_netaddress)<br/>                           | Представляет представление ADSI атрибута **net Address** .<br/>                                 |
| [**\_ \_ дескриптор безопасности AD \_ ADS**](/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor)<br/> | Описывает дескриптор безопасности.<br/>                                                                    |
| [**\_ \_ сведения об объекте ADS**](/windows/desktop/api/Iads/ns-iads-ads_object_info)<br/>                        | Описывает данные объекта службы каталогов.<br/>                                                            |
| [**\_список октетов ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)<br/>                          | Представляет представление ADSI атрибута **списка октетов** .<br/>                                  |
| [**\_Строка октета ADS \_**](/windows/win32/api/iads/ns-iads-ads_octet_string)<br/>                      | Представляет представление ADSI атрибута **строки октета** .<br/>                                |
| [**\_путь AD**](/windows/win32/api/iads/ns-iads-ads_path)<br/>                                       | Представляет представление ADSI атрибута **path** .<br/>                                        |
| [**ADS \_ посталаддресс**](/windows/win32/api/iads/ns-iads-ads_postaladdress)<br/>                     | Представляет представление в ADSI атрибута **почтового адреса** .<br/>                              |
| [**\_Специальные ADS Prov \_**](/windows/win32/api/iads/ns-iads-ads_prov_specific)<br/>                    | Описывает тип данных, зависящий от поставщика.<br/>                                                            |
| [**ADS \_ репликапоинтер**](/windows/win32/api/iads/ns-iads-ads_replicapointer)<br/>                   | Представляет представление ADSI атрибута указателя реплики.<br/>                                 |
| [**\_столбец поиска баннеров \_**](/windows/desktop/api/Iads/ns-iads-ads_search_column)<br/>                    | Представляет столбец, полученный в результате запроса к каталогу.<br/>                                               |
| [**\_ \_ сведения о ads сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)<br/>                | Описывает параметры запроса.<br/>                                                                        |
| [**ADS — \_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)<br/>                                 | Описывает ключ сортировки, используемый для сортировки запроса.<br/>                                                    |
| [**\_Метка времени ADS**](/windows/win32/api/iads/ns-iads-ads_timestamp)<br/>                             | Представляет представление в ADSI атрибута **timestamp** .<br/>                                   |
| [**ADS \_ типеднаме**](/windows/win32/api/iads/ns-iads-ads_typedname)<br/>                             | Представляет представление в ADSI атрибута **типизированного имени** .<br/>                                  |
| [**адсвалуе**](/windows/desktop/api/Iads/ns-iads-adsvalue)<br/>                                        | Описывает значение типа данных ADSI.<br/>                                                           |
| [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)<br/>                                         | Указывает, что виртуальное представление списка должно использоваться при возврате результатов поиска с сервера.<br/>  |



 

 

 





