---
title: Элемент username (CHAP)
description: Сведения об элементе username, определяющем пользователя, для которого выполняется проверка подлинности. См. пример синтаксиса и Просмотр дополнительных доступных ресурсов.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Элемент username, EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9ad861388ba8e15bb0df924610e6df1f833968794101cb1b04ccc47fb5ae541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086158"
---
# <a name="username-element-chap"></a>Элемент username (CHAP)

Элемент **username** определяет пользователя, для которого выполняется проверка подлинности.

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a>Remarks

Если элемент **username** отсутствует, имя пользователя получается из Winlogon. Этот элемент является необязательным.

## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





