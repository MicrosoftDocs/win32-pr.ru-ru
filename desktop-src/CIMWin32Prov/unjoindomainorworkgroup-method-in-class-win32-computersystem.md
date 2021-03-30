---
description: Удаляет компьютерную систему из домена или рабочей группы.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Метод Унжоиндомаинорворкграуп класса Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896369"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Метод Унжоиндомаинорворкграуп \_ класса ComputerSystem Win32

Метод **унжоиндомаинорворкграуп** удаляет компьютерную систему из домена или рабочей группы.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пароль* \[ окне\]
</dt> <dd>

Если параметр *username* указывает имя учетной записи, параметр *Password* должен указывать на пароль, используемый при подключении к контроллеру домена. В противном случае этот параметр должен иметь **значение NULL**.

> [!Note]  
> При подключении к WINMGMT или [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) по указателю [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) *пароль* должен использовать высокий уровень проверки подлинности, а не менее **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C**. Если локальная для WinMgmt, это не проблема.

 

</dd> <dt>

*Имя пользователя* \[ окне\]
</dt> <dd>

Указатель на постоянную строку символов, завершающуюся нулем, которая указывает имя учетной записи, используемой при подключении к контроллеру домена. Необходимо указать домен и учетную запись пользователя, например "пользователь домена \\ " или " user@domain ". Если этот параметр имеет **значение NULL**, используется контекст вызывающего объекта.

> [!Note]  
> При подключении к WINMGMT или [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) по указателю [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) *имя пользователя* должно использовать высокий уровень проверки подлинности, а не меньше, чем **RPC \_ C \_ AUTHN \_ уровня \_ \_ безопасности PKT**. Если локальная для WinMgmt, это не проблема.

 

</dd> <dt>

*Фунжоиноптионс* \[ окне\]
</dt> <dd>

Набор битовых флагов, определяющих параметры отсоединений.

<dt>



  (0)


</dt> <dd>

По умолчанию. Без параметров.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**Нетсетуп \_ \_Удаление acct** (4)


</dt> <dd>

Отключите учетную запись Active Directory после операции отмены объединения, но не удаляйте учетную запись.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод **унжоиндомаинорворкграуп** возвращает 0 (нуль) при успешном выполнении или при отсутствии параметров. Любое другое значение указывает на ошибку. Коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Другие** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Комментарии

После вызова этого метода перезагрузите затронутый компьютер, чтобы применить изменения.

## <a name="examples"></a>Примеры

[Отсоединение компьютера от домена](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) Пример сценария VBScript отсоединяет локальный компьютер от текущего домена и отключает учетную запись компьютера.

При [отсоединении компьютера из домена с помощью примера сценария VBS](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) указанный компьютер из домена не присоединяется к указанному компьютеру. .

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

[**Win32 \_ ComputerSystem**](win32-computersystem.md)
</dt> <dt>

[**Метод Жоиндомаинорворкграуп**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

