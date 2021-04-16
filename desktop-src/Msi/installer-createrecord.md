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
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652287"
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

## <a name="remarks"></a>Комментарии

Поле 0, а не одно из полей в *подсчете*, обычно используется для элементов, ориентированных на запись, таких как строки формата или Op-коды выполнения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




