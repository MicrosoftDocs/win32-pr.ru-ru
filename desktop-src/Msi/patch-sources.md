---
description: Свойство Sources перечисляет все источники для экземпляра patch. Это свойство вызывает Мсисаурцелистенумсаурцес и возвращает массив строк и принимает тип источника в качестве аргумента.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Свойство patch. sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2a2f190c7d8ae42e43ac934a043dfb1a98a5e15e142415736406ffbd7f3cbc4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042404"
---
# <a name="patchsources-property"></a>Свойство patch. sources

Свойство **Sources** перечисляет все источники для экземпляра patch. Это свойство вызывает [**мсисаурцелистенумсаурцес**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) и возвращает массив строк и принимает тип источника в качестве аргумента.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a>Значение свойства

Тип источника для перечисления. Значение может быть *мсиинсталлсаурцетипенетворк* (1) или *мсиинсталлсаурцетипеурл* (2).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Обновление**](patch-object.md)
</dt> <dt>

[**мсисаурцелистенумсаурцес**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




