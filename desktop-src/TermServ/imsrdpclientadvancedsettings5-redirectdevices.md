---
title: IMsRdpClientAdvancedSettings5 Редиректдевицес, свойство
description: Задает или получает конфигурацию для перенаправления устройства.
ms.assetid: bf989ca0-5c79-4a73-a32b-51ef97ca0dff
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректдевицес
- Службы удаленных рабочих столов свойства Редиректдевицес, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректдевицес
- Службы удаленных рабочих столов свойства Редиректдевицес, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректдевицес
- Службы удаленных рабочих столов свойства Редиректдевицес, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректдевицес
- Службы удаленных рабочих столов свойства Редиректдевицес, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректдевицес
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectDevices
- IMsRdpClientAdvancedSettings5.get_RedirectDevices
- IMsRdpClientAdvancedSettings5.put_RedirectDevices
- IMsRdpClientAdvancedSettings6.RedirectDevices
- IMsRdpClientAdvancedSettings6.get_RedirectDevices
- IMsRdpClientAdvancedSettings6.put_RedirectDevices
- IMsRdpClientAdvancedSettings7.RedirectDevices
- IMsRdpClientAdvancedSettings7.get_RedirectDevices
- IMsRdpClientAdvancedSettings7.put_RedirectDevices
- IMsRdpClientAdvancedSettings8.RedirectDevices
- IMsRdpClientAdvancedSettings8.get_RedirectDevices
- IMsRdpClientAdvancedSettings8.put_RedirectDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6e72c5441b7eaa79b7bfeceb4e910b09041b72fb90dc58a54abda73baf9109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118855332"
---
# <a name="imsrdpclientadvancedsettings5redirectdevices-property"></a>Свойство IMsRdpClientAdvancedSettings5:: Редиректдевицес

Задает или получает конфигурацию для перенаправления устройства.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RedirectDevices(
  [in]  VARIANT_BOOL fRedirectPnPDevices
);

HRESULT get_RedirectDevices(
  [out] VARIANT_BOOL *pfRedirectPnPDevices
);
```



## <a name="property-value"></a>Значение свойства

Задает для режима перенаправления устройства **значение true** или **false**. Если задано **значение true**, режим перенаправления устройств включен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





