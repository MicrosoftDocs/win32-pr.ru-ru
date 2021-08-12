---
description: Метод СоздатьЗапись объекта Installer возвращает новый объект Record с запрошенным числом полей.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Метод Installer. СоздатьЗапись
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: da9c6132b79706cca2135ffcea1bff09040e15a90af5b8b3b1b7175a41229dc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631915"
---
# <a name="installercreaterecord-method"></a>Метод Installer. СоздатьЗапись

Метод **СоздатьЗапись** объекта [**Installer**](installer-object.md) возвращает новый объект [**Record**](record-object.md) с запрошенным числом полей.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*count* 
</dt> <dd>

Требуемое число полей, которое может быть равно 0. Максимальное число полей в записи ограничено 65535.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Поле 0, а не одно из полей в *подсчете*, обычно используется для элементов, ориентированных на запись, таких как строки формата или Op-коды выполнения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




