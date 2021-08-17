---
description: свойство Version объекта Installer является свойством только для чтения, которое является строковым представлением текущей версии установщик Windows. Строка возвращается в следующей форме.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Свойство установщика. Version
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3d2aeb845647317751eba53caae1609f8d3d66f9f7d373aa7faa24e3b8cdfb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119295553"
---
# <a name="installerversion-property"></a>Свойство установщика. Version

свойство **Version** объекта [**Installer**](installer-object.md) является свойством только для чтения, которое является строковым представлением текущей версии установщик Windows. Строка возвращается в следующей форме.

*основной*. *дополнительный номер*. *Сборка*. *Обновление*

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




