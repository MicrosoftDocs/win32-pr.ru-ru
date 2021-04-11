---
description: Создает моментальный снимок виртуальной машины.
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: Метод CreateSnapshot класса Msvm_VirtualSystemSnapshotService (Дбдаоинт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c62b4abf60e367da1c4ac4b176e5f5d70f547c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346365"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Метод CreateSnapshot \_ класса Виртуалсистемснапшотсервице мсвм

Создает моментальный снимок виртуальной машины.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедсистем* \[ окне\]
</dt> <dd>

Ссылка на класс [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину для создания моментального снимка.

</dd> <dt>

*Снапшотсеттингс* \[ окне\]
</dt> <dd>

Строка, содержащая встроенный экземпляр класса [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) , который содержит настройки параметров для моментального снимка. Этот параметр является необязательным и может быть пустой строкой.

</dd> <dt>

*Снапшоттипе* \[ окне\]
</dt> <dd>

Указывает тип запрошенного моментального снимка. Это должно быть одно из следующих значений.

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Полный моментальный снимок** (2)


</dt> <dd>

Завершите создание моментального снимка виртуальной машины.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Моментальный снимок диска** (3)


</dt> <dd>

Моментальный снимок дисков виртуальной машины.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)


</dt> <dd></dd> </dl> </dd> <dt>

*Ресултингснапшот* \[ в, out\]
</dt> <dd>

Ссылка на объект [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющий результирующий моментальный снимок виртуальной машины.

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

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Недопустимый параметр** (4)
</dt> <dt>

**Недопустимое состояние** (5)
</dt> <dt>

**Недопустимый тип** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="examples"></a>Примеры

В следующем примере кода C# создается виртуальная машина. Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Дбдаоинт. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемснапшотсервице**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**Креатевиртуалсистемснапшот (v1)**](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

