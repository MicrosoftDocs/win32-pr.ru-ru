---
title: IMsRdpClientNonScriptable4 Алловкредентиалсавинг, свойство
description: Указывает, отображает ли диалоговое окно учетные данные флажок, позволяющий сохранить учетные данные.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Алловкредентиалсавинг
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681936"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a>Свойство IMsRdpClientNonScriptable4:: Алловкредентиалсавинг

Указывает, отображает ли диалоговое окно учетные данные флажок, позволяющий сохранить учетные данные.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a>Значение свойства

Указывает, отображает ли диалоговое окно учетные данные флажок, позволяющий сохранить учетные данные.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





