---
title: Метод Update класса Win32_TSGatewayResourceAuthorizationPolicy
description: Обновление текущей удаленный рабочий стол политики авторизации ресурсов (RD \ 160; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода обновления
- Метод Update службы удаленных рабочих столов, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136299"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Метод Update \_ класса Win32 тсгатевайресаурцеаусоризатионполици

Обновляет текущую удаленный рабочий стол политики авторизации ресурсов (RD RAP).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* \[ окне\]
</dt> <dd>

Имя политики авторизации ресурсов удаленных рабочих столов.

</dd> <dt>

*Описание* \[ окне\]
</dt> <dd>

Описание политики авторизации ресурсов удаленных рабочих столов.

</dd> <dt>

*Включено* \[ окне\]
</dt> <dd>

Указывает, следует ли включить политику авторизации ресурсов удаленных рабочих столов.

</dd> <dt>

*ResourceGroupName* \[ окне\]
</dt> <dd>

Имя группы ресурсов, связанной с этим политик авторизации ресурсов удаленных рабочих столов.

</dd> <dt>

*Ресаурцеграуптипе* \[ окне\]
</dt> <dd>

Тип группы ресурсов.

<dt>

RG
</dt> <dd>

группа ресурсов;

</dd> <dt>

CG
</dt> <dd>

Группа компьютеров, сохраненная в домен Active Directory Services.

</dd> <dt>

КАЖДОГО
</dt> <dd>

Все ресурсы.

</dd> </dl> </dd> <dt>

*Усерграупнамес* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список имен групп пользователей. Имена имеют формат *домена \\ усерграупнаме*. Если пользователь принадлежит к любой из этих групп пользователей, доступ будет разрешен.

</dd> <dt>

*Протоколнамес* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список имен протоколов, включенных для этой политики. Имена должны соответствовать возвращаемому методу [**жетпротоколнаме**](getprotocolname-win32-tsgatewayserversettings.md) класса [**Win32 \_ тсгатевайсерверсеттингс**](win32-tsgatewayserversettings.md) .

</dd> <dt>

*Портнумберс* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список номеров портов, включенных для этой политики. Чтобы разрешить любой номер порта, установите " \* ".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

