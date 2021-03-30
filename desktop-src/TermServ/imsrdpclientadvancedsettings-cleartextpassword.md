---
title: Имсрдпклиентадванцедсеттингс Клеартекстпассворд, свойство
description: Указывает пароль для подключения. Дополнительные сведения см. в описании интерфейса Имстскнонскриптабле.
ms.assetid: 9bb12dd6-f74c-488d-b6e5-4f96346610a1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Клеартекстпассворд
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ClearTextPassword
- IMsRdpClientAdvancedSettings.put_ClearTextPassword
- IMsRdpClientAdvancedSettings2.ClearTextPassword
- IMsRdpClientAdvancedSettings2.put_ClearTextPassword
- IMsRdpClientAdvancedSettings3.ClearTextPassword
- IMsRdpClientAdvancedSettings3.put_ClearTextPassword
- IMsRdpClientAdvancedSettings4.ClearTextPassword
- IMsRdpClientAdvancedSettings4.put_ClearTextPassword
- IMsRdpClientAdvancedSettings5.ClearTextPassword
- IMsRdpClientAdvancedSettings5.put_ClearTextPassword
- IMsRdpClientAdvancedSettings6.ClearTextPassword
- IMsRdpClientAdvancedSettings6.put_ClearTextPassword
- IMsRdpClientAdvancedSettings7.ClearTextPassword
- IMsRdpClientAdvancedSettings7.put_ClearTextPassword
- IMsRdpClientAdvancedSettings8.ClearTextPassword
- IMsRdpClientAdvancedSettings8.put_ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6943913193b2ecc9ed6ab31728d0274fb9ddd231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490353"
---
# <a name="imsrdpclientadvancedsettingscleartextpassword-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Клеартекстпассворд

Указывает пароль для подключения. Дополнительные сведения см. в описании интерфейса [**имстскнонскриптабле**](imstscnonscriptable-interface.md) .

> [!Caution]  
> Несмотря на то, что доступ к паролям с использованием обычного текста можно получить с помощью этого свойства, разработчик по-прежнему обязан соблюдать осторожность и обеспечивать безопасность при передаче паролей в свои приложения.

 

Это свойство доступно только на запись.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR clearTextPassword
);
```



## <a name="property-value"></a>Значение свойства

Новый пароль.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                        |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                  |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





