---
description: Получает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: 'Метод __SystemSecurity:: Get9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656665"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_Метод Системсекурити:: Get9XUserList

Метод [**\_ \_ системсекурити:: Set9XUserList**](--systemsecurity-set9xuserlist.md) получает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.

Эта функция аналогична дескриптору безопасности, но более ограничена. Группы не поддерживаются, и локальный доступ не контролируется, так как локальный пользователь всегда имеет полный доступ. Разрешены и Deny, и разрешить записи контроля доступа (ACE), и поэтому порядок ACE важен в списке управления доступом на уровне пользователей (DACL). Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*UL* \[ заполняет\]
</dt> <dd>

Массив пользователей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение HRESULT** , указывающее состояние вызова метода. В следующем списке перечислены возвращаемые значения, которые являются значимыми для **Get9XUserList**. Для сценариев и Visual Basic приложений результат может быть [параметром Parameters. returnValue](parsing-outparameters-objects.md). Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

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

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Защита пространств имен WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Константы безопасности WMI](wmi-security-constants.md)
</dt> </dl>

 

