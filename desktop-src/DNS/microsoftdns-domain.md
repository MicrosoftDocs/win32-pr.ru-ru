---
title: Класс MicrosoftDNS_Domain
description: '\_Доменный класс микрософтднс представляет домен в ИЕРАРХИИ DNS.'
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- DNS класса MicrosoftDNS_Domain
- DNS-MicrosoftDNS_Domain класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a30b171777e6c8a99ddadcfb39c8cdfdd90b09a43ae255c9bbcc026db09bdb1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163323"
---
# <a name="microsoftdns_domain-class"></a>\_Класс домена микрософтднс

**\_ Доменный класс Микрософтднс** представляет домен в иерархии DNS.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a>Члены

Класс **\_ домена микрософтднс** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ домена микрософтднс** содержит следующие методы.



| Метод                   | Описание                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **жетдистингуишеднаме** | Получает различающееся имя DS для зоны. <br/> Квалификаторы: Реализовано<br/> |



 

### <a name="properties"></a>Свойства

Класс **\_ домена микрософтднс** имеет следующие свойства.

<dl> <dt>

**ContainerName;**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя контейнера домена, который может быть зоной, кэшем или Русинтс.

В случаях, когда контейнер является зоной (экземпляром класса [**микрософтднс \_ Zone**](microsoftdns-zone.md) ), это свойство содержит полное доменное имя зоны.

Если контейнер является корневой зоной, \\ следует использовать строку. \\

В случаях, когда контейнер является кэшем DNS записей ресурсов (экземпляр класса [**\_ кэша микрософтднс**](microsoftdns-cache.md) ), для этого свойства задается строка \\ .. Кэш \\ .

Если контейнером является Русинтс (экземпляр класса [**микрософтднс \_ русинтс**](microsoftdns-roothints.md) ), этому свойству должно быть присвоено значение \\ . Русинтс \\ .

</dd> <dt>

**днссервернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

FQDN или IP-адрес DNS-сервера, содержащего домен.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Полное доменное имя домена.

Для экземпляров кэша DNS или Русинтс строки \\ .. Кэш \\ и \\ .. Русинтс \\ следует использовать соответственно.

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

[**Метод Жетдистингуишеднаме \_ класса домена микрософтднс**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





