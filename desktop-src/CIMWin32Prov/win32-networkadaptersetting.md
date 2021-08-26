---
description: '\_Класс WMI взаимосвязей Win32 нетворкадаптерсеттинг связывает сетевой адаптер и его параметры конфигурации.'
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Класс Win32_NetworkAdapterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f7330e5b6a2b86508528bb1136acd58b308ca4b9c44b31b9b6e0777f4eccd19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972677"
---
# <a name="win32_networkadaptersetting-class"></a>\_Класс Win32 нетворкадаптерсеттинг

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ нетворкадаптерсеттинг** связывает сетевой адаптер и его параметры конфигурации.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ нетворкадаптерсеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ нетворкадаптерсеттинг** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ сетевого адаптера**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ сетевого адаптера")
</dt> </dl>

[**\_ Сетевого адаптера Win32**](win32-networkadapter.md) , описывающий свойства сетевого адаптера, использующего определенный параметр сетевого адаптера.

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ NetworkAdapterConfiguration**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")
</dt> </dl>

[**\_ NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) , описывающий параметры конфигурации, используемые сетевым адаптером.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ нетворкадаптерсеттинг** является производным от [**Win32 \_ девицесеттингс**](win32-devicesettings.md).

Сведения о том, как использовать классы ассоциаций, см. в разделе [соединители оператора](../wmisdk/associators-of-statement.md).

## <a name="examples"></a>Примеры

Следующий пример VBScript использует **Win32 \_ нетворкадаптерсеттинг** для задания IP-адреса подключения по локальной сети.


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Девицесеттингс Win32**](win32-devicesettings.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> <dt>

[Задачи WMI: Сетевые подключения](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
