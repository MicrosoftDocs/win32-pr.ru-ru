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
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652160"
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

## <a name="remarks"></a>Комментарии

Чтобы перечислить связанные продукты, приложение выполняет итерацию по [**стринглист**](stringlist-object.md) , используя для каждой конструкции. Так как связанные продукты не упорядочены, любой новый связанный продукт имеет произвольный индекс. Это означает, что функция может возвращать связанные продукты в любом порядке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиенумрелатедпродуктс**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




