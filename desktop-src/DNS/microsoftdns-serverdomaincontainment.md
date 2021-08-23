---
title: Класс MicrosoftDNS_ServerDomainContainment
description: Каждый экземпляр \_ класса WMI ассоциации сервера микрософтднс может содержать несколько экземпляров \_ класса домена микрософтднс.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- DNS класса MicrosoftDNS_ServerDomainContainment
- DNS-MicrosoftDNS_ServerDomainContainment класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc747cae72ac4733ad9bec7288858731b6250312d43476a000d2f99a989267d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527254"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>\_Класс микрософтднс сервердомаинконтаинмент

Каждый экземпляр класса WMI [**ассоциации \_ сервера микрософтднс**](microsoftdns-server.md) может содержать несколько экземпляров класса [**\_ домена микрософтднс**](microsoftdns-domain.md) . Каждый экземпляр класса **\_ домена микрософтднс** принадлежит одному экземпляру класса **\_ сервера микрософтднс** и определен как ненадежный для этого сервера.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **микрософтднс \_ сервердомаинконтаинмент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **микрософтднс \_ сервердомаинконтаинмент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **микрософтднс \_ Server**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Квалификаторы: ключ, переопределение ("GroupComponent"), min (1), Max (1)

Описание: DNS-сервер.

Наследуется от **\_ компонента CIM**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **\_ домен микрософтднс**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Квалификаторы: ключ, переопределение ("PartComponent")

Описание: домен, зона, кэш или Русинтс, управляемые DNS-сервером.

Наследуется от **\_ компонента CIM**.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **микрософтднс \_ сервердомаинконтаинмент** является производным от класса **\_ компонента CIM** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Микрософтднс \_ домаиндомаинконтаинмент**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**Микрософтднс \_ домаинресаурцерекордконтаинмент**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





