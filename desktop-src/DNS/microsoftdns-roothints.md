---
title: Класс MicrosoftDNS_RootHints
description: Класс Микрософтднс \_ русинтс описывает русинтс, хранимые в файле кэша на DNS-сервере. Этот класс упрощает визуализацию включения DNS-объектов, а не представляет реальный объект.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- DNS класса MicrosoftDNS_RootHints
- DNS-MicrosoftDNS_RootHints класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050da9acb1d3865fb490035b6de57fcc1279a45b6f9d78c57df305993d590c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913004"
---
# <a name="microsoftdns_roothints-class"></a>\_Класс микрософтднс русинтс

Класс **микрософтднс \_ Русинтс** описывает русинтс, хранимые в файле кэша на DNS-сервере. Этот класс упрощает визуализацию включения DNS-объектов, а не представляет реальный объект.

**Микрософтднс \_ Русинтс** — это контейнер для записей ресурсов, хранимых DNS-сервером в файле кэша. Каждый экземпляр класса **микрософтднс \_ русинтс** должен быть назначен ровно одному DNS-серверу. Он может быть связан с несколькими экземплярами класса [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) .

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Члены

Класс **микрософтднс \_ русинтс** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **микрософтднс \_ русинтс** содержит следующие методы.



| Метод                        | Описание                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **жетдистингуишеднаме**      | Извлекает различающееся имя зоны. <br/> Квалификаторы: Реализовано<br/>   |
| **вритебаккрусинтдатафиле** | Записывает Русинтс обратно в файл кэша DNS. <br/> Квалификаторы: Реализовано<br/> |



 

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

[**Метод Вритебаккрусинтдатафиле \_ класса Русинтс микрософтднс**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Метод Жетдистингуишеднаме \_ класса Русинтс микрософтднс**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





