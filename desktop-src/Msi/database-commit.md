---
description: Метод Commit объекта Database завершает постоянную форму базы данных.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 049dec8c4d0531240d1244efb5bb7e1f0a3a337f51498d39ae09bcd6cf31c374
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044874"
---
# <a name="databasecommit-method"></a>Database. Commit, метод

Метод **commit** объекта [**Database**](database-object.md) завершает постоянную форму базы данных. Все постоянные данные записываются в базу данных, доступную для записи, а временные столбцы или строки не записываются. Этот метод не влияет на базу данных, открытую только для чтения. Этот метод может вызываться несколько раз для сохранения текущего состояния таблиц, загруженных в память. Когда база данных закрывается, выполняется откат всех изменений, сделанных после последней **фиксации** . Этот метод обычно вызывается перед завершением работы, когда все изменения базы данных были завершены.

## <a name="syntax"></a>Синтаксис


```JScript
Database.Commit()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




