---
title: IMsRdpClientNonScriptable3 Варнабаутсендингкредентиалс, свойство
description: Указывает или получает значение, указывающее, должно ли диалоговое окно "предупреждение системы безопасности" включать предупреждение об отправке учетных данных на удаленный сервер перед запуском сеанса.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Варнабаутсендингкредентиалс
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681832"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a>Свойство IMsRdpClientNonScriptable3:: Варнабаутсендингкредентиалс

Указывает или получает значение, указывающее, должно ли диалоговое окно "предупреждение системы безопасности" включать предупреждение об отправке учетных данных на удаленный сервер перед запуском сеанса.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Значение свойства

Указывает, должно ли диалоговое окно предупреждения системы безопасности включать предупреждение об отправке учетных данных на удаленный сервер перед запуском сеанса.

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

 

 





