---
description: Содержит список протоколов, используемых DCOM. Он содержит объект для каждого протокола.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Коллекция Дкомпротоколс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496164"
---
# <a name="dcomprotocols-collection"></a>Коллекция Дкомпротоколс

Содержит список протоколов, используемых DCOM. Он содержит объект для каждого протокола.

Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **дкомпротоколс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Корневой**](root.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Name](#name)
-   [Заказ](#order)
-   [протоколкоде](#protocolcode)

### <a name="name"></a>Имя



| Ввод | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя протокола. Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | ReadWrite                                                                                                                                                   |
| Тип           | Строка                                                                                                                                                      |
| По умолчанию        | "Новый протокол"                                                                                                                                              |
| Минимальная система | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>Заказ



| Ввод | Значение |
|----------------|-----------------------------------------|
| Описание    | Порядок, в котором следует использовать протокол. |
| Access         | ReadWrite                               |
| Тип           | Long (0-65000)                          |
| Значение по умолчанию        | 0                                       |
| Минимальная система | Windows 2000                            |



 

### <a name="protocolcode"></a>протоколкоде



| Ввод | Значение |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Код, указывающий последовательность протокола RPC. Поддерживаемые коды протоколов включают в себя: нкакн \_ IP \_ TCP, нкакн \_ http, нкакн \_ SPX. Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции. |
| Access         | Флагом writeonce                                                                                                                                                                                                                                                                   |
| Тип           | Строка                                                                                                                                                                                                                                                                      |
| По умолчанию        | ""                                                                                                                                                                                                                                                                          |
| Минимальная система | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
