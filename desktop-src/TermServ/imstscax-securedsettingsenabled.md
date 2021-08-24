---
title: Имстскакс Секуредсеттингсенаблед, свойство
description: Указывает, доступен ли интерфейс Имстсксекуредсеттингс. То есть, находится ли веб-страница, содержащая данный элемент управления, в одной из разрешенных зон безопасности URL-адресов Internet Explorer.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Секуредсеттингсенаблед
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc03fb9cff3a99d77006989b7adade40a15ad4bb4d63e6f940092b765b1e250f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771064"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a>Свойство Имстскакс:: Секуредсеттингсенаблед

Указывает, доступен ли интерфейс [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) . То есть, находится ли веб-страница, содержащая данный элемент управления, в одной из разрешенных зон безопасности URL-адресов Internet Explorer.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Значение свойства

Значение этого параметра равно **true** , если интерфейс доступен, и **false** в противном случае.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Используйте этот метод, чтобы запросить доступ к интерфейсу [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) перед получением свойства [**секуредсеттингс**](imstscax-securedsettings.md) .

Список зон безопасности с ограниченным URL-адресом см. в руководстве по обеспечению [безопасности клиента RDP](providing-for-rdp-client-security.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпклиент**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**имстскакс**](imstscax-interface.md)
</dt> <dt>

[**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





