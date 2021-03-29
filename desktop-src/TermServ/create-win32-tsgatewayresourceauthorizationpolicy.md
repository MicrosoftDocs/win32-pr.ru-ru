---
title: Метод Create класса Win32_TSGatewayResourceAuthorizationPolicy
description: Создание удаленный рабочий стол политики авторизации ресурсов (RD \ 160; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Create
- Создание службы удаленных рабочих столов метода, Win32_TSGatewayResourceAuthorizationPolicy класса
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6372706a294902b03f22807049db9a954de4f7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414953"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Метод Create \_ класса Win32 тсгатевайресаурцеаусоризатионполици

Создание удаленный рабочий стол политики авторизации ресурсов (RD RAP).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
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

*ResourceGroupName* \[ окне\]
</dt> <dd>

Имя группы ресурсов.

</dd> <dt>

*Усерграупнамес* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список имен групп пользователей. Если пользователь принадлежит к любой из этих групп пользователей, доступ будет разрешен. Имена групп пользователей должны иметь формат *домена \\ усерграупнаме*.

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

 

