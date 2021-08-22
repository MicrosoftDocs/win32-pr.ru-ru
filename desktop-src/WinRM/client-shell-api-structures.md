---
title: Структуры и определения API оболочки клиента
description: в следующей таблице приведены общие сведения о структурах и других определениях для API-интерфейса клиентской оболочки служба удаленного управления Windows (WinRM).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9c3d1f6f9f9d476e9b49ef309e5236e4421e0b5afa77fa1072b92f2060cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643264"
---
# <a name="client-shell-api-structures-and-definitions"></a>Структуры и определения API оболочки клиента

в следующей таблице приведены общие сведения о структурах и других определениях для API-интерфейса клиентской оболочки служба удаленного управления Windows (WinRM).



| Функция                                                                      | Описание                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_ \_ функция завершения оболочки \_ WSMan**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | Функция обратного вызова, которая вызывается для операций оболочки, что приводит к удаленному запросу. |



 



| Структура                                                                      | Описание                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_учетные данные проверки подлинности WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Определяет метод проверки подлинности и учетные данные, используемые для проверки подлинности сервера или прокси.                                              |
| [**\_данные WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Хранит входящие и исходящие данные, используемые в API WinRM.                                                                                     |
| [**\_ \_ двоичные данные WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Хранит двоичные данные для использования с различными функциями API WinRM.                                                                                |
| [**\_текст данных \_ WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Хранит текстовые данные для использования с различными функциями API WinRM.                                                                            |
| [**\_переменная окружения WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Определяет отдельную переменную среды с помощью пары "имя-значение".                                                                  |
| [**\_набор переменных окружения WSMan \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Определяет массив переменных среды.                                                                                                  |
| [**\_Ошибка WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Содержит сведения об ошибке.                                                                                                                 |
| [**\_ключ WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Представляет пару "ключ-значение" в наборе селектора и используется для обнаружения определенного ресурса.                                       |
| [**WSMAN, \_ параметр**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Представляет конкретное имя параметра и пару значений.                                                                                           |
| [**\_набор параметров \_ WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Представляет набор параметров.                                                                                                                |
| [**\_ \_ сведения о прокси WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Задает сведения о прокси-сервере для каждого сеанса.                                                                                                |
| [**\_результат получения \_ данных \_ WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Представляет выходные данные, полученные от API [**всманрецеивешеллаутпут**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput) .                                |
| [**\_данные ответа \_ WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Представляет выходные данные, полученные из операции [**WSMan**](wsman.md) .                                                                |
| [**\_набор селектора WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Определяет набор ключей, представляющих идентификатор ресурса.                                                                            |
| [**\_оболочка WSMan \_ Async**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Определяет асинхронную структуру, которая передается всем операциям оболочки.                                                                   |
| [**\_ \_ сведения об отключении оболочки WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | Подлежит уточнению                                                                                                                                         |
| [**\_ \_ сведения о запуске оболочки WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Хранит все данные, относящиеся к оболочке, которые необходимы для создания оболочки с помощью вызова подключаемого модуля [**всманкреатешелл**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) . |
| [**\_ \_ набор идентификаторов потока WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Перечисляет все потоки, используемые для ввода или вывода команд и.                                                  |
| [**учетные \_ пароли WSMan username \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Определяет учетные данные, используемые для проверки подлинности.                                                                                            |



 

 

 