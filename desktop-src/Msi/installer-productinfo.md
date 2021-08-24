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
ms.openlocfilehash: 5d04ad49fd8c1cf017131b5ded6be088e6436731b6bd97dd437060d09988d3aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745294"
---
# <a name="installerproductinfo-property"></a>Свойство Installer. ProductInfo

Свойство **ProductInfo** является свойством только для чтения, которое возвращает значение указанного атрибута для установленного или опубликованного продукта.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Свойство **ProductInfo** ("локалпаккаже") не обязательно возвращает путь к кэшированному пакету. Установка режима обслуживания не должна вызываться из Локалпаккаже. Кэшированный пакет предназначен только для внутреннего использования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003 или Windows XP.<br/> |
| Заголовок<br/>  | <dl> <dt>Оемупжекс. h</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсижетпродуктинфо**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**мсижетусеринфо**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




