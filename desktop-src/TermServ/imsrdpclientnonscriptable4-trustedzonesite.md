---
title: IMsRdpClientNonScriptable4 Трустедзонесите, свойство
description: Указывает, находится ли веб-сайт, с которого пользователь запустил подключение, в списке надежных сайтов клиентского компьютера пользователя.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Трустедзонесите
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415768"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a>Свойство IMsRdpClientNonScriptable4:: Трустедзонесите

Указывает, находится ли веб-сайт, с которого пользователь запустил подключение, в списке надежных сайтов клиентского компьютера пользователя.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a>Значение свойства

Задает свойство Трустедзонесите. Этот метод не влияет на то, находится ли веб-сайт, с которого пользователь запустил подключение, в списке надежных сайтов клиентского компьютера.

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

 

 





