---
description: Указывает, когда байтовый поток был изменен в последний раз.
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: Атрибут MF_BYTESTREAM_LAST_MODIFIED_TIME (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b476a78dba2bf757ed37b6029d67d5084804d1360dbc61e7c8861005b74a3bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113974"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a>\_ \_ \_ Атрибут времени последнего изменения MF BYTESTREAM \_

Указывает, когда байтовый поток был изменен в последний раз.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Remarks

Этот атрибут является необязательным. Значением атрибута является структура [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                                              |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты потока байтов](byte-stream-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
