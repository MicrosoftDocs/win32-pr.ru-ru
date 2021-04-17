---
description: Свойство State возвращает состояние установки данного экземпляра продукта.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Свойство Product. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652081"
---
# <a name="productstate-property"></a>Свойство Product. State

Свойство **State** возвращает состояние установки данного экземпляра продукта.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Product.State
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Это свойство возвращает одно из следующих значений.



| Состояние установки       | Значение                                |
|--------------------------|----------------------------------------|
| INSTALLSTATE \_ по умолчанию    | Экземпляр продукта, установленный локально. |
| INSTALLSTATE \_ объявлено | Объявленный экземпляр продукта.        |
| INSTALLSTATE \_ неизвестный    | Экземпляр продукта неизвестен.           |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Продукта**](product-object.md)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




