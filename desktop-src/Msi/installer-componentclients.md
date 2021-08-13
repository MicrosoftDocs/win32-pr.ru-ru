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
ms.openlocfilehash: c94a30247bbfc39675308308457c369785bd9a67413a5b0b62af143e17e2112b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632716"
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

## <a name="remarks"></a>Remarks

Для перечисления клиентов компонентов приложение может выполнить итерацию по объекту [**стринглист**](stringlist-object.md) , используя для каждой конструкции. Так как клиенты не упорядочиваются, все новые компоненты имеют произвольный индекс. Это означает, что функция может возвращать клиентов в любом порядке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиенумклиентс**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




