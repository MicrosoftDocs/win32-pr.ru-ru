---
title: IMsRdpClientNonScriptable4 Маркрдпсеттингссекуре, свойство
description: Указывает, помечены ли параметры протокол удаленного рабочего стола (RDP) как безопасные.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Маркрдпсеттингссекуре
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534451"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a>Свойство IMsRdpClientNonScriptable4:: Маркрдпсеттингссекуре

Указывает, помечены ли параметры [протокол удаленного рабочего стола](remote-desktop-protocol.md) (RDP) как безопасные. Это означает, что параметры, применяемые к элементу управления, были подписаны сторонним или доверенным издателем.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a>Значение свойства

Указывает, помечены ли параметры RDP как безопасные.

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

 

 





