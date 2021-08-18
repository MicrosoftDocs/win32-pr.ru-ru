---
description: Обновляет дескриптор безопасности доступа DCOM-приложения с новым дескриптором безопасности, который определяется экземпляром \_ класса SecurityDescriptor Win32.
ms.assetid: 71b708ba-5eb7-400e-bee2-37ca93966c3f
ms.tgt_platform: multiple
title: Метод Сетакцесссекуритидескриптор класса Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab668b12d6f08e205c770f4c717eda6f996971897fedb48e70702fc2d80a3c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752694"
---
# <a name="setaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Метод Сетакцесссекуритидескриптор \_ класса Win32 дкомаппликатионсеттинг

Метод **сетакцесссекуритидескриптор** обновляет дескриптор безопасности доступа DCOM-приложения с новым дескриптором безопасности, который определяется экземпляром класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Этот дескриптор безопасности управляет доступом к приложению. Учетная запись, выполняющая скрипт или приложение, вызывающее этот метод, должна иметь права **SeSecurityPrivilege** и **сересторепривилеже** . Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetAccessSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дескриптор* \[ окне\]
</dt> <dd>

Дескриптор безопасности, заданный для DCOM приложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку. Дополнительные сведения см. в статье [коды возврата WMI](/windows/desktop/WmiSdk/wmi-return-codes) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Успешно**
</dt> <dd>

0

Успешное завершение

</dd> <dt>

**2**
</dt> <dd>

У пользователя нет доступа к запрошенной информации

</dd> <dt>

**8**
</dt> <dd>

Неизвестный сбой

</dd> <dt>

**9**
</dt> <dd>

У пользователя нет необходимых прав для выполнения метода

</dd> <dt>

**открыт**
</dt> <dd>

Параметр, указанный в вызове метода, является недопустимым

</dd> <dt>

**Другое**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Remarks

Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL). Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).

Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL. Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).

При вызове этого метода можно обновить списки DACL и SACL в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , но вы также можете обновить только список DACL или только список SACL.

Следующие значения в [**\_ \_ элементе управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) определяют, обновляются ли списки DACL, SACL или и то, и другое.

-   **SE \_ \_имеется DACL**

    Указывает, что список DACL должен быть обновлен. Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение DACL.

-   **SE \_ Список SACL \_ имеется**

    Указывает, что список SACL должен быть обновлен. Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение списка SACL. Для обновления списка SACL учетная запись должна иметь права **SeSecurityPrivilege** . Для сценариев имя привилегии — **SeSecurityPrivilege**. Дополнительные сведения см. в разделе [**константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants).

Если доверенное лицо группы и свойства доверенного лица владельца не равны **null**, они обновляются. В противном случае Инструментарий WMI сохраняет исходные значения. Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).

Если при вызове этого метода новый список SACL имеет **значение NULL** , то список SACL дескриптора безопасности на целевом защищаемом объекте остается без изменений.

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

[**\_Дкомаппликатионсеттинг Win32**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Изменение параметров безопасности доступа для защищаемых объектов](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

