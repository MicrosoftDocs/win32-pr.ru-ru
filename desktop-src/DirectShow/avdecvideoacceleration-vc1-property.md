---
description: Включает или отключает аппаратное ускорение для декодирования видео VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Свойство AVDecVideoAcceleration_VC1 (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1767206fab479dbcae1dec5e768b21d768440a66776b1f41610b75be4190d6c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663843"
---
# <a name="avdecvideoacceleration_vc1-property"></a>Авдеквидеоакцелератион \_ VC1, свойство

Включает или отключает аппаратное ускорение для декодирования видео VC-1.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авдеквидеоакцелератион \_ VC1**

## <a name="remarks"></a>Remarks

Если значение равно нулю, декодер не использует ускорение видео DirectX (ДКСВА) для декодирования видео VC-1. для DirectShow фильтров установите это свойство перед подключением выходного пин-кода декодера.

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

 

 




