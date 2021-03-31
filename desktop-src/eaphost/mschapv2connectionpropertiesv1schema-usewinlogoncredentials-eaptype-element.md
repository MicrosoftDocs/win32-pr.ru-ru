---
title: Усевинлогонкредентиалс (Еаптипе), элемент
description: Сведения об элементе Усевинлогонкредентиалс (Еаптипе). Этот элемент управляет использованием учетных данных винлогин.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Элемент Усевинлогонкредентиалс EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793927"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Усевинлогонкредентиалс (Еаптипе), элемент

Элемент **усевинлогонкредентиалс (еаптипе)** управляет использованием учетных данных винлогин.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

Элемент **усевинлогонкредентиалс** определяется элементом [**еаптипе**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Комментарии

Если значение — TRUE, EAP MS-CHAPv2 получает учетные данные из Winlogon. Если значение равно FALSE, то EAP MS-CHAPv2 получает учетные данные от пользователя. Элемент **усевинлогонкредентиалс (еаптипе)** является необязательным.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|-------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еаптипе**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**еаптипе**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





