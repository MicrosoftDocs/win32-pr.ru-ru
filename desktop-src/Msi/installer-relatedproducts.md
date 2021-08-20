---
description: Свойство Релатедпродуктс только для чтения возвращает объект Стринглист, перечисляющий набор всех продуктов, установленных или объявленных для текущего пользователя и компьютера с указанным свойством UpgradeCode в своей таблице свойств.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Свойство Installer. Релатедпродуктс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 15e84a063b8f094dbeee02f3000bdd1c69356f5fa664f6e6f6aff87d19d07dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946142"
---
# <a name="installerrelatedproducts-property"></a>Свойство Installer. Релатедпродуктс

Свойство **релатедпродуктс** только для чтения возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор всех продуктов, установленных или объявленных для текущего пользователя и компьютера с указанным свойством [**UpgradeCode**](upgradecode.md) в своей [таблице свойств](property-table.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Значение свойства

Код обновления связанных продуктов, перечисленный установщиком.

## <a name="remarks"></a>Remarks

Чтобы перечислить связанные продукты, приложение выполняет итерацию по [**стринглист**](stringlist-object.md) , используя для каждой конструкции. Так как связанные продукты не упорядочены, любой новый связанный продукт имеет произвольный индекс. Это означает, что функция может возвращать связанные продукты в любом порядке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мсиенумрелатедпродуктс**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




