---
description: '&Win32 \_ привилежесстатус \# 8194; Класс WMI сообщает сведения о привилегиях, необходимых для выполнения операции. Он может быть возвращен при сбое операции или при возвращении частично заполненного экземпляра.'
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Класс Win32_PrivilegesStatus (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e2c2b2329884b22eecdc00a629abb8d05bc87435ce06d35e51907cb4095c8fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020092"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a>Класс Win32_PrivilegesStatus (поставщики WMI CIMWin32)

 [Класс WMI](../wmisdk/retrieving-a-class.md) **\_ привилежесстатус для Win32** сообщает сведения о привилегиях, необходимых для выполнения операции. Он может быть возвращен при сбое операции или при возвращении частично заполненного экземпляра.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ привилежесстатус** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ привилежесстатус** имеет следующие свойства.

<dl> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Любая определяемая пользователем строка, описывающая ошибку или оперативное состояние.

Это свойство наследуется от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**Операция**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Операция, выполняемая во время сбоя или аномалии. как правило, инструментарий управления Windows (WMI) (WMI) задает для этого свойства имя API COM для метода WMI, например: [**IWbemServices:: CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).

Это свойство наследуется от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Параметры, участвующие в изменении состояния или ошибки. Например, если приложение пытается извлечь несуществующий класс, для этого свойства задается имя класса, вызвавшего ошибку.

Это свойство наследуется от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**привилежесноселд**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT privileges")
</dt> </dl>

Список необходимых привилегий доступа отсутствует для завершения операции. типы привилегий доступа можно найти в Windowsных привилегиях.

пример: "SE \_ SHUTDOWN \_ NAME"

</dd> <dt>

**привилежесрекуиред**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT privileges")
</dt> </dl>

Список всех привилегий, необходимых для выполнения операции. К ним относятся значения из свойства **привилежесноселд** .

пример: "SE \_ SHUTDOWN \_ NAME"

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет поставщика, который вызывает или сообщает об ошибке или изменении состояния. если поставщик не задействован, для этой строки задается значение "управление Windows".

Это свойство наследуется от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Содержит код ошибки или сведения для операции. Это может быть любое значение, определенное поставщиком, но значение 0 (нуль) обычно зарезервировано для обозначения успеха.

Это свойство наследуется от [**\_ \_ нотифистатус**](../wmisdk/--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ привилежесстатус** является производным от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_екстендедстатус**](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
