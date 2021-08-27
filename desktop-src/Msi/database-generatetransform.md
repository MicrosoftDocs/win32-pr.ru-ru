---
description: Метод GenerateTransform объекта Database создает преобразование, которое при применении к базе данных объектов приводит к созданию справочной базы данных. Преобразование хранится в объекте хранилища.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Database. GenerateTransform, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5c07e7483a43ea4f69eac473c76747447932fba57e53e22f79fa0663d4babc86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129654"
---
# <a name="databasegeneratetransform-method"></a>Database. GenerateTransform, метод

Метод **GenerateTransform** объекта [**Database**](database-object.md) создает [*Преобразование*](t-gly.md) , которое при применении к базе данных объектов приводит к созданию справочной базы данных. Преобразование хранится в объекте хранилища.

Если преобразование должно быть применено во время установки, необходимо использовать метод [**креатетрансформсуммаринфо**](database-createtransformsummaryinfo.md) для заполнения сводного информационного потока.

## <a name="syntax"></a>Синтаксис


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*reference* 
</dt> <dd>

Требуемая база данных, не включающая изменения.

</dd> <dt>

*storage* 
</dt> <dd>

Имя созданного файла преобразования. Это необязательно.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Преобразование может добавлять непервичные ключевые столбцы в конец таблицы. Невозможно создать преобразование, которое добавляет столбцы первичного ключа в таблицу. Невозможно создать преобразование, которое изменяет порядок, имена или определения столбцов.

Этот метод возвращает логическое значение. Он возвращает значение TRUE, если создается преобразование. Он возвращает значение FALSE, если преобразование не создается из-за отсутствия различий между двумя базами данных. Если метод завершается с ошибкой, выдается ошибка.

В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**База данных**](database-object.md)
</dt> <dt>

[Преобразования баз данных](database-transforms.md)
</dt> </dl>

 

 




