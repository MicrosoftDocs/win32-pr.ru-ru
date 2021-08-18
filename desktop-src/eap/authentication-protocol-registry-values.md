---
title: Значения реестра протокола проверки подлинности
description: Программа установки для DLL-библиотеки EAP может создать следующие значения реестра, приведенные ниже еаптипеид.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0822e7abb62aad136a3abbe36ee92f5b6f1ec9fbeabd6426c039f05c1f752d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739564"
---
# <a name="authentication-protocol-registry-values"></a>Значения реестра протокола проверки подлинности

Программа установки для DLL-библиотеки EAP может создать следующие значения реестра, приведенные ниже **&lt; еаптипеид &gt;**. Эти значения реестра определены в файле заголовка Расеапиф. h. Значения **RAS_EAP_VALUENAME_PATH** и **RAS_EAP_VALUENAME_FRIENDLY_NAME** являются обязательными. Программа установки может также создавать и другие ключи и значения. Они могут использоваться самим протоколом проверки подлинности. Дополнительные сведения и пример настройки реестра см. в разделе [Пример значений реестра](registry-values-example.md).

[RAS_EAP_VALUENAME_PATH](#ras_eap_valuename_path)

[RAS_EAP_VALUENAME_FRIENDLY_NAME](#ras_eap_valuename_friendly_name)

[RAS_EAP_VALUENAME_CONFIGUI](#ras_eap_valuename_configui)

[RAS_EAP_VALUENAME_DEFAULT_DATA](#ras_eap_valuename_default_data)

[RAS_EAP_VALUENAME_REQUIRE_CONFIGUI](#ras_eap_valuename_require_configui)

[RAS_EAP_VALUENAME_CONFIG_CLSID](#ras_eap_valuename_config_clsid)

[RAS_EAP_VALUENAME_IDENTITY](#ras_eap_valuename_identity)

[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Сохранении

[RAS_EAP_VALUENAME_INVOKE_NAMEDLG](#ras_eap_valuename_invoke_namedlg)

[RAS_EAP_VALUENAME_INVOKE_PWDDLG](#ras_eap_valuename_invoke_pwddlg)

[RAS_EAP_VALUENAME_ENCRYPTION](#ras_eap_valuename_encryption)

[RAS_EAP_VALUENAME_STANDALONE_SUPPORTED](#ras_eap_valuename_standalone_supported)

[RAS_EAP_VALUENAME_ROLES_SUPPORTED](#ras_eap_valuename_roles_supported)

[RAS_EAP_VALUENAME_PER_POLICY_CONFIG](#ras_eap_valuename_per_policy_config)

[RAS_EAP_VALUENAME_ISTUNNEL_METHOD](#ras_eap_valuename_istunnel_method)

[RAS_EAP_VALUENAME_FILTER_INNERMETHODS](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a>RAS_EAP_VALUENAME_PATH

| Константа | Путь                               |
|----------------|------------------------------------|
| Тип           | REG_EXPAND_SZ                    |
| Описание    | Указывает путь к DLL-библиотеке EAP. |

## <a name="ras_eap_valuename_friendly_name"></a>RAS_EAP_VALUENAME_FRIENDLY_NAME

| Константа | FriendlyName                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_SZ                                                                                                                                                           |
| Описание    | Указывает понятное имя для протокола проверки подлинности. Это имя отображается в пользовательском интерфейсе приложения EAP для реализаций удаленного доступа и беспроводной связи. |

## <a name="ras_eap_valuename_configui"></a>RAS_EAP_VALUENAME_CONFIGUI

| Константа | конфигуипас                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_EXPAND_SZ                                                                                                                   |
| Описание    | Указывает путь к библиотеке DLL, реализующей пользовательский интерфейс конфигурации на клиенте, так как этот пользовательский интерфейс предназначен только для клиента. |

## <a name="ras_eap_valuename_default_data"></a>RAS_EAP_VALUENAME_DEFAULT_DATA

| Константа | конфигдата                                                            |
|----------------|-----------------------------------------------------------------------|
| Тип           | REG_BINARY                                                           |
| Описание    | Указывает данные конфигурации по умолчанию для протокола проверки подлинности. |

## <a name="ras_eap_valuename_require_configui"></a>RAS_EAP_VALUENAME_REQUIRE_CONFIGUI

| Константа | рекуиреконфигуи                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_DWORD                                                                                                                                                                                                                                               |
| Описание    | Указывает, должен ли пользователь предоставлять данные конфигурации в пользовательском интерфейсе клиентского приложения EAP. Если это значение равно 1, пользователь не может выйти из пользовательского интерфейса клиентского приложения EAP без предоставления данных конфигурации. Значение по умолчанию — 0. |

## <a name="ras_eap_valuename_config_clsid"></a>RAS_EAP_VALUENAME_CONFIG_CLSID

| Константа | конфигклсид                                                   |
|----------------|---------------------------------------------------------------|
| Тип           | REG_SZ                                                       |
| Описание    | Указывает идентификатор класса пользовательского интерфейса конфигурации на сервере. |

## <a name="ras_eap_valuename_identity"></a>RAS_EAP_VALUENAME_IDENTITY

| Константа | идентитипас                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_EXPAND_SZ                                                                                                                        |
| Описание    | Указывает путь к библиотеке DLL, которая реализует функции для получения удостоверения пользователя на клиенте, так как этот пользовательский интерфейс предназначен только для клиента. |

## <a name="ras_eap_valuename_interactiveui"></a>RAS_EAP_VALUENAME_INTERACTIVEUI

| Константа | интерактивеуипас                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_EXPAND_SZ                                                                                                                 |
| Описание    | Указывает путь к библиотеке DLL, которая реализует интерактивный пользовательский интерфейс на клиенте, так как этот пользовательский интерфейс предназначен только для клиента. |

## <a name="ras_eap_valuename_invoke_namedlg"></a>RAS_EAP_VALUENAME_INVOKE_NAMEDLG

| Константа | инвокеусернамедиалог                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_DWORD                                                                                                                                                                                             |
| Описание    | указывает, должен ли RAS отображать стандартное диалоговое окно Windows NT/Windows 2000 (значение 1) или вызывать [**расеапжетидентити**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (значение 0). Значение по умолчанию — 1. |

## <a name="ras_eap_valuename_invoke_pwddlg"></a>RAS_EAP_VALUENAME_INVOKE_PWDDLG

| Константа | инвокепассворддиалог                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_DWORD                                                                                                                                                                                  |
| Описание    | указывает, должен ли RAS отображать стандартное диалоговое окно пароля Windows NT/Windows 2000. Если это значение существует и равно 0, служба RAS не будет отображать диалоговое окно пароля. Значение по умолчанию — 1. |


## <a name="ras_eap_valuename_encryption"></a>RAS_EAP_VALUENAME_ENCRYPTION

| Константа | мппинкриптионсуппортед                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_DWORD                                                                                                                                                                                    |
| Описание    | Если это значение равно 1, протокол проверки подлинности может создавать ключи для шифрования с шифрованием типа "точка — точка" (MPPE). Возможные значения: 0 или 1. Значение по умолчанию — 0. |

## <a name="ras_eap_valuename_standalone_supported"></a>RAS_EAP_VALUENAME_STANDALONE_SUPPORTED

| Константа | стандалонесуппортед                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_DWORD                                                                                                                                                                     |
| Описание    | указывает, поддерживается ли этот протокол проверки подлинности на автономном сервере Windows 2000. Значение 0 указывает, что протокол EAP не поддерживается. Значение по умолчанию — 1. |

## <a name="ras_eap_valuename_roles_supported"></a>RAS_EAP_VALUENAME_ROLES_SUPPORTED

| Постоянное значение | ролессуппортед                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип           | REG_DWORD                                                                                                                                                                                                                                 |
| Описание    | Указывает различные роли, поддерживаемые EAP. Указывает, можно ли использовать на сервере или клиенте, поддерживается ли он для подключений RAS (VPN) или PEAP. Поведение по умолчанию — отображение метода EAP в протоколе PEAP и в протоколе EAP. |

## <a name="ras_eap_valuename_per_policy_config"></a>RAS_EAP_VALUENAME_PER_POLICY_CONFIG

| Постоянное значение | перполициконфиг |
|----------------|-----------------|
| Тип           | REG_DWORD      |
| Описание    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a>RAS_EAP_VALUENAME_ISTUNNEL_METHOD

Это значение реестра не используется.

## <a name="ras_eap_valuename_filter_innermethods"></a>RAS_EAP_VALUENAME_FILTER_INNERMETHODS

Это значение реестра не используется.

