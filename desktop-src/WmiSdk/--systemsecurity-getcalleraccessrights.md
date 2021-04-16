---
description: Устанавливает параметр прав в виде точечного рисунка с каждым битом, соответствующим прав доступа.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Метод Жеткаллеракцессригхтс класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702751"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a>Метод Жеткаллеракцессригхтс \_ \_ класса системсекурити

Метод **\_ \_ системсекурити:: жеткаллеракцессригхтс** устанавливает параметр *Rights* в виде точечного рисунка с каждым битом, соответствующим право доступа. Любой клиент может вызвать эту функцию, чтобы определить, какие права у клиента. Этот метод полезен для клиентов, которые включают или отключают функции. Например, приложение с графическим пользовательским интерфейсом может отключить кнопку, если у пользователя, выполнившего вход в систему, нет прав на выполнение метода.

Любой включенный клиент имеет право вызывать **жеткаллеракцессригхтс**, даже если у этого клиента нет прав на выполнение метода общего доступа.

## <a name="syntax"></a>Синтаксис


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*права доступа* \[ заполняет\]
</dt> <dd>

Права доступа клиента. Дополнительные сведения см. в разделе [**\_ \_ системсекурити**](--systemsecurity.md) и [константы безопасности WMI](wmi-security-constants.md).

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ВКЛЮЧИТЬ** (1 (0x1))


</dt> <dd>

Включает учетную запись и предоставляет пользователю разрешения на чтение. Это право доступа по умолчанию для всех пользователей.

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ \_Выполнение метода** (2 (0x2))


</dt> <dd>

Разрешает выполнение методов.

> [!Note]  
> Поставщики могут выполнять дополнительные проверки доступа.

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ ПОЛНЫЙ \_ \_ представитель** (4 (0x4))


</dt> <dd>

Позволяет вызывающему, контексту безопасности или пользователю выполнять запись в классы и экземпляры, кроме системных классов.

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ Представитель частичной записи** (8 (0x8))


</dt> <dd>

Позволяет вызывающему, контексту безопасности или пользователю записывать экземпляры поставщика, но не статические классы или статические экземпляры в репозиторий.

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Поставщик записи** (16 (0x10))


</dt> <dd>

Позволяет вызывающему, контексту безопасности или пользователю создавать классы и экземпляры для поставщиков.

> [!Note]  
> Олицетворение поставщиков может выполнять дополнительные проверки доступа.

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ УДАЛЕННЫЙ \_ доступ** (32 (0x20))


</dt> <dd>

Позволяет учетной записи пользователя удаленно выполнять любые операции, разрешенные разрешениями, заданными другими битами.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072 (0x20000))


</dt> <dd>

Разрешает доступ на чтение к дескрипторам безопасности.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144 (0x40000))


</dt> <dd>

Разрешает доступ на запись к избирательным спискам управления доступом (DACL).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение HRESULT** , указывающее состояние вызова метода. В следующем списке перечислены возвращаемые значения, которые являются значимыми для [**Set9XUserList**](--systemsecurity-set9xuserlist.md). Для сценариев и Visual Basic приложений результат можно получить из [параметров out. returnValue](parsing-outparameters-objects.md). Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_метод WBEM \_ E \_ отключен**
</dt> <dd>

Этот метод не поддерживается в поддерживаемых версиях Windows.

</dd> </dl>

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

[**\_\_Системсекурити:: получает**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_Системсекурити:: настраивается**](--systemsecurity-setsd.md)
</dt> <dt>

[Константы безопасности WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Защита пространств имен WMI](securing-wmi-namespaces.md)
</dt> <dt>

Константы безопасности WMI
</dt> </dl>

 

