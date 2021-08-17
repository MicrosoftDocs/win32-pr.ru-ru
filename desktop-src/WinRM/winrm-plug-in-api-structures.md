---
title: Структуры API подключаемых модулей WinRM
description: Структуры API подключаемых модулей WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a57cbc31ae19bd858a191cec827760d055a87fc7ca19b134f61b17f8fd065e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742774"
---
# <a name="winrm-plug-in-api-structures"></a>Структуры API подключаемых модулей WinRM

в следующей таблице приведены общие сведения о структурах в интерфейсе прикладного программирования (API) подключаемого модуля служба удаленного управления Windows (WinRM).



| Структура                                                        | Описание                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**\_Квота на авторизацию WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | Определяет сведения о квотах для каждого пользователя.                                           |
| [**\_сведения о сертификате WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | Представляет поля в сертификате клиента.                                     |
| [**\_ \_ набор аргументов команды \_ WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | Представляет набор аргументов, передаваемых в командную строку.                  |
| [**\_Фильтр WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | Определяет фильтрацию, используемую для операции.                                             |
| [**\_фрагмент WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | Определяет сведения о фрагменте для операции.                                       |
| [**\_ \_ сведения о операции WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | Представляет конкретную конечную точку ресурса, для которой подключаемый модуль должен выполнить запрос. |
| [**\_запрос подключаемого модуля WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | Содержит сведения о запросе и передается в каждую операцию подключаемого модуля.       |
| [**\_ \_ сведения об отправителе WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | Указывает сведения о клиенте для каждого входящего запроса.                                      |



 

 

 




