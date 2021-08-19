---
description: Представляет идентифицирующие сведения о видеомониторе, например название производителя, год изготовления или серийный номер.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Класс Вмимониторид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 552e66a4e3a0c6f120bcc95123e3a2674fc579457de16c9ef8cd1e80161f175e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051152"
---
# <a name="wmimonitorid-class"></a>Класс Вмимониторид

Класс WMI **вмимониторид** представляет идентифицирующие сведения о видеомониторе, например название производителя, год изготовления или серийный номер. Данные в этом классе соответствуют данным в блоке идентификации поставщика или продукта определение входного видео для расширенного расширенного представления идентификационных данных (E-EDID).

## <a name="syntax"></a>Синтаксис

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a>Члены

Класс **вмимониторид** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **вмимониторид** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает активный монитор.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Имя конкретного экземпляра монитора.

</dd> <dt>

**ManufacturerName**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя производителя.

</dd> <dt>

**мануфактурернамеленгс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Длина имени производителя, расположенного в свойстве **ManufacturerName** .

</dd> <dt>

**продукткодеид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Код продукта, назначенный поставщиком.

</dd> <dt>

**сериалнумберид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Серийный номер.

</dd> <dt>

UserFriendlyName
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Понятное имя монитора. Размер имени — это длина, заданная свойством Усерфриендлинамеленгс.

</dd> <dt>

усерфриендлинамеленгс
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число символов в имени, расположенном в свойстве Усерфриендлинаме.

</dd> <dt>

**викофмануфактуре**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Неделя производства по номеру недели. Диапазон — от 1 до 53. Ноль (0) не определен.

</dd> <dt>

**еарофмануфактуре**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Год изготовления.

</dd> </dl>

## <a name="remarks"></a>Remarks

Обсуждение того, как преобразовать массивы, в которых хранится идентификатор серийного номера, см. в статье [о мониторе отчетов с Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) .

## <a name="examples"></a>Примеры

В следующем примере PowerShell извлекается серийный номер нескольких мониторов.


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



Следующий код VBScript также извлекает сведения об ИДЕНТИФИКАТОРах монитора из системы.


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мсмониторкласс**](msmonitorclass.md)
</dt> </dl>

 

