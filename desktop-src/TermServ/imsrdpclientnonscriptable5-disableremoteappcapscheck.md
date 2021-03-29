---
title: IMsRdpClientNonScriptable5 Дисаблеремотеаппкапсчекк, свойство
description: Указывает, должен ли элемент управления ActiveX удаленный рабочий стол не проверять наличие у сервера возможностей RemoteApp.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисаблеремотеаппкапсчекк
- Службы удаленных рабочих столов свойства Дисаблеремотеаппкапсчекк, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Дисаблеремотеаппкапсчекк
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493179"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a>IMsRdpClientNonScriptable5: свойство Исаблеремотеаппкапсчекк:D

Указывает, должен ли элемент управления ActiveX удаленный рабочий стол не проверять наличие у сервера возможностей RemoteApp. Если это свойство содержит **вариант \_ true**, элемент управления не должен проверять сервер на наличие возможностей RemoteApp. Если это свойство содержит **\_ значение Variant false**, элемент управления может проверить наличие возможностей удаленного приложения RemoteApp на сервере.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a>Значение свойства

Указывает новое значение свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                             |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





