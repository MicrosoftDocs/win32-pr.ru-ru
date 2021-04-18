---
description: Свойство Шорткуттаржет объекта installer проверяет ярлык и возвращает его продукт, имя функции и компонент, если он доступен.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Свойство Installer. Шорткуттаржет
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652159"
---
# <a name="installershortcuttarget-property"></a>Свойство Installer. Шорткуттаржет

Свойство **шорткуттаржет** объекта [**Installer**](installer-object.md) проверяет ярлык и возвращает его продукт, имя функции и компонент, если он доступен.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Значение свойства

Полный путь и имя файла.

## <a name="remarks"></a>Комментарии

Шорткуттаржет возвращает [**объект Record**](record-object.md) , содержащий три поля:

-   Поле 1 — это идентификатор GUID для кода продукта ярлыка, если он доступен. Это поле может иметь значение null.
-   Поле 2 — это идентификатор компонента ярлыка, если он доступен. Это поле может иметь значение null.
-   Поле 3 — это идентификатор GUID для кода компонента, если он доступен. Это поле может иметь значение null.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсижетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**мсижеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




