---
description: Свойство Медиадискс перечисляет все диски носителя для данного экземпляра продукта. Это свойство вызывает Мсисаурцелистенуммедиадискс. Возвращает сведения о диске в виде массива объектов Record.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Свойство Product. Медиадискс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 00496739c9e51b5a735bf57788cdc47be0c41e177201ef445f58ea3748fb062f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042204"
---
# <a name="productmediadisks-property"></a>Свойство Product. Медиадискс

Свойство **медиадискс** перечисляет все диски носителя для данного экземпляра продукта. Это свойство вызывает [**мсисаурцелистенуммедиадискс**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa). Возвращает сведения о диске в виде массива объектов [**Record**](record-object.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

В каждой записи первое поле содержит идентификатор диска, второе поле содержит метку тома, а третье поле содержит приглашение диска, зарегистрированное для диска.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Продукта**](product-object.md)
</dt> <dt>

[**мсисаурцелистенуммедиадискс**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




