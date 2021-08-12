---
title: Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс)
description: Сведения об элементе Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс). Указывает, должен ли пользователь запрашивать проверку сервера. | Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
keywords:
- Элемент Дисаблеусерпромптфорсервервалидатион EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37f412f9c6200e7d2a54d624d0a77b4df5316ea7edd0ab75b69f92c753abbcff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273722"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a>Элемент Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс) (TLS)

Элемент **дисаблеусерпромптфорсервервалидатион (сервервалидатионпараметерс)** указывает, следует ли пользователю запрашивать проверку сервера.

Если **дисаблеусерпромптфорсервервалидатион** имеет значение true, то EAP-TLS выполняет проверку сервера без участия пользователя. Если проверка завершается неудачно, EAP-TLS не проверяет подлинность. Если **дисаблеусерпромптфорсервервалидатион** имеет значение false, пользователю предлагается ввести проверенный сертификат или имя сервера или корневой центр сертификации (CA).

Элемент **дисаблеусерпромптфорсервервалидатион** является необязательным.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

Элемент **дисаблеусерпромптфорсервервалидатион** определяется сложным типом [**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Возможные непосредственные родительские элементы в экземпляре схемы**
</dt> <dt>

[**Сервервалидатион (Еаптипе)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





