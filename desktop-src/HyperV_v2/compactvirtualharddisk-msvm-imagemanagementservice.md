---
description: Сжимает файл виртуального жесткого диска.
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Метод Компактвиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683761"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Метод Компактвиртуалхарддиск \_ класса) мсвм

Сжимает файл виртуального жесткого диска. Сжатие — это процесс освобождения неиспользуемых частей виртуального жесткого диска. Виртуальный жесткий диск не подключен автоматически. Ограничения на использование для этого метода см. в разделе Примечания.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь* \[ окне\]
</dt> <dd>

Тип: **строка**

Полный путь, указывающий расположение файла слияния.

</dd> <dt>

*Режим* \[ окне\]
</dt> <dd>

Тип: **UInt16**

Задает режим для операции Compact. Это должно быть одно из следующих значений.

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

**Full** (0)


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

**Быстрый** (1)


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

Повторно **обрезать** (2)


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

**Предобрезанные** (3)


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

**До нуля** (4)


</dt> <dd></dd> </dl> </dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**

Ссылка на задание (может иметь **значение NULL** , если задача завершена).

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

С этим методом можно использовать только следующие типы виртуальных жестких дисков:

-   Фиксированный VHDX
-   Динамический виртуальный жесткий диск
-   Динамические VHDX
-   Разностный виртуальный жесткий диск
-   Разностные VHDX

Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

В следующем примере C# сжимается виртуальный жесткий диск. Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
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

 

