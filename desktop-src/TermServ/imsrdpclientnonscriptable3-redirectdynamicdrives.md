---
title: IMsRdpClientNonScriptable3 Редиректдинамикдривес, свойство
description: Указывает или получает значение, указывающее, доступны ли для перенаправления динамически подключаемые диски самонастраивающийся (PnP), перечисленные в сеансе.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Редиректдинамикдривес
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803886"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a>Свойство IMsRdpClientNonScriptable3:: Редиректдинамикдривес

Указывает или получает значение, указывающее, доступны ли для перенаправления динамически подключаемые диски самонастраивающийся (PnP), перечисленные в сеансе.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a>Значение свойства

Указывает, доступны ли для перенаправления динамически подключаемые диски PnP, перечисленные в сеансе.

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

 

 





