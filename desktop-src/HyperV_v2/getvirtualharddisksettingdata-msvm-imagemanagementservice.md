---
description: Извлекает данные настройки, связанные с файлом виртуального жесткого диска.
ms.assetid: b82c018e-8d23-4615-99c1-3b622a8f41da
title: Метод Жетвиртуалхарддисксеттингдата класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cf8f19d3bbdac593dabef0a1ff8e9c9b60027301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990936"
---
# <a name="getvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a>Метод Жетвиртуалхарддисксеттингдата \_ класса) мсвм

Извлекает данные настройки, связанные с файлом виртуального жесткого диска.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetVirtualHardDiskSettingData(
  [in]  string              Path,
  [out] string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь* \[ окне\]
</dt> <dd>

Полный путь к файлу образа диска.

</dd> <dt>

*SettingData* \[ заполняет\]
</dt> <dd>

В случае успеха получает встроенный экземпляр класса [**мсвм \_ виртуалхарддисксеттингдата**](msvm-virtualharddisksettingdata.md) , который содержит данные параметров для виртуального жесткого диска.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Сбой** (32768)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Не поддерживается** (32770)
</dt> <dt>

**Состояние неизвестно** (32771)
</dt> <dt>

**Время ожидания** (32772)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Система используется** (32774)
</dt> <dt>

**Недопустимое состояние для этой операции** (32775)
</dt> <dt>

**Неверный тип данных** (32776)
</dt> <dt>

**Система недоступна** (32777)
</dt> <dt>

**Недостаточно памяти** (32778)
</dt> <dt>

**Файл не найден** (32779)
</dt> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

В следующем примере C# показано, как вызвать метод [**жетвиртуалхарддискстате**](getvirtualharddiskstate-msvm-imagemanagementservice.md) . Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
public static void GetVirtualHardDiskSettingData(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskSettingData");

    inParams["Path"] = vhdPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskSettingData", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["SettingData"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ )**](msvm-imagemanagementservice.md)
</dt> </dl>

 

