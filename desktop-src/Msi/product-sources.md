---
description: Свойство Sources перечисляет все источники для экземпляра продукта.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Свойство Product. sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675976"
---
# <a name="productsources-property"></a>Свойство Product. sources

Свойство **Sources** перечисляет все источники для экземпляра продукта. Это свойство вызывает [**мсисаурцелистенумсаурцес**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) и возвращает массив строк и принимает тип источника в качестве аргумента. Исходный тип может быть МСИСАУРЦЕТИПЕ \_ сетевым или мсисаурцетипе \_ URL-адресом.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a>Значение свойства

Тип источника для перечисления. Значение может быть *мсиинсталлсаурцетипенетворк* (1) или *мсиинсталлсаурцетипеурл* (2).

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

[**мсисаурцелистенумсаурцес**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




