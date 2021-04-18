---
description: Используется для передачи подробных сведений о состоянии и ошибке.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: Класс __ExtendedStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713114"
---
# <a name="__extendedstatus-class"></a>\_\_Класс Екстендедстатус

Класс System **\_ \_ екстендедстатус** используется для передачи подробных сведений о состоянии и ошибках.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ екстендедстатус** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ екстендедстатус** имеет следующие свойства.

<dl> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Любая определяемая пользователем строка, описывающая ошибку или оперативное состояние.

</dd> <dt>

**Операция**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Операция, выполняемая во время сбоя или аномалии. Как правило, инструментарий управления Windows (WMI) (WMI) задает для этого свойства имя API COM для метода WMI, например: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Параметры, участвующие в изменении состояния или ошибки. Например, если приложение пытается извлечь несуществующий класс, для этого свойства задается имя класса, вызвавшего ошибку.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет поставщика, который вызывает или сообщает об ошибке или изменении состояния. Если поставщик не задействован, для этой строки задается значение "Управление Windows".

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Содержит код ошибки или сведения для операции. Это может быть любое значение, определенное поставщиком, но значение 0 (нуль) обычно зарезервировано для обозначения успеха. Это свойство наследуется от [**\_ \_ нотифистатус**](--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ екстендедстатус** является производным от класса [**\_ \_ нотифистатус**](--notifystatus.md) .

Используйте класс **\_ \_ екстендедстатус** , чтобы сообщить более сложную информацию, чем простой код результата. Поставщики могут создавать собственные классы от **\_ \_ екстендедстатус** , если им требуются дополнительные свойства для описания ошибок.

Свойство **StatusCode** , унаследованное от родительского класса [**\_ \_ нотифистатус**](--notifystatus.md) , представляет собой целое число без знака, представляющее ошибку или значение состояния. Когда экземпляры этого класса возвращаются из метода динамическим поставщиком, свойства **StatusCode** и **Description** задаются поставщиком, а другие свойства устанавливаются WMI.

## <a name="examples"></a>Примеры

Следующий пример кода, взятый из [FND: как выполнять обработку Configuration Manager асинхронных ошибок с помощью](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) примера кода на языке сценариев VBScript в коллекции TechNet, описывает использование **\_ \_ екстендедстатус** для получения сведений об ошибках.


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_нотифистатус**](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> </dl>

 

