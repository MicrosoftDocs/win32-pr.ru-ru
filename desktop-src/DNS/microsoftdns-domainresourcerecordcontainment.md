---
title: Класс MicrosoftDNS_DomainResourceRecordContainment
description: Класс Микрософтднс \_ домаинресаурцерекордконтаинмент используется для включения записи RR; каждый экземпляр \_ домена микрософтднс может содержать несколько экземпляров \_ класса микрософтднс ресаурцерекорд.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- DNS класса MicrosoftDNS_DomainResourceRecordContainment
- DNS-MicrosoftDNS_DomainResourceRecordContainment класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 498d9b953895ebece94dc77edb587045d1cfdd45c29f04c202756bd1080dc9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795614"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>\_Класс микрософтднс домаинресаурцерекордконтаинмент

Класс **микрософтднс \_ домаинресаурцерекордконтаинмент** используется для включения записи RR; каждый экземпляр [**\_ домена микрософтднс**](microsoftdns-domain.md) может содержать несколько экземпляров класса [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) . Каждый экземпляр класса **микрософтднс \_ ресаурцерекорд** принадлежит одному экземпляру класса **\_ домена микрософтднс** и определен как слабый для этого экземпляра.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **микрософтднс \_ домаинресаурцерекордконтаинмент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **микрософтднс \_ домаинресаурцерекордконтаинмент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **\_ домен микрософтднс**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Квалификаторы: ключ, переопределение ("GroupComponent")

Описание: зона, кэш, Русинтс или домен, непосредственно содержащий запись ресурса.

Наследуется от \_ компонента CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **микрософтднс \_ ресаурцерекорд**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Квалификаторы: ключ, переопределение ("PartComponent")

Описание: запись ресурса, содержащаяся в домене, зоне, кэше или Русинтс.

Наследуется от \_ компонента CIM.

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

[**Микрософтднс \_ сервердомаинконтаинмент**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**Микрософтднс \_ домаиндомаинконтаинмент**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





