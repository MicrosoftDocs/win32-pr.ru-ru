---
description: Возвращает дескриптор безопасности, определяющий, кому разрешено запускать DCOM-приложение.
ms.assetid: ba02807f-aa2a-4b1c-9692-2803d93cd2ee
ms.tgt_platform: multiple
title: Метод Жетлаунчсекуритидескриптор класса Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b76a37db5b1edbc230c4cc4aed712ef4eee9dd4221cc4cb85fb8f205db69d35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878954"
---
# <a name="getlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Метод Жетлаунчсекуритидескриптор \_ класса Win32 дкомаппликатионсеттинг

Метод WMI **жетлаунчсекуритидескриптор** получает дескриптор безопасности, который определяет, кому разрешено запускать DCOM-приложение. Дескриптор безопасности является экземпляром класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Учетная запись, выполняющая скрипт или приложение, вызывающее этот метод, должна иметь права **SeSecurityPrivilege** и **сересторепривилеже** . Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetLaunchSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дескриптор* \[ заполняет\]
</dt> <dd>

Дескриптор безопасности, определяющий, кто может запускать приложение DCOM.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку. Дополнительные сведения см. в статье [коды возврата WMI](/windows/desktop/WmiSdk/wmi-return-codes) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Успешно**
</dt> <dd>

0

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

</dd> <dt>

**Другое**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Remarks

Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL). Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).

Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL. Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Дкомаппликатионсеттинг Win32**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Изменение параметров безопасности доступа для защищаемых объектов](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

