---
description: Задает идентификатор ключа для образца.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Атрибут MFSampleExtension_Content_KeyID (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38498665dddaed0cd38082246f61f0f86c9b1b7a1e8cec7d19d476c860fe8d6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848174"
---
# <a name="mfsampleextension_content_keyid-attribute"></a>\_ \_ Атрибут KeyID Content мфсампликстенсион

Задает идентификатор ключа для образца.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="examples"></a>Примеры

В следующем примере показано, как задать идентификатор ключа для образца.


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                     |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[\_Субсамплемаппингсплит шифрования \_ мфсампликстенсион](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




