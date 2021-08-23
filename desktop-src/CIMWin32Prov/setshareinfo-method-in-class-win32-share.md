---
description: Сетшареинфо&\# 8194; Метод класса WMI задает параметры общего ресурса.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Метод Сетшареинфо класса Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9ee76a0b8336ccdca90a04ee3c2a223b7269a30a00276418d6c46a8bb3abc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800904"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Метод Сетшареинфо \_ класса общего ресурса Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) сетшареинфо задает параметры общего ресурса.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*MaximumAllowed* \[ в необязательное\]
</dt> <dd>

Максимальное число пользователей, которым разрешено использовать этот ресурс одновременно.

Пример: 10. Это необязательный параметр.

</dd> <dt>

*Описание* \[ в необязательное\]
</dt> <dd>

Необязательный комментарий для описания ресурса, к которому предоставляется общий доступ.

</dd> <dt>

*Доступ к* \[ в необязательное\]
</dt> <dd>

Дескриптор безопасности для разрешений уровня пользователя. Дескриптор безопасности содержит сведения о разрешениях, владельце и доступе ресурса. Дополнительные сведения см. в разделе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Отказано в доступе** (2)
</dt> <dt>

**Неизвестный сбой** (8)
</dt> <dt>

**Недопустимое имя** (9)
</dt> <dt>

**Недопустимый уровень** (10)
</dt> <dt>

**Недопустимый параметр** (21)
</dt> <dt>

**Повторяющаяся общая папка** (22)
</dt> <dt>

**Путь перенаправления** (23)
</dt> <dt>

**Неизвестное устройство или каталог** (24)
</dt> <dt>

**Не найдено сетевое имя** (25)
</dt> <dt>

**Другие** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarks

Метод **сетшареинфо** является динамическим методом объекта и используется для вхождения этого класса.

Только члены локальной группы "Администраторы" или "Операторы учетных записей" или пользователи с членством в группе операторов связи, печати или сервера могут успешно выполнять **сетшареинфо**. Оператор Print может устанавливать только очереди принтера. Оператор связи может устанавливать только очереди устройств связи.

## <a name="examples"></a>Примеры

Следующий пример PowerShell обновляет имя общей папки **невшаре** .


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



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

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Общий ресурс Win32**](win32-share.md)
</dt> </dl>

 

