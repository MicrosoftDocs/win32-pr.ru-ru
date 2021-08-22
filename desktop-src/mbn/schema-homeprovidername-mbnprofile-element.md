---
description: Определяет имя поставщика услуг домашнего доступа для указанной SIM-карты или устройства.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Хомепровидернаме (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 1868be18dc7acf9d5146f987658feb006714fbcc3db35883007afd01c308609e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035832"
---
# <a name="homeprovidername-mbnprofile-element"></a>Хомепровидернаме (Мбнпрофиле), элемент

Элемент **хомепровидернаме (мбнпрофиле)** определяет имя поставщика услуг домашнего доступа для указанной SIM-карты или устройства.

Этот элемент является необязательным и задается службой мобильного широкополосного подключения для внутреннего использования. Приложение не должно задавать это поле при создании или обновлении профиля.

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

Элемент **хомепровидернаме** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




