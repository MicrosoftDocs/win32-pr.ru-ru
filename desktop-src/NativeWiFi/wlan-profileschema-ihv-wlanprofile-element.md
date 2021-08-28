---
description: Содержит различные параметры для независимых поставщиков оборудования.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Элемент IHV (Вланпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1cfcd9ee463ef91d04d0bebbeac800d48da32fdd777edc2a08ccf0051410160d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799924"
---
# <a name="ihv-wlanprofile-element"></a>Элемент IHV (Вланпрофиле)

Элемент IHV (Вланпрофиле) содержит различные параметры для независимых поставщиков оборудования. Если профиль включает параметры безопасности IHV, они переопределяют любую систему безопасности, определенную корпорацией Майкрософт.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
                type="boolean"
                minOccurs="0"
             />
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

Элемент определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                             | Тип                                                              | Описание                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**установлен**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Содержит параметры подключения, связанные с IHV.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**КОДОМ**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Содержит 3-байтовый hexBinary, определяющий IHV.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**ауихеадер**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Идентифицирует независимый поставщик оборудования.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**бюллетеня**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Содержит параметры безопасности, зависящие от IHV. Параметры безопасности Microsoft и параметры безопасности IHV являются взаимоисключающими. Если заданы оба параметра безопасности, то весь профиль считается недопустимым.<br/>                                                                                                                                                                                            |
| [**Тип**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Содержит 1-байтовый hexBinary, используемый для различения сетевых карт одним и тем же IHV.<br/>                                                                                                                                                                                                                                                                                                        |
| [**усемсонекс**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | Указывает источник параметров безопасности 802.1 X, используемых компонентом безопасности независимого поставщика оборудования. Если [**усемсонекс**](wlan-profileschema-usemsonex-ihv-element.md) имеет значение true, компоненты безопасности IHV используют определенные корпорацией Майкрософт параметры 802.1 x. Если **усемсонекс** имеет значение false, компоненты безопасности IHV используют предоставленные поставщиком параметры 802.1 x. По умолчанию **усемсонекс** имеет значение false. Этот элемент является необязательным.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
