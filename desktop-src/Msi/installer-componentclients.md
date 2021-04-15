---
description: Свойство Компонентклиентс только для чтения возвращает объект Стринглист, перечисляющий набор клиентов указанного компонента.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Свойство Installer. Компонентклиентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651967"
---
# <a name="installercomponentclients-property"></a>Свойство Installer. Компонентклиентс

Свойство **компонентклиентс** только для чтения возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор клиентов указанного компонента.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Значение свойства

Строковый идентификатор GUID, представляющий код компонента компонента. Коды компонентов указываются в столбце ComponentId [таблицы Component](component-table.md).

## <a name="remarks"></a>Комментарии

Для перечисления клиентов компонентов приложение может выполнить итерацию по объекту [**стринглист**](stringlist-object.md) , используя для каждой конструкции. Так как клиенты не упорядочиваются, все новые компоненты имеют произвольный индекс. Это означает, что функция может возвращать клиентов в любом порядке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиенумклиентс**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




