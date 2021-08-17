---
description: Свойство State возвращает состояние установки данного экземпляра обновления.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Свойство patch. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b28eee03cfc74537c8be7669124a4f70db40ca88196678889553978232c934c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942294"
---
# <a name="patchstate-property"></a>Свойство patch. State

Свойство **State** возвращает состояние установки данного экземпляра обновления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Это свойство возвращает одно из следующих значений.



| Состояние установки        | Значение                                                      |
|---------------------------|--------------------------------------------------------------|
| МСИПАТЧСТАТЕ \_ применено    | К этому экземпляру продукта применено исправление.                   |
| МСИПАТЧСТАТЕ \_ заменено | Исправление применено к этому экземпляру продукта, но заменено. |
| МСИПАТЧСТАТЕ \_ устарел  | Исправление установлено в этом экземпляре продукта, но устарело.      |



 

Этот метод может возвращать ошибку \_ неизвестное \_ исправление, если объект [**Patch**](patch-object.md) инициализируется пустой строкой для *ProductCode*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Обновление**](patch-object.md)
</dt> <dt>

[**мсижетпатчинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




