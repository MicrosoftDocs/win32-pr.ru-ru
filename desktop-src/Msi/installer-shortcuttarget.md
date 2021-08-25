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
ms.openlocfilehash: b54e334314c0bfd0fb721b175d0a14894d8a509ea02ff36e324903bb1fdbffaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894004"
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

## <a name="remarks"></a>Remarks

Шорткуттаржет возвращает [**объект Record**](record-object.md) , содержащий три поля:

-   Поле 1 — это идентификатор GUID для кода продукта ярлыка, если он доступен. Это поле может иметь значение null.
-   Поле 2 — это идентификатор компонента ярлыка, если он доступен. Это поле может иметь значение null.
-   Поле 3 — это идентификатор GUID для кода компонента, если он доступен. Это поле может иметь значение null.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мсижетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**мсижеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




