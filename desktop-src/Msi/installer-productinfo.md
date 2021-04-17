---
description: Свойство ProductInfo является свойством только для чтения, которое возвращает значение указанного атрибута для установленного или опубликованного продукта.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Свойство Installer. ProductInfo (Оемупжекс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652226"
---
# <a name="installerproductinfo-property"></a>Свойство Installer. ProductInfo

Свойство **ProductInfo** является свойством только для чтения, которое возвращает значение указанного атрибута для установленного или опубликованного продукта.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Свойство **ProductInfo** ("локалпаккаже") не обязательно возвращает путь к кэшированному пакету. Установка режима обслуживания не должна вызываться из Локалпаккаже. Кэшированный пакет предназначен только для внутреннего использования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.<br/> |
| Header<br/>  | <dl> <dt>Оемупжекс. h</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсижетпродуктинфо**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**мсижетусеринфо**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




