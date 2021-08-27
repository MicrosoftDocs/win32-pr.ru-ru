---
title: Класс MicrosoftDNS_Cache
description: '\_Класс кэша микрософтднс описывает существующий кэш на DNS-сервере.'
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- DNS класса MicrosoftDNS_Cache
- DNS-MicrosoftDNS_Cache класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03728a82f7668e38e43c92e3edacff1717333c6b073ee3491389723fb63b5f7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077074"
---
# <a name="microsoftdns_cache-class"></a>\_Класс кэша микрософтднс

Класс **\_ кэша микрософтднс** описывает существующий кэш на DNS-сервере. Этот класс упрощает визуализацию включения DNS-объектов, а не представляет реальный объект. Класс **\_ кэша микрософтднс** — это контейнер для записей ресурсов, кэшированных DNS-сервером. Не путайте это с файлом кэша, содержащим корневые ссылки.

Каждый экземпляр **\_ кэша микрософтднс** класса должен быть назначен ровно одному DNS-серверу. Он может быть связан с несколькими экземплярами классов [**микрософтднс \_ domain**](microsoftdns-domain.md) или [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) .

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Члены

Класс **\_ кэша микрософтднс** содержит следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **\_ кэша микрософтднс** содержит следующие методы.



| Метод                   | Описание                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | Очищает кэш DNS-сервера записей ресурсов. <br/> Квалификаторы: Реализовано<br/> |
| **жетдистингуишеднаме** | Извлекает различающееся имя зоны. <br/> Квалификаторы: Реализовано<br/>   |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Домен микрософтднс**](microsoftdns-domain.md)
</dt> <dt>

[**Метод ClearCache \_ класса кэша микрософтднс**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**Метод Жетдистингуишеднаме \_ класса кэша микрософтднс**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





