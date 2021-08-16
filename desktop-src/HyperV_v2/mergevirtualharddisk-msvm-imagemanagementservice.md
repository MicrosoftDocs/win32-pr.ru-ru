---
description: Слияние дочернего виртуального жесткого диска в цепочке разностного с одним или несколькими родительскими виртуальными жесткими дисками в цепочке.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Метод Мержевиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fa9867222cf27e6ca23a4d96a04a6b94b558e7c043f182fdf8d8331ad73010c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644876"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Метод Мержевиртуалхарддиск \_ класса) мсвм

Слияние дочернего виртуального жесткого диска в цепочке разностного с одним или несколькими родительскими виртуальными жесткими дисками в цепочке. Ограничения на использование для этого метода см. в разделе Примечания.

Если пользователь, выполняющий эту функцию, не имеет разрешения на обновление виртуальных машин, то эта функция завершится ошибкой.

## <a name="syntax"></a>Синтаксис


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Источник* \[ окне\]
</dt> <dd>

Тип: **строка**

Полный путь, указывающий расположение файла виртуального жесткого диска для слияния.

</dd> <dt>

*DestinationPath* \[ окне\]
</dt> <dd>

Тип: **строка**

Полный путь, указывающий расположение файла родительского виртуального жесткого диска, в который должны быть объединены данные. Это может быть непосредственный родительский виртуальный жесткий диск файла слияния или образа родительского диска, а несколько уровней разностной цепочки.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Этот метод может возвращать одно из следующих значений.

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

## <a name="remarks"></a>Remarks

Дочерний виртуальный жесткий диск должен быть вне сети.

С этим методом можно использовать только следующие типы виртуальных жестких дисков:

-   Разностный виртуальный жесткий диск
-   Разностные VHDX

Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

В следующем примере кода C# разворачивается файл виртуального жесткого диска. Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Мсвм \_ )**](msvm-imagemanagementservice.md)
</dt> </dl>

 

