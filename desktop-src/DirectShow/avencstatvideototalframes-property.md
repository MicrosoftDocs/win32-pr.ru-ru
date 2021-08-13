---
description: Возвращает число кадров видео, полученных кодировщиком.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Свойство Авенкстатвидеототалфрамес (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 461708e9006db183992cf550bf7f98eeaeacbfe16c100675ab4992b54f0768d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663445"
---
# <a name="avencstatvideototalframes-property"></a>Авенкстатвидеототалфрамес, свойство

Возвращает число кадров видео, полученных кодировщиком.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенкстатвидеототалфрамес**

## <a name="remarks"></a>Remarks

Это свойство доступно после завершения кодирования.

Значением этого свойства является общее число кадров, отправленных кодировщику, включая пропущенные кадры. Чтобы получить количество закодированных кадров, прочитайте свойство [**авенкстатвидеокодедфрамес**](avencstatvideocodedframes-property.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional приложения \[ UWP для классических приложений \|\]<br/>                     |
| Минимальная версия сервера<br/> | \[приложения UWP для классических приложений Windows 2000 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства кодека API](codec-api-properties.md)
</dt> <dt>

[**Интерфейс Икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




