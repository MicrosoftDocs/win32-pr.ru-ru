---
description: Возвращает дескриптор безопасности для пространства имен, к которому подключен пользователь. Этот метод возвращает дескриптор безопасности в двоичном формате массива байтов. При написании скрипта используйте метод Жетсекуритидескриптор.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Получение метода класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702377"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a>Получение метода \_ \_ класса системсекурити

Метод **получает** дескриптор безопасности для пространства имен, к которому подключен пользователь. Этот метод возвращает дескриптор безопасности в двоичном формате массива байтов. При написании скрипта используйте метод [**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md) . Дополнительные сведения см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md).

Пользователь должен иметь разрешение на **Чтение \_** . По умолчанию у администраторов есть такое разрешение. Единственной частью действительно используемого дескриптора безопасности является список управления доступом на уровне пользователей (DACL). Список DACL может содержать как наследуемые, так и неунаследованные ACE. Разрешены и Deny, и Allow.

При программировании на C++ можно управлять двоичным дескриптором безопасности с помощью [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), а также методами преобразования [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="syntax"></a>Синтаксис


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SD* \[ заполняет\]
</dt> <dd>

Дескриптор безопасности в двоичном формате байтового массива.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение HRESULT** , указывающее состояние вызова метода. В следующем списке перечислены возвращаемые значения, которые являются значимыми **для получения**. Для сценариев и Visual Basic приложений результат можно получить из [параметров out. returnValue](parsing-outparameters-objects.md). Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_ОК**
</dt> <dd>

Метод успешно выполнен.

</dd> <dt>

**\_ \_ отказано в доступе к WBEM \_**
</dt> <dd>

Вызывающий объект не имеет достаточных прав для вызова этого метода.

</dd> <dt>

**\_метод WBEM \_ E \_ отключен**
</dt> <dd>

Попытка запустить этот метод в неподдерживаемой системе.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Дополнительные сведения об изменении безопасности пространства имен программным путем или вручную см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Примеры

Следующий скрипт показывает, как использовать метод **получает** , чтобы получить текущий дескриптор безопасности для корневого \\ пространства имен CIMV2 и изменить его на массив байтов, показанный в **отображении**.


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_системсекурити**](--systemsecurity.md)
</dt> <dt>

[Константы безопасности WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_\_Системсекурити:: настраивается**](--systemsecurity-setsd.md)
</dt> <dt>

[**\_Дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Защита пространств имен WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

