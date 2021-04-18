---
title: IMsRdpClientNonScriptable3 Варнабаутклипбоардредиректион, свойство
description: Указывает, следует ли отображать диалоговое окно "предупреждение системы безопасности", чтобы предупредить пользователей о перенаправлении буфера обмена.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Варнабаутклипбоардредиректион
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533932"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a>Свойство IMsRdpClientNonScriptable3:: Варнабаутклипбоардредиректион

Указывает, следует ли отображать диалоговое окно "предупреждение системы безопасности", чтобы предупредить пользователей о перенаправлении буфера обмена.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Значение свойства

Указывает, следует ли отображать диалоговое окно "предупреждение системы безопасности", чтобы предупредить пользователей о перенаправлении буфера обмена.

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

 

 





