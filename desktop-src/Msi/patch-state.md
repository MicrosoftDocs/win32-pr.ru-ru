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
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652148"
---
# <a name="patchstate-property"></a>Свойство patch. State

Свойство **State** возвращает состояние установки данного экземпляра обновления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

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
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Защиты**](patch-object.md)
</dt> <dt>

[**мсижетпатчинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




