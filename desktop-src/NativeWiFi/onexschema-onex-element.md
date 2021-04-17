---
description: Указывает сведения о конфигурации 802.1 X для профиля проводной или беспроводной локальной сети.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: OneX, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663045"
---
# <a name="onex-element"></a>OneX, элемент

Элемент OneX указывает сведения о конфигурации 802.1 X для профиля проводной или беспроводной локальной сети. Этот элемент является уникальным корневым элементом для профиля 802.1 X.

Целевым пространством имен для элемента OneX является `https://www.microsoft.com/networking/OneX/v1` . Большинство дочерних элементов элемента OneX находятся в `OneX` пространстве имен. Существует одно исключение: элемент [**еапконфиг**](onexschema-eapconfig-onex-element.md) находится в `https://www.microsoft.com/provisioning/EapHostConfig` пространстве имен.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Поддерживается только элемент [**еапконфиг**](onexschema-eapconfig-onex-element.md) . Другие элементы, если они есть в профиле, будут игнорироваться.

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="type"
                            minOccurs="1"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="preLogon"
                                     />
                                    <xs:enumeration
                                        value="postLogon"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="maxDelay"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:enumeration
                                        value="0"
                                     />
                                    <xs:enumeration
                                        value="120"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="userBasedVirtualLan"
                            type="boolean"
                            minOccurs="0"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип    | Описание                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аусмоде**](onexschema-authmode-onex-element.md)                               |         | Указывает тип учетных данных, используемых для проверки подлинности.<br/>                                                                                                                                                        |
| [**ауспериод**](onexschema-authperiod-onex-element.md)                           |         | Указывает максимальный интервал времени (в секундах), в течение которого клиент ожидает ответа от средства проверки подлинности.<br/>                                                                                                  |
| [**качеусердата**](onexschema-cacheuserdata-onex-element.md)                     | Логическое | Указывает, кэшируются ли учетные данные пользователя для последующих подключений.<br/>                                                                                                                                     |
| [**еапконфиг**](onexschema-eapconfig-onex-element.md)                             |         | Задает конфигурацию EAPHost.<br/>                                                                                                                                                                              |
| [**хелдпериод**](onexschema-heldperiod-onex-element.md)                           |         | Указывает период времени в секундах, в течение которого клиент не будет повторно пытаться пройти проверку подлинности после неудачной попытки проверки подлинности.<br/>                                                                             |
| [**максаусфаилурес**](onexschema-maxauthfailures-onex-element.md)                 |         | Указывает максимальное количество ошибок проверки подлинности, разрешенных для набора учетных данных.<br/>                                                                                                                         |
| [**максделай**](onexschema-maxdelay-singlesignon-element.md)                       |         | Указывает максимальную задержку в секундах, по истечении которой попытка подключения единого входа завершится неудачей.<br/>                                                                                                                      |
| [**максстарт**](onexschema-maxstart-onex-element.md)                               |         | Указывает максимальное число отправленных сообщений EAPOL-Start.<br/>                                                                                                                                                        |
| [**singleSignOn**](onexschema-singlesignon-onex-element.md)                       |         | Задает сведения о конфигурации сети для единого входа.<br/>                                                                                                                                                       |
| [**стартпериод**](onexschema-startperiod-onex-element.md)                         |         | Указывает период времени (в секундах) ожидания перед отправкой EAPOL-Start.<br/>                                                                                                                                  |
| [**суппликантмоде**](onexschema-supplicantmode-onex-element.md)                   |         | Указывает метод передачи, используемый для пакетов EAPOL.<br/>                                                                                                                                                      |
| [**Тип**](onexschema-type-singlesignon-element.md)                               |         | Указывает, когда выполняется единый вход. Если задано значение `preLogon` , единый вход выполняется до входа пользователя в систему. Если задано значение `postLogon` , единый вход выполняется сразу после входа пользователя в систему.<br/> |
| [**усербаседвиртуаллан**](onexschema-userbasedvirtuallan-singlesignon-element.md) | Логическое | Указывает, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя.<br/>                                                                                                                   |



## <a name="remarks"></a>Комментарии

Сведения о просмотре списка дочерних элементов в древовидной структуре см. в разделе [элементы схемы OneX](onexschema-elements.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                 |



 

 




