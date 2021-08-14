---
description: Задает сведения о конфигурации сети единого входа (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Элемент singleSignOn (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5d0e002133366527624a0954df9054272cc08d894ba8dc3121b8a86b807caab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798035"
---
# <a name="singlesignon-onex-element"></a>Элемент singleSignOn (OneX)

Элемент singleSignOn (OneX) задает сведения о конфигурации сети единого входа (SSO).

Этот элемент является необязательным. Не используйте элемент singleSignOn в профиле, если он не требуется в сети.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.

``` syntax
<xs:element name="singleSignOn">
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
```

Элемент **singleSignOn** определяется элементом [**OneX**](onexschema-onex-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип    | Описание                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Указывает максимальную задержку в секундах, по истечении которой попытка подключения единого входа завершится неудачей.<br/>                                                                                                                      |
| [**Тип**](onexschema-type-singlesignon-element.md)                               |         | Указывает, когда выполняется единый вход. Если задано значение `preLogon` , единый вход выполняется до входа пользователя в систему. Если задано значение `postLogon` , единый вход выполняется сразу после входа пользователя в систему.<br/> |
| [**усербаседвиртуаллан**](onexschema-userbasedvirtuallan-singlesignon-element.md) | Логическое | Указывает, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя.<br/>                                                                                                                   |



## <a name="remarks"></a>Remarks

Этот параметр можно задать в командной строке с помощью команды **netsh wlan set профилепараметер** . Дополнительные сведения см. в разделе [команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> </dl>

 

 
