---
description: Метод Import объекта базы данных импортирует таблицу базы данных из текстовых архивных файлов, удаляя любую существующую таблицу.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Метод Database. Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31bd306475460b03e9b4b5137cbd8fe214128dbec0dac516d2d9557de137a82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075034"
---
# <a name="databaseimport-method"></a>Метод Database. Import

Метод **Import** объекта [**базы данных**](database-object.md) импортирует таблицу базы данных из [текстовых архивных файлов](text-archive-files.md), удаляя любую существующую таблицу.

## <a name="syntax"></a>Синтаксис


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*путь* 
</dt> <dd>

Обязательная папка, в которой находится текстовый файл.

</dd> <dt>

*file* 
</dt> <dd>

Обязательное имя импортируемого файла. Сюда не входит папка, которая должна быть задана в объекте Path. Имя таблицы указывается в файле.

</dd> </dl>

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**База данных**](database-object.md)
</dt> <dt>

[**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




