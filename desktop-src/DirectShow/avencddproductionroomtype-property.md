---
description: Указывает тип комнаты для потока цифрового аудио Dolby. Это свойство применяется к кодировщикам цифрового аудио Dolby.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Свойство Авенкддпродуктионрумтипе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140451"
---
# <a name="avencddproductionroomtype-property"></a>Авенкддпродуктионрумтипе, свойство

Указывает тип комнаты для потока цифрового аудио Dolby. Это свойство применяется к кодировщикам цифрового аудио Dolby.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенкддпродуктионрумтипе**

## <a name="property-value"></a>Значение свойства

Значение этого свойства является членом перечисления [**еавенкддпродуктионрумтипе**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .

## <a name="remarks"></a>Комментарии

*Тип комнаты* относится к размеру комнаты, используемой в рабочей среде. Если это свойство задано, задайте для свойства [**авенкддпродуктионинфоексистс**](avencddproductioninfoexists-property.md) значение **true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Приложения Windows 2000 Professional \[ классические приложения \| UWP\]<br/>                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows 2000 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства кодека API](codec-api-properties.md)
</dt> <dt>

[**Интерфейс Икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

