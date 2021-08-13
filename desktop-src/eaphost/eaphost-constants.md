---
title: Константы EAPHost (Еаптипес. h)
description: Просмотрите список констант EAPHost (Еаптипес. h), используемых методами EAPHost, и ознакомьтесь с требованиями к их использованию.
ms.assetid: 56338B98-06E3-4CD3-B1CA-F8F45AA39566
topic_type:
- apiref
api_name:
- EAP_INTERACTIVE_UI_DATA_VERSION
- EAP_CREDENTIAL_VERSION
- EAPHOST_PEER_API_VERSION
- CERTIFICATE_HASH_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH
- EAP_UI_INPUT_FIELD_PROPS_DEFAULT
- EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT
- EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST
- EAP_UI_INPUT_FIELD_PROPS_READ_ONLY
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab336b147557722f1bec72bfe662b12599a64ee1622b31bdad6a92a05af6d92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119483014"
---
# <a name="eaphost-constants"></a>Константы EAPHost

Константы, используемые методами EAPHost.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**\_интерактивная \_ \_ версия данных пользовательского \_ интерфейса EAP**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Версия интерактивных данных пользовательского интерфейса EAP.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**\_версия учетных данных EAP \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Версия учетных данных EAP, предоставленных пользователем.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**\_версия однорангового \_ API EAPHOST \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Версия однорангового API EAPHost.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**\_Длина ХЭША \_ сертификата**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Длина хэша SHA1 сертификата.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**Максимальная \_ \_ \_ длина входного \_ поля \_ конфигурации EAP**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Задает максимальную поддерживаемую длину поля ввода.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**Максимальная \_ \_ \_ \_ \_ Длина значения входного поля конфигурации EAP \_**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



Задает максимальную поддерживаемую длину поля ввода.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**свойства \_ \_ \_ \_ \_ по умолчанию для поля ввода пользовательского интерфейса EAP**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista с пакетом обновления 1 (SP1) или более поздней версии: представляет значение свойства по умолчанию для записей полей ввода в пользовательском интерфейсе.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**свойства \_ \_ \_ \_ \_ по умолчанию для поля ввода конфигурации EAP**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Представляет значение свойства по умолчанию для записей поля ввода конфигурации, отображаемых в пользовательском интерфейсе.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**Свойства "Свойства" для \_ поля ввода пользовательского интерфейса EAP \_ \_ не удается \_ \_ \_ воспроизвести**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista с пакетом обновления 1 (SP1) или более поздней версии: указывает, что записи полей ввода не будут отображаться в пользовательском интерфейсе (например, пароль или PIN-код).


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**\_НЕотображаемые свойства \_ свойств входного \_ поля конфигурации \_ \_ EAP \_**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Указывает, что записи полей ввода конфигурации не будут отображаться в пользовательском интерфейсе (например, пароль или PIN-код).


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**свойства \_ свойств для поля ввода пользовательского интерфейса EAP \_ \_ \_ \_ не \_ сохранены**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista с пакетом обновления 1 (SP1) или более поздней версии: указывает, что метод EAP не будет кэшировать данные поля; запрашивающий объект должен кэшировать данные поля для роуминга.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**свойства \_ поля ввода пользовательского интерфейса EAP \_ \_ \_ \_ доступны \_ только для чтения**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista с пакетом обновления 1 (SP1) или более поздней версии: указывает, что поле ввода доступно только для чтения и не может быть изменено.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows 8 \[ только классические приложения\]<br/> |
| Сервер<br/> | Windows Server 2012 \[ только классические приложения\]<br/> |



 

 





