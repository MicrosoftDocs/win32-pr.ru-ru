---
description: Метод Креатетрансформсуммаринфо объекта Database создает и заполняет поток сводных данных существующего файла преобразования. Этот метод заполняет свойства базовыми и ссылочными ProductCode и ProductVersion.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Database. Креатетрансформсуммаринфо, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e1daa3e31ccfb49e49842994d6203b58534d86c111cd98652e66079fa47322cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745734"
---
# <a name="databasecreatetransformsummaryinfo-method"></a>Database. Креатетрансформсуммаринфо, метод

Метод **креатетрансформсуммаринфо** объекта [**Database**](database-object.md) создает и заполняет поток сводных данных существующего файла преобразования. Этот метод заполняет свойства базовыми и ссылочными [**ProductCode**](productcode.md) и [**ProductVersion**](productversion.md).

## <a name="syntax"></a>Синтаксис


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
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

</dd> <dt>

*ерроркондитионс* 
</dt> <dd>

Обязательные условия ошибки, которые следует подавлять при применении преобразования. Объедините одно или несколько следующих значений условий ошибки.



| Имя условия ошибки                                                                                                                                                                                                                                                                                                                                        | Значение                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <dt>**мситрансформеррорноне**</dt> <dt>0</dt> </dl>                                                                         | Ни одно из следующих условий не задано.<br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**мситрансформеррораддексистингров**</dt> <dt>1</dt> </dl>                                 | Добавляет уже существующую строку.<br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**мситрансформеррорделетенонексистингров**</dt> <dt>2</dt> </dl>         | Удаляет несуществующую строку.<br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**мситрансформеррораддексистингтабле**</dt> <dt>4</dt> </dl>                         | Добавляет уже существующую таблицу.<br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**мситрансформеррорделетенонексистингтабле**</dt> <dt>8</dt> </dl> | Удаляет несуществующую таблицу.<br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**мситрансформеррорупдатенонексистингров**</dt> <dt>16</dt> </dl>        | Обновляет несуществующую строку.<br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**мситрансформеррорчанжекодепаже**</dt> <dt>32</dt> </dl>                                | Кодовые страницы преобразований и баз данных не совпадают, и ни одна кодовая страница не является нейтральной.<br/> |



 

</dd> <dt>

*validation* 
</dt> <dd>

Требуется при применении преобразования к базе данных. показывает, какие свойства должны быть проверены, чтобы убедиться, что это преобразование может быть применено к базе данных. Все свойства содержатся в [наборе свойств потока сводных данных](summary-information-stream-property-set.md).

Объедините одно или несколько из следующих значений.



| Флаг проверки                                                                                                                                                                                                                                                                                                         | Значение                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <dt>**мситрансформвалидатионноне**</dt> <dt>0</dt> </dl>                 | Проверка не выполнена.<br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <dt>**мситрансформвалидатионлангуаже**</dt> <dt>1</dt> </dl> | Язык по умолчанию должен соответствовать базовой базе данных.<br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <dt>**мситрансформвалидатионпродукт**</dt> <dt>2</dt> </dl>     | Продукт должен соответствовать базовой базе данных.<br/>          |



 

Чтобы проверить версию продукта, сначала выберите один или несколько из этих трех флагов, чтобы указать, какая часть версии должна быть проверена.



| Флаг проверки                                                                                                                                                                                                                                                                                                              | Значение                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <dt>**мситрансформвалидатионмажорвер**</dt> <dt>8</dt> </dl>      | Проверяет только основной номер версии.<br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <dt>**мситрансформвалидатионминорвер**</dt> <dt>16</dt> </dl>     | Проверяет только основной и дополнительный номер версии.<br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <dt>**мситрансформвалидатионупдатевер**</dt> <dt>32</dt> </dl> | Проверяет основные, дополнительные и обновленные версии.<br/> |



 

Затем выберите один из следующих элементов, чтобы указать требуемую связь между версией продукта базы данных, к которой применяется преобразование, и базой данных в базовой базе.



| Флаг проверки                                                                                                                                                                                                                                                                                                                                   | Значение                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <dt>**мситрансформвалидатионлесс**</dt> <dt>64</dt> </dl>                                          | Примененная версия < базовая версия<br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <dt>**мситрансформвалидатионлессорекуал**</dt> <dt>128</dt> </dl>             | Примененная версия <= базовая версия<br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <dt>**мситрансформвалидатионекуал**</dt> <dt>256</dt> </dl>                                     | Примененная версия = базовая версия<br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <dt>**мситрансформвалидатионгреатерорекуал**</dt> <dt>512</dt> </dl> | Примененная версия >= базовая версия<br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <dt>**мситрансформвалидатионгреатер**</dt> <dt>1024</dt> </dl>                            | Примененная версия > базовая версия<br/>  |



 

Чтобы убедиться, что преобразование применяется к пакету с соответствующим параметром [**UpgradeCode**](upgradecode.md), установите следующий флаг.



| Флаг проверки                                                                                                                                                                                                                                                                                                                        | Значение                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <dt>**мситрансформвалидатионупградекоде**</dt> <dt>2048</dt> </dl> | Проверяет, что преобразование является соответствующим параметром [**UpgradeCode**](upgradecode.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Чтобы создать информационный поток сводки для преобразования, свойства [**ProductCode**](productcode.md) и [**ProductVersion**](productversion.md) должны быть определены в таблицах [свойств](property-table.md) базовых и эталонных баз данных. Если используется Мситрансформвалидатионупградекоде, свойство [**UpgradeCode**](upgradecode.md) должно быть определено в обеих базах данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Преобразования баз данных](database-transforms.md)
</dt> </dl>

 

 




