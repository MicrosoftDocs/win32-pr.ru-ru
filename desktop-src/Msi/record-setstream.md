---
description: Метод Сетстреам объекта Record копирует содержимое указанного файла в указанное поле записи в виде потоковых данных. Данные потока не могут быть вставлены во временные поля.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Метод Record. Сетстреам
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679576"
---
# <a name="recordsetstream-method"></a>Метод Record. Сетстреам

Метод **сетстреам** объекта [**Record**](record-object.md) копирует содержимое указанного файла в указанное поле записи в виде потоковых данных. Данные потока не могут быть вставлены во временные поля.

## <a name="syntax"></a>Синтаксис


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*полями* 
</dt> <dd>

Обязательный номер поля значения в записи, 1.

</dd> <dt>

*Равно* 
</dt> <dd>

Расположение копируемого файла. Перевод какого-либо типа не выполняется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




