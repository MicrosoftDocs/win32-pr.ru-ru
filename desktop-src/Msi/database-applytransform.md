---
description: Метод Апплитрансформ объекта Database применяет преобразование к этой базе данных.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Database. Апплитрансформ, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9c3424dab82b6981af033b40b33481937fd7c36d3c00dcf3ddfcba5f13f56ec7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289624"
---
# <a name="databaseapplytransform-method"></a>Database. Апплитрансформ, метод

Метод **апплитрансформ** объекта [**Database**](database-object.md) применяет преобразование к этой базе данных.

## <a name="syntax"></a>Синтаксис


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*storage* 
</dt> <dd>

Путь к примененному файлу преобразования. Это обязательный параметр.

</dd> <dt>

*ерроркондитионс* 
</dt> <dd>

Указывает условия ошибки, которые следует подавлять. Укажите как сочетание следующих целочисленных значений.



| Условие ошибки                                                                                                                                                                                                                                                                                                                                                  | Значение                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**мситрансформеррораддексистингров**</dt> <dt>0x0001</dt> </dl>                                 | Добавляет уже существующую строку.<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**мситрансформеррорделетенонексистингров**</dt> <dt>0x0002</dt> </dl>         | Удаляет несуществующую строку.<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**мситрансформеррораддексистингтабле**</dt> <dt>0x0004</dt> </dl>                         | Добавляет уже существующую таблицу.<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**мситрансформеррорделетенонексистингтабле**</dt> <dt>0x0008</dt> </dl> | Удаляет несуществующую таблицу.<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**мситрансформеррорупдатенонексистингров**</dt> <dt>0x0010</dt> </dl>         | Обновляет несуществующую строку.<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**мситрансформеррорчанжекодепаже**</dt> <dt>0x0020</dt> </dl>                                 | Кодовые страницы преобразований и баз данных не совпадают, и ни одна из них не имеет нейтральной кодовой страницы.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**мситрансформеррорвиевтрансформ**</dt> <dt>0x0100</dt> </dl>                                     | Создает временную [ \_ таблицу данных reformview](-transformview-table.md).<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод **апплитрансформ** задерживает Преобразование таблиц до последнего возможного момента. Шаги, выполняемые в **апплитрансформ** , позволяют немедленно преобразовать каталоги таблиц и столбцов для базы данных. Каталоги таблиц и столбцов обновляются в соответствии с добавлением или удалением таблицы и добавлением столбца (удаление столбцов запрещено). Если таблица в данный момент загружена в память и ее необходимо преобразовать, она преобразуется. В противном случае для состояния таблицы задается значение, для которого требуется преобразование, чтобы при загрузке таблицы или при фиксации базы данных было применено преобразование. Преобразование в этом экземпляре означает, что фактические (строки) данные таблицы добавляются, удаляются или обновляются.

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

[Преобразования баз данных](database-transforms.md)
</dt> </dl>

 

 




