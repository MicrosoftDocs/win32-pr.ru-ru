---
description: Метод Реадстреам объекта Record считывает указанное число байтов из поля записи, содержащего потоковые данные.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Метод Record. Реадстреам
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668636"
---
# <a name="recordreadstream-method"></a>Метод Record. Реадстреам

Метод **реадстреам** объекта [**Record**](record-object.md) считывает указанное число байтов из поля записи, содержащего потоковые данные.

## <a name="syntax"></a>Синтаксис


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*полями* 
</dt> <dd>

Номер поля, требуемого для значения в записи, 1.

</dd> <dt>

*length* 
</dt> <dd>

Требуемое число байтов для чтения из потока.

</dd> <dt>

*format* 
</dt> <dd>

Требуется интерпретация и возвращение байтов данных.



| Имя параметра                                                                                                                                                                                                                                                                  | Значение                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <dt>**мсиреадстреаминтежер**</dt> <dt>0</dt> </dl> | В виде длинного целого числа длина должна быть от 1 до 4.<br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <dt>**мсиреадстреамбитес**</dt> <dt>1</dt> </dl>         | Данные в виде **BSTR**— один байт на символ.<br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <dt>**мсиреадстреаманси**</dt> <dt>2</dt> </dl>             | Байты ANSI, переведенные в Юникод **BSTR**.<br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <dt>**мсиреадстреамдирект**</dt> <dt>3</dt> </dl>     | Пары байтов, возвращаемые непосредственно в виде **BSTR**.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает строку, содержащую запрошенное число байтов, считанных из поля записи.

## <a name="remarks"></a>Комментарии

Возвращенное значение несуществующего поля является пустым значением. Если в потоке меньше байтов, запрошенных счетчиком, возвращаемая строка сокращается соответствующим образом.

Пример этого метода см. [в разделе Копирование файла ANSI в поле базы данных](copy-ansi-file-into-a-database-field.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




