---
description: Записывает обновленную версию дескриптора безопасности, которая управляет доступом к пространству имен WMI, к которому вы подключены. Дескриптор безопасности представлен экземпляром \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Метод Сетсекуритидескриптор класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702559"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Метод Сетсекуритидескриптор \_ \_ класса системсекурити

Метод [**сетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) записывает обновленную версию дескриптора безопасности, которая управляет доступом к пространству имен WMI, к которому вы подключены. Дескриптор безопасности представлен экземпляром [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дескриптор* \[ окне\]
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

Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/a-gly) (SACL). Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).

Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL. Дополнительные сведения см. в статьях [**константы прав**](privilege-constants.md) и [выполнение привилегированных операций](executing-privileged-operations.md).

При вызове этого метода можно обновить списки DACL и SACL в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , но вы также можете обновить только список DACL или только список SACL.

Следующие значения в [**\_ \_ элементе управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) определяют, обновляются ли списки DACL или SACL или оба этих элемента.

-   **\_присутствие DACL \_ SE**

    Указывает, что список DACL должен быть обновлен. Если значение не задано, Инструментарий WMI сохраняет исходное значение DACL.

-   **\_имеется список SACL для SE \_**

    Указывает, что список SACL должен быть обновлен. Если значение не задано, Инструментарий WMI сохраняет исходное значение списка SACL. Для обновления списка SACL учетная запись должна иметь права **SeSecurityPrivilege** . Для сценариев имя привилегии — **SeSecurityPrivilege**. Дополнительные сведения см. в разделе [**константы прав доступа**](privilege-constants.md).

Если доверенное лицо группы и свойства доверенного лица владельца не равны **null**, они обновляются. В противном случае Инструментарий WMI сохраняет исходные значения. Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md).

Если в вызове этого метода новый список SACL имеет **значение NULL** , то список SACL дескриптора безопасности на целевом защищаемом объекте остается без изменений.

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

 

