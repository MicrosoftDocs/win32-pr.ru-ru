---
title: Элемент EAP (свойства соединения)
description: Сведения об элементе EAP. Этот элемент захватывает выбранный тип метода и конфигурацию конкретного метода. | Элемент EAP (свойства соединения)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
keywords:
- Элемент EAP EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693972"
---
# <a name="eap-element-connection-properties"></a>Элемент EAP (свойства соединения)

Элемент **EAP** захватывает выбранный тип метода и конфигурацию конкретного метода.

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Комментарии

Метод может определять составные элементы внутри элемента **EAP** . Метод также выполняет проверку схемы для элементов в **EAP**.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





