---
description: '\_Класс WMI взаимосвязей Win32 принтерконтроллер связывает принтер и локальное устройство, к которому подключен принтер. Обратите внимание, что этот класс возвращает только экземпляры для локальных принтеров.'
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Класс Win32_PrinterController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895946"
---
# <a name="win32_printercontroller-class"></a>\_Класс Win32 принтерконтроллер

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ принтерконтроллер** связывает принтер и локальное устройство, к которому подключен принтер. Обратите внимание, что этот класс возвращает только экземпляры для локальных принтеров.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ принтерконтроллер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ принтерконтроллер** имеет следующие свойства.

<dl> <dt>

**акцессстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние доступа контроллера к устройству. Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.

Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Неизвестно

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Активна

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**открыт**


</dt> <dd>

Неактивно

</dd> </dl>

</dd> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ Controller**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Ссылка на экземпляр [**\_ контроллера CIM**](cim-controller.md) , представляющий локальное устройство, связанное с этим принтером.

Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ принтер Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Ссылка на экземпляр [**\_ принтера Win32**](win32-printer.md) , представляющий принтер, связанный с локальным устройством.

Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).

</dd> <dt>

**неготиатеддатавидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ширина данных, используемая между устройствами (если возможны несколько значений ширины данных для шины или соединения). Ширина данных указывается в битах. Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).

Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).

</dd> <dt>

**неготиатедспид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Скорость использования между устройствами (если возможно несколько шин или скорость соединения). Скорость указывается в битах в секунду. Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).

Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**нумберофхардресетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число жестких сбросов, выданных контроллером.

Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).

</dd> <dt>

**нумберофсофтресетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество мягких сбросов, выданных контроллером.

Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ принтерконтроллер** является производным от [**CIM \_ контролледби**](cim-controlledby.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОНТРОЛЛЕДБИ CIM**](cim-controlledby.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
