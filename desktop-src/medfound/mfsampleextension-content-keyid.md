---
description: Задает идентификатор ключа для образца.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Атрибут MFSampleExtension_Content_KeyID (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662779"
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
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[\_Субсамплемаппингсплит шифрования \_ мфсампликстенсион](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




