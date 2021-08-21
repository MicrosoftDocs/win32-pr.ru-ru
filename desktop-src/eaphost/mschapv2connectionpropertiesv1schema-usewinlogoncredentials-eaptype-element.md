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
ms.openlocfilehash: 2a407c505139562a155e5aa9d7ed57fed5d15077cf5d035ea8bb7bbe0e177363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086195"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Усевинлогонкредентиалс (Еаптипе), элемент

Элемент **усевинлогонкредентиалс (еаптипе)** управляет использованием учетных данных винлогин.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

Элемент **усевинлогонкредентиалс** определяется элементом [**еаптипе**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarks

Если значение — TRUE, EAP MS-CHAPv2 получает учетные данные из Winlogon. Если значение равно FALSE, то EAP MS-CHAPv2 получает учетные данные от пользователя. Элемент **усевинлогонкредентиалс (еаптипе)** является необязательным.

## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|-------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

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

 

 





