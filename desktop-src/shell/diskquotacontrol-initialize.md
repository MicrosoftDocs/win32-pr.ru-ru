---
description: Открывает указанный том и инициализирует его объект управления квотой.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Iniметод тиализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984248"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Iniметод тиализе

Открывает указанный том и инициализирует его объект управления квотой.

## <a name="syntax"></a>Синтаксис


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*спас* 
</dt> <dd>

Тип: **строка**

Строковое значение, содержащее полный путь к тому, который должен быть инициализирован.

</dd> <dt>

*бреадврите* 
</dt> <dd>

Тип: **Boolean**

Логическое значение, указывающее способ открытия тома. Задайте для параметра *Бреадврите* **значение true** для доступа на чтение и запись или **false** для доступа только для чтения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




