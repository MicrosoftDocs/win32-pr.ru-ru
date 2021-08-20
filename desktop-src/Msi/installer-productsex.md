---
description: Возвращает объект Рекордлист, перечисляющий список продуктов.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Свойство Installer. Продуктсекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9320ef38fefd32c60b7022923add5ca55d609d82ff01b8654104bb35b1dbf6be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074934"
---
# <a name="installerproductsex-property"></a>Свойство Installer. Продуктсекс

Свойство **продуктсекс** возвращает объект [**рекордлист**](recordlist-object.md) , перечисляющий список продуктов. Это свойство вызывает [**мсиенумпродуктсекс**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003 или Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Установщик**](installer-object.md)
</dt> <dt>

[**мсиенумпродуктсекс**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Продукт**](product-object.md)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




