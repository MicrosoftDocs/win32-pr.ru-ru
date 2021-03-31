---
title: IMsRdpClientNonScriptable3 Редиректдинамикдевицес, свойство
description: Указывает или получает значение, указывающее, доступны ли для перенаправления динамически подключаемые устройства самонастраивающийся (PnP), перечисленные в сеансе.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Редиректдинамикдевицес
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801450"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a>Свойство IMsRdpClientNonScriptable3:: Редиректдинамикдевицес

Указывает или получает значение, указывающее, доступны ли для перенаправления динамически подключаемые устройства самонастраивающийся (PnP), перечисленные в сеансе.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a>Значение свойства

Указывает, доступны ли для перенаправления динамически подключаемые устройства PnP, перечисленные в сеансе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





