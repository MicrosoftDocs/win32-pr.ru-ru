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
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071869"
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

### <a name="properties"></a>Свойства

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Микрософтднс \_ домаинресаурцерекордконтаинмент**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Микрософтднс \_ сервердомаинконтаинмент**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





