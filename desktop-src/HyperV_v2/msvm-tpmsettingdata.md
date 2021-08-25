---
description: Представляет настроенное состояние устройства TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Класс Msvm_TPMSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f25cd57e1f3cd6ebf015009af176b3bcc68c1d271836c5bb548b9358e9007086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899124"
---
# <a name="msvm_tpmsettingdata-class"></a>\_Класс мсвм тпмсеттингдата

Представляет настроенное состояние устройства TPM.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ тпмсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ тпмсеттингдата** имеет следующие свойства.

<dl> <dt>

**Защищаемые**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**значение true** , чтобы задать политику для защиты данных виртуальной машины. в противном случае — **значение false**. Вновь созданный модуль TPM отключен, поэтому начальное состояние защиты данных — **false**.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Включенные и отключенные состояния элемента. Значение по умолчанию — **disabled**.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**кэйпротектор**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **октетстринг**
</dt> </dl>

Предохранитель ключа от клиента службы защиты узла.

</dd> <dt>

**ласткновнгудкэйпротектор**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **октетстринг**
</dt> </dl>

Последний известный хороший предохранитель ключа успешно зашифровал состояние устройства TPM во время последней загрузки виртуальной машины.

Это свойство доступно только для чтения для клиента WMI и может быть изменено только устройством TPM виртуальной машины.

</dd> <dt>

**Экранирование**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**значение true** , чтобы определить политику, которая изолирует виртуальную машину. в противном случае — **значение false**. Вновь созданный модуль TPM отключен, поэтому начальное состояние экранирования — **false**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Окончание поддержки клиента<br/>    | Windows 10,<br/>                                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

