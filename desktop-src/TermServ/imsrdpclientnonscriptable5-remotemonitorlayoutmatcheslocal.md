---
title: IMsRdpClientNonScriptable5 Ремотемониторлайаутматчеслокал, свойство
description: Указывает, идентичен ли макет удаленного монитора структуре локального монитора.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Ремотемониторлайаутматчеслокал
- Службы удаленных рабочих столов свойства Ремотемониторлайаутматчеслокал, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Ремотемониторлайаутматчеслокал
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136526"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a>Свойство IMsRdpClientNonScriptable5:: Ремотемониторлайаутматчеслокал

Указывает, идентичен ли макет удаленного монитора структуре локального монитора. Если это свойство содержит **вариант \_ true**, макет удаленного монитора идентичен макету локального монитора. Если это свойство содержит **вариант \_ false**, то удаленный и локальный мониторы имеют разные макеты.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a>Значение свойства

Получает значение свойства.

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

 

 





