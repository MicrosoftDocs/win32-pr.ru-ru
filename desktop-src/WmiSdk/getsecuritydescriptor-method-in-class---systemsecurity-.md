---
description: Возвращает дескриптор безопасности, управляющий доступом к пространству имен WMI, к которому вы подключены. Дескриптор безопасности возвращается в виде экземпляра \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Метод Жетсекуритидескриптор класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702665"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Метод Жетсекуритидескриптор \_ \_ класса системсекурити

Метод **жетсекуритидескриптор** получает дескриптор безопасности, который управляет доступом к пространству имен WMI, к которому вы подключены. Дескриптор безопасности возвращается в виде экземпляра [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дескриптор* \[ заполняет\]
</dt> <dd>

Дескриптор безопасности, связанный с пространством имен WMI.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку. Дополнительные сведения см. в статье [коды возврата WMI](wmi-return-codes.md) или [**вбемерроренум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**0**
</dt> <dd>

Успешное завершение.

</dd> <dt>

**2**
</dt> <dd>

У пользователя нет доступа к запрошенной информации.

</dd> <dt>

**8**
</dt> <dd>

Неизвестный сбой.

</dd> <dt>

**9**
</dt> <dd>

У пользователя нет необходимых прав для выполнения метода.

</dd> <dt>

**открыт**
</dt> <dd>

В вызове метода указан недопустимый параметр.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL). Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).

Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL. Дополнительные сведения см. в статьях [**константы прав**](privilege-constants.md) и [выполнение привилегированных операций](executing-privileged-operations.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_системсекурити**](--systemsecurity.md)
</dt> <dt>

[Настройка дескрипторов безопасности Намепаце](setting-namespace-security-descriptors.md)
</dt> </dl>

 

