---
title: Элемент Дисаблеусерпромптфорсервервалидатион (PEAP)
description: Сведения об элементе Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс). Указывает, должен ли пользователь запрашивать проверку сервера. | Элемент Дисаблеусерпромптфорсервервалидатион (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
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
ms.openlocfilehash: c032c4c0dcb67f60f64fe2b447fd1af7061df51ed19586f4ee15b43d6a6f870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561764"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>Элемент Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс) (PEAP)

Элемент **дисаблеусерпромптфорсервервалидатион (сервервалидатионпараметерс)** указывает, следует ли пользователю запрашивать проверку сервера.

Если **дисаблеусерпромптфорсервервалидатион** имеет значение true, то EAP-TLS выполняет проверку сервера без участия пользователя. Если проверка завершается неудачно, EAP-TLS не проверяет подлинность. Если **дисаблеусерпромптфорсервервалидатион** имеет значение false, пользователю предлагается ввести проверенный сертификат или имя сервера или корневой центр сертификации (CA).

Элемент **дисаблеусерпромптфорсервервалидатион** является необязательным.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

Элемент **дисаблеусерпромптфорсервервалидатион** определяется сложным типом [**сервервалидатионпараметерс**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**сервервалидатионпараметерс**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Возможные непосредственные родительские элементы в экземпляре схемы**
</dt> <dt>

[**Сервервалидатион (Еаптипе)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





