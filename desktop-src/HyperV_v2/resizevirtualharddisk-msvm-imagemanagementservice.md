---
description: Изменяет размер существующего виртуального жесткого диска.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Метод Ресизевиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682830"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Метод Ресизевиртуалхарддиск \_ класса) мсвм

Изменяет размер существующего виртуального жесткого диска. Виртуальный жесткий диск должен быть вне сети. Ограничения на использование для этого метода см. в разделе Примечания.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь* \[ окне\]
</dt> <dd>

Тип: **строка**

Полный путь к файлу виртуального жесткого диска.

</dd> <dt>

*Максинтерналсизе* \[ окне\]
</dt> <dd>

Тип: **UInt64**

Максимальный размер виртуального жесткого диска, отображаемый виртуальной машиной в байтах. Минимальное значение *максинтерналсизе* — *DiskSize* + 512 — (*DiskSize* mod 512). *DiskSize* — это размер файла виртуального жесткого диска в байтах. Если указанное значение *максинтерналсизе* меньше минимального значения, возвращается ошибка инвалидпараметер (32773).

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

## <a name="remarks"></a>Комментарии

С этим методом можно использовать только следующие типы виртуальных жестких дисков при увеличении размера виртуального жесткого диска:

-   Фиксированный виртуальный жесткий диск
-   Фиксированный VHDX
-   Динамический виртуальный жесткий диск
-   Динамические VHDX
-   Разностные VHDX

С этим методом можно использовать только следующие типы виртуальных жестких дисков при уменьшении размера виртуального жесткого диска:

-   Фиксированный VHDX
-   Динамические VHDX
-   Разностные VHDX

Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

В следующем примере кода C# разворачивается файл виртуального жесткого диска. Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Мсвм \_ )**](msvm-imagemanagementservice.md)
</dt> </dl>

 

