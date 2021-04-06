---
description: Содержит GUID категории для Media Foundation преобразования (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: Свойство MFPKEY_CATEGORY (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910195"
---
# <a name="mfpkey_category-property"></a>МФПКЭЙ, \_ свойство категории

Содержит GUID категории для Media Foundation преобразования (MFT).



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**GUID** (**CLSID** \* )

VT \_ CLSID

**пууид**



## <a name="remarks"></a>Комментарии

Значением этого свойства является идентификатор GUID, определяющий категорию MFT. Список категорий см. в разделе [**MFT \_ Category**](mft-category.md).

Это свойство является необязательным и является информационным. Таблица MFT может использовать это свойство для сообщения категории, под которой он зарегистрирован. Чтобы получить это свойство, запросите MFT для интерфейса **ипропертисторе** .

Чтобы перечислить категорию MFT, вызовите функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) . Нет прямой связи между функцией **мфтенум** и этим свойством.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




