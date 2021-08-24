---
title: Класс MicrosoftDNS_ResourceRecord
description: Класс Микрософтднс \_ ресаурцерекорд представляет общие свойства записи ресурса DNS. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- DNS класса MicrosoftDNS_ResourceRecord
- DNS-MicrosoftDNS_ResourceRecord класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b54d23ae522291a2a38ad5d3f046fc444efdefd4d270519fbc3a2ee5739ba47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874804"
---
# <a name="microsoftdns_resourcerecord-class"></a>\_Класс микрософтднс ресаурцерекорд

Класс **микрософтднс \_ ресаурцерекорд** представляет общие свойства записи ресурса DNS.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a>Члены

Класс **микрософтднс \_ ресаурцерекорд** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **микрософтднс \_ ресаурцерекорд** содержит следующие методы.



| Метод                                   | Описание                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **креатеинстанцефромтекстрепресентатион** | Анализирует запись ресурса в строке Текстрепресентатион, а также с входными DNS-сервером и именами контейнеров, определяет и создает объект Ресаурцерекорд. Метод возвращает ссылку на новый объект в качестве выходного параметра. <br/> Квалификаторы: нет<br/> |
| **жетобжектбитекстрепресентатион**        | Извлекает существующий экземпляр \_ подкласса микрософтднс ресаурцерекорд, представленный строкой текстрепресентатион вместе с DNS-сервером и именем контейнера. <br/> Квалификаторы: нет<br/>                                                        |



 

### <a name="properties"></a>Свойства

Класс **микрософтднс \_ ресаурцерекорд** имеет следующие свойства.

<dl> <dt>

**ContainerName;**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего запись ресурса.

</dd> <dt>

**днссервернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает полное доменное имя (FQDN) или IP-адрес DNS-сервера, содержащего запись ресурса.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Представляет полное доменное имя домена, содержащего запись ресурса. Это свойство может содержать строки \\ .. Кэш \\ или \\ .. Русинтс \\ , если внутренний кэш или русинтс содержит запись ресурса соответственно.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя владельца для записи ресурса.

</dd> <dt>

**Рекордкласс = 1**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

* * Windows Server 2003: * *

Эта строка представляет класс записи ресурса. Допустимые значения:

1: в (Интернет)

2: CS (КСНЕТ)

3: CH (CHAOS)

4: HS (Хесиод)

</dd> <dt>

**рекорддата**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Данные записи ресурса.

</dd> <dt>

**текстрепресентатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое представление всей записи ресурса.

</dd> <dt>

**TimeStamp**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время последнего обновления записи ресурса, выраженное в прошедшем времени с 1 января 1601 г., среднее время по Гринвичу (GMT).

</dd> <dt>

**Срок жизни**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время в секундах, в течение которого запись ресурса может быть кэширована [*распознавателем*](r-gly.md)DNS.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Метод Креатеинстанцефромтекстрепресентатион \_ класса Ресаурцерекорд микрософтднс**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Метод Жетобжектбитекстрепресентатион \_ класса Ресаурцерекорд микрософтднс**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





