---
title: Имстскакс Адванцедсеттингс, свойство
description: Извлекает указатель интерфейса Имстскадванцедсеттингс.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Адванцедсеттингс
- Службы удаленных рабочих столов свойства Адванцедсеттингс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Адванцедсеттингс
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988647"
---
# <a name="imstscaxadvancedsettings-property"></a>Свойство Имстскакс:: Адванцедсеттингс

Извлекает указатель интерфейса [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a>Значение свойства

Указатель интерфейса [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>См. также раздел

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
</dt> </dl>

 

 





