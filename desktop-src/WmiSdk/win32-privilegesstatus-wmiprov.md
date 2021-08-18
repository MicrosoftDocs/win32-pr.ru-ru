---
description: '&Win32 \_ привилежесстатус \# 8194; Класс WMI сообщает сведения о привилегиях, необходимых для выполнения операции. Он может быть возвращен при сбое операции или при возвращении частично заполненного экземпляра.'
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Класс Win32_PrivilegesStatus (WMI)
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
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 97276023325dc4e2a460daefd35ee01104b5c0adf5c855f145e0f11c954eba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757634"
---
# <a name="win32_privilegesstatus-class-wmi"></a>Класс Win32_PrivilegesStatus (WMI)

[Класс WMI](retrieving-a-class.md) **\_ привилежесстатус для Win32** сообщает сведения о привилегиях, необходимых для выполнения операции.    Он может быть возвращен при сбое операции или при возвращении частично заполненного экземпляра.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
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

Это свойство наследуется от [**\_ \_ екстендедстатус**](--extendedstatus.md).

</dd> <dt>

**Операция**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Операция, выполняемая во время сбоя или аномалии. как правило, инструментарий управления Windows (WMI) (WMI) задает для этого свойства имя API COM для метода WMI, например: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

Это свойство наследуется от [**\_ \_ екстендедстатус**](--extendedstatus.md).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Параметры, участвующие в изменении состояния или ошибки. Например, если приложение пытается извлечь несуществующий класс, для этого свойства задается имя класса, вызвавшего ошибку.

Это свойство наследуется от [**\_ \_ екстендедстатус**](--extendedstatus.md).

</dd> <dt>

**привилежесноселд**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список необходимых привилегий доступа отсутствует для завершения операции. типы привилегий доступа можно найти в Windowsных привилегиях.

пример: "SE \_ SHUTDOWN \_ NAME"

</dd> <dt>

**привилежесрекуиред**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
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

Это свойство наследуется от [**\_ \_ екстендедстатус**](--extendedstatus.md).

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Содержит код ошибки или сведения для операции. Это может быть любое значение, определенное поставщиком, но значение 0 (нуль) обычно зарезервировано для обозначения успеха. Это свойство наследуется от [**\_ \_ нотифистатус**](--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ привилежесстатус** является производным от [**\_ \_ екстендедстатус**](--extendedstatus.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                     |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_екстендедстатус**](--extendedstatus.md)
</dt> </dl>

 

 




