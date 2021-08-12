---
title: Элемент Identity
description: Сведения об элементе удостоверения EAPHost. Этот элемент захватывает удостоверение, используемое для проверки подлинности.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Элемент Identity EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad88e84583be2b392ce8a4dfdaec7495f1c063fa13d4327004bfbecbc1f925ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275471"
---
# <a name="identity-element"></a>Элемент Identity

Элемент **Identity** захватывает удостоверение, используемое для проверки подлинности.

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a>Remarks

Элемент **Identity** является абстрактным; Каждый метод должен определять и использовать производный элемент в документах экземпляра.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





