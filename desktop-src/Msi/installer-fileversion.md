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
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651604"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




