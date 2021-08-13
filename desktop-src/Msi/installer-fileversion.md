---
description: Метод FileVersion объекта Installer возвращает строку версии или строку языка пути, указанного в параметре path, используя формат, в котором установщик планирует найти их в базе данных.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Метод Installer. FileVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 492ebb0c7678b7819f3abc423517dcf77d071b81009c3b12017b1b627bb84057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630586"
---
# <a name="installerfileversion-method"></a>Метод Installer. FileVersion

Метод **FileVersion** объекта [**Installer**](installer-object.md) возвращает строку версии или строку языка пути, указанного в параметре *path* , используя формат, в котором установщик планирует найти их в базе данных. Для версий это строка в \# формате ". \# . \# . \# ". Для языка это Десятичный идентификатор языка.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь* 
</dt> <dd>

Обязательная строка, содержащая путь к файлу.

</dd> <dt>

*Язык* 
</dt> <dd>

Флаг, определяющий, является ли возвращаемое значение ИДЕНТИФИКАТОРом языка или строкой версии. TRUE Возвращает язык, FALSE Возвращает версию. Этот параметр является необязательным и имеет значение по умолчанию FALSE.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




