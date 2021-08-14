---
title: Точки входа подключаемого модуля авторизации
description: Точки входа подключаемого модуля авторизации
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16ca861df6b6546920aaf3f778c61117776ff3861556377b280c990c03711fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324082"
---
# <a name="authorization-plug-in-entry-points"></a>Точки входа подключаемого модуля авторизации

подключаемые модули авторизации настраиваются только для хост-процесса службы IIS (IIS). Для каждого виртуального каталога можно настроить только один подключаемый модуль авторизации.

Все подключаемые модули авторизации должны поддерживать следующие точки входа:

-   [**всманплугинстартуп**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**всманплугиншутдовн**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**всманплугинаусзусер**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**всманплугинаусзоператион**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

Следующая точка входа является необязательной:

-   [**всманплугинаусзкуерикуота**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

в следующей таблице приведены общие сведения о точках входа подключаемого модуля авторизации в интерфейсе API подключаемого модуля служба удаленного управления Windows (WinRM).



| Функция                                                                                      | Описание                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Операция авторизации подключаемого модуля WSMan \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Вызывается для авторизации определенной операции. <br/> Имя точки входа библиотеки DLL для этого метода должно быть [**всманплугинаусзоператион**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation).<br/>                                                                                                                                                                                                       |
| [**\_ \_ \_ Квота запроса авторизации ПОДКЛЮЧАЕМого модуля WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Вызывается после того, как соединение получает разрешение на получение сведений о квотах для пользователя. <br/> Имя точки входа библиотеки DLL для этого метода должно быть [**всманплугинаусзкуерикуота**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota).<br/>                                                                                                                                                    |
| [**\_подключаемый модуль WSMan \_ авторизовать \_ \_ контекст выпуска**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Вызывается для освобождения контекста, в котором подключаемые модули отчитывается от методов [**всманплугинаусзусеркомплете**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) или [**всманплугинаусзоператионкомплете**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) . <br/> Имя точки входа библиотеки DLL для этого метода должно быть [**всманплугинаусзрелеасеконтекст**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context).<br/> |
| [**\_подключаемый модуль WSMan \_ авторизовать \_ пользователя**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Вызывается, чтобы определить, разрешено ли пользователю выполнять запрос. <br/> Имя точки входа библиотеки динамической компоновки (DLL) для этого метода должно быть [**всманплугинаусзусер**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user).<br/>                                                                                                                                                            |



 

 

