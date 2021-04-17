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
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652134"
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

## <a name="remarks"></a>Комментарии

В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




