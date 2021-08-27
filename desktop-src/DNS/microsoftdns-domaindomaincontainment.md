---
title: Класс MicrosoftDNS_DomainDomainContainment
description: Класс Микрософтднс \_ домаиндомаинконтаинмент используется для включения домена. Домены DNS могут содержать другие домены DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- DNS класса MicrosoftDNS_DomainDomainContainment
- DNS-MicrosoftDNS_DomainDomainContainment класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f96d03f007af463fb4c4f672eb0d1374867636f4a4224469589563b9c5882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084754"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>\_Класс микрософтднс домаиндомаинконтаинмент

Класс **микрософтднс \_ домаиндомаинконтаинмент** используется для включения домена. Домены DNS могут содержать другие домены DNS. Каждый экземпляр класса [**\_ домена микрософтднс**](microsoftdns-domain.md) может содержать несколько других экземпляров **\_ домена микрософтднс**. Экземпляр объекта **\_ домена микрософтднс** напрямую содержится в не более чем в одном **\_ домене микрософтднс** более высокого уровня.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **микрософтднс \_ домаиндомаинконтаинмент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **микрософтднс \_ домаиндомаинконтаинмент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **\_ домен микрософтднс**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Квалификаторы: Key, Max (1), reoverride ("GroupComponent")

Описание: домен более высокого уровня, зона, кэш или Русинтс.

Наследуется от \_ компонента CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **\_ домен микрософтднс**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Квалификаторы: ключ, переопределение ("PartComponent")

Описание: домен, содержащийся в домене более высокого уровня, в зоне, кэше или Русинтс.

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

[**Микрософтднс \_ домаинресаурцерекордконтаинмент**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Микрософтднс \_ сервердомаинконтаинмент**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





