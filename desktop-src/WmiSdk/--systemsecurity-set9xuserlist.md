---
description: задает права удаленного доступа для списка отдельных пользователей на компьютерах с устаревшими версиями Windows, где управление доступом через Windows дескрипторы безопасности недоступно.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: 'Метод __SystemSecurity:: Set9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: d1185fa91d9d12e240f592d458b975b650947cf5b8cd1b289a7e016b455556a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109965"
---
# <a name="__systemsecurityset9xuserlist-method"></a>\_\_Метод Системсекурити:: Set9XUserList

метод **\_ \_ системсекурити:: Set9XUserList** задает права удаленного доступа для списка отдельных пользователей на компьютерах с устаревшими версиями Windows, где управление доступом через Windows дескрипторы безопасности недоступно.

Список указывается в виде массива внедренных объектов, где каждый объект является экземпляром класса [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) . Эта функция аналогична дескриптору безопасности, но более ограничена. Группы не поддерживаются, и локальный доступ не контролируется, так как локальный пользователь всегда имеет полный доступ. Разрешены и Deny, и разрешить записи контроля доступа (ACE), и поэтому порядок ACE важен в списке управления доступом на уровне пользователей (DACL). Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*UL* \[ окне\]
</dt> <dd>

Массив пользователей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение HRESULT** , указывающее состояние вызова метода. В следующем списке перечислены возвращаемые значения, которые являются значимыми для **Set9XUserList**. для сценариев и Visual Basic приложений результат можно получить из [параметров out. ReturnValue](parsing-outparameters-objects.md). Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_метод WBEM \_ E \_ отключен**
</dt> <dd>

Этот метод не поддерживается.

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

[**\_\_SystemSecurity**](--systemsecurity.md)
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

 

