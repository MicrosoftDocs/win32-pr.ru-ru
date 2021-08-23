---
title: IMsRdpClientAdvancedSettings5 Коннектионбаршовпинбуттон, свойство
description: Задает или получает конфигурацию кнопки закрепить на панели подключения.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Коннектионбаршовпинбуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Коннектионбаршовпинбуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Коннектионбаршовпинбуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Коннектионбаршовпинбуттон
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a978f6d1b6a26fe84f5ad590cfc41ab384d6ba49f1e265eecc0ea408b67b59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001392"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a>Свойство IMsRdpClientAdvancedSettings5:: Коннектионбаршовпинбуттон

Задает или получает конфигурацию кнопки закрепить на панели подключения.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a>Значение свойства

Логическое значение **true** или **false**. Значение **true** показывает, что кнопка закрепить на панели подключения. Значение **false** скрывает кнопку закрепить на панели подключения.

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

 

 





