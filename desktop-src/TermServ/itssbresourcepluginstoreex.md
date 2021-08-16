---
title: Интерфейс Итссбресаурцеплугинсторикс
description: Предоставляет методы, позволяющие подключаемым модулям ресурсов хранить объекты, такие как сеансы и целевые объекты.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Итссбресаурцеплугинсторикс
- Службы удаленных рабочих столов интерфейса Итссбресаурцеплугинсторикс, описание
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23c3ba6689f52d592d9c9799b6c7bec0acd58e1afcbc8e7a18e0cb9dbe6db98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351297"
---
# <a name="itssbresourcepluginstoreex-interface"></a>Интерфейс Итссбресаурцеплугинсторикс

Предоставляет методы, позволяющие подключаемым модулям ресурсов хранить объекты, такие как сеансы и целевые объекты. Эти методы добавляют, удаляют и запрашивают эти объекты.

этот интерфейс доступен только в Windows Server 2012 R2 с установленным [KB3091411](https://support.microsoft.com/kb/3091411) . Методы [**аккуиретаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) и [**релеасетаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) интерфейса [**итссбресаурцеплугинсторе**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) доступны начиная с Windows Server 2016.

## <a name="members"></a>Элементы

Интерфейс **итссбресаурцеплугинсторикс** наследует от [**итссбресаурцеплугинсторе**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore). **Итссбресаурцеплугинсторикс** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **итссбресаурцеплугинсторикс** содержит следующие методы.



| Метод                                                                                                            | Описание                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**аккуиретаржетлокк**](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | Блокирует целевой объект.<br/>                                                                                      |
| [**адденвиронменттосторе**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | Добавляет среду в хранилище подключаемых модулей ресурсов.<br/>                                                   |
| [**аддсессионтосторе**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | Добавляет новый сеанс в хранилище подключаемых модулей ресурсов.<br/>                                                    |
| [**аддтаржеттосторе**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | Добавляет целевой объект в хранилище подключаемых модулей ресурсов.<br/>                                                         |
| [**делететаржет**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | Удаляет целевой объект.<br/>                                                                                    |
| [**енумератинвиронментс**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | Возвращает массив, содержащий среды, которые находятся в хранилище подключаемых модулей ресурсов.<br/>               |
| [**енумератефармс**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | Перечисляет все фермы, добавленные в хранилище подключаемых модулей ресурсов.<br/>                         |
| [**енумератесессионс**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | Перечисляет заданный набор сеансов.<br/>                                                              |
| [**енумератетаржетс**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | Возвращает массив, содержащий указанные целевые объекты, которые имеются в хранилище подключаемых модулей ресурсов.<br/> |
| [**жетфармпроперти**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | Извлекает свойство фермы.<br/>                                                                      |
| [**куеренвиронмент**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | Возвращает указанный объект среды.<br/>                                                            |
| [**куерисессионбисессионид**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | Возвращает объект Session с указанным ИДЕНТИФИКАТОРом сеанса.<br/>                                        |
| [**куеритаржет**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | Возвращает целевой объект с указанным именем целевого объекта и именем фермы.<br/>                                 |
| [**релеасетаржетлокк**](itssbresourcepluginstoreex-releasetargetlock.md)                                         | Снимает блокировку на целевой объект.<br/>                                                                         |
| [**ремовинвиронментфромсторе**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | Удаляет указанную среду из хранилища подключаемых модулей ресурсов.<br/>                                   |
| [**савинвиронмент**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | Сохраняет окружение.<br/>                                                                                |
| [**савесессион**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | Сохраняет сеанс.<br/>                                                                                     |
| [**саветаржет**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | Сохраняет целевой объект.<br/>                                                                                      |
| [**сетенвиронментпроперти**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | Задает свойство среды.<br/>                                                                   |
| [**сетенвиронментпропертивисверсиончекк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | Задает свойство среды.<br/>                                                                   |
| [**сетсессионстате**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | Установка состояния сеанса.<br/>                                                                         |
| [**сеттаржетпроперти**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | Задает свойство для целевого объекта.<br/>                                                                         |
| [**сеттаржетпропертивисверсиончекк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | Задает свойство для целевого объекта.<br/>                                                                         |
| [**сеттаржетстате**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | Задает состояние целевого объекта.<br/>                                                                          |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                             |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                             |
| IID<br/>                      | IID \_ итссбресаурцеплугинсторикс определен как 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итссбресаурцеплугинсторе**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[Интерфейсы виртуализации удаленный рабочий стол](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





