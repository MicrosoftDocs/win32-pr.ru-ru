---
description: Клиентский объект представляет связь между компонентом и клиентским продуктом.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Клиентский объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668564"
---
# <a name="client-object"></a>Клиентский объект

Клиентский объект представляет связь между компонентом и клиентским продуктом.

**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается. Этот объект доступен, начиная с установщик Windows 5,0.

## <a name="members"></a>Элементы

**Клиентский** объект имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

**Клиентский** объект имеет эти свойства.



| Свойство                                                 | Описание                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**компоненткоде**](client-componentcode.md)<br/> | Код компонента рассматриваемого компонента.<br/> |
| [**Локального**](client-context.md)<br/>             | Контекст продукта.<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | Клиентское программное произведение рассматриваемого компонента.<br/> |
| [**UserSID**](client-usersid.md)<br/>             | Идентификатор безопасности пользователя для компонента.<br/>                  |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 или более поздней версии.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ иклиент определен как 000C1098-0000-0000-C000-000000000046<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование интерфейса автоматизации](using-the-automation-interface.md)
</dt> <dt>

[Примеры сценариев установщик Windows](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




