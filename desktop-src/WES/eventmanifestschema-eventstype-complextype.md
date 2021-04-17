---
title: Сложный тип Евентстипе
description: Содержит список поставщиков, определенных в манифесте. | Сложный тип Евентстипе
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- Журнал событий сложных типов Евентстипе
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694006"
---
# <a name="eventstype-complex-type"></a>Сложный тип Евентстипе

Содержит список поставщиков, определенных в манифесте.

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы

| Элемент | Тип | Описание |
|---------|------|-------------|
| message |      | Определяет строку сообщения. |
| мессажетабле | | Определяет список строк сообщений. Не следует использовать таблицу сообщений, за исключением следующих случаев, когда необходимо определить таблицу сообщений для явного назначения номеров ресурсов строкам сообщений. <ul><li>Выполняется миграция из текстового файла сообщения (. MC) в манифест, но все еще записываются события в приложения и системные каналы, чтобы устаревшие потребители продолжали потреблять события. Чтобы сделать эту работу, идентификаторы ресурсов для строк сообщений, определенных в манифесте, должны совпадать с идентификаторами событий. Однако компилятор сообщений автоматически назначает идентификаторы ресурсов строкам сообщений. Чтобы переопределить компилятор, используйте таблицу сообщений и присвойте атрибуту Value идентификатор события и атрибут Message для ссылки на строку в таблице строк в разделе локализации манифеста.</li><li>Если требуется определить более 16 поставщиков, необходимо включить таблицу сообщений, которую семнадцатого и поставщики должны использовать для назначения значений ресурсов для строк сообщений, которые они определяют. Если поставщик ссылается на строки сообщений, определенные поставщиками от 1 до 16, эти строки сообщений не включаются в таблицу сообщений.</li></ul>|
| [**поставщики**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Список поставщиков, которые необходимо определить. |

## <a name="attributes"></a>Атрибуты

| Имя    | Тип                                                             | Описание                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**стртаблереф**](eventmanifestschema-strtableref-simpletype.md) | Ссылка на локализованную строку в таблице строк.                               |
| mid     | xs:string                                                        | Не используется.                                                                              |
| символ  | [**ксимболтипе**](eventmanifestschema-csymboltype-simpletype.md) | Символьное имя, создаваемое компилятором сообщений для этой строки сообщения.|
| значение   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Число, используемое в качестве идентификатора сообщения для данного сообщения.                          |


## <a name="remarks"></a>Комментарии

Практический лимит количества поставщиков, которые можно определить в манифесте, составляет 16 поставщиков. При указании более 16 поставщиков необходимо использовать таблицу сообщений для явного присвоения номеров ресурсов строкам сообщений, на которые ссылается поставщик. Дополнительные сведения см. в элементе Message выше.

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------------|-------------------------------------------|
| Минимальная версия клиента | Только для \[ классических приложений Windows Vista\]       |
| Минимальная версия сервера | \[Только для настольных приложений Windows Server 2008\] |
