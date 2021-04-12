---
title: Структуры API подключаемых модулей WinRM
description: Структуры API подключаемых модулей WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331280"
---
# <a name="winrm-plug-in-api-structures"></a>Структуры API подключаемых модулей WinRM

В следующей таблице приведены общие сведения о структурах в интерфейсе прикладного программирования (API) подключаемого модуля служба удаленного управления Windows (WinRM).



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



 

 

 




