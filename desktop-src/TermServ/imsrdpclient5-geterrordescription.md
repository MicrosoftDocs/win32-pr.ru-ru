---
title: IMsRdpClient5 Жетеррордескриптион, метод
description: Возвращает описание ошибки для событий отключения сеанса.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Жетеррордескриптион
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416049"
---
# <a name="imsrdpclient5geterrordescription-method"></a>Метод IMsRdpClient5:: Жетеррордескриптион

Возвращает описание ошибки для событий отключения сеанса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*дисконнектреасон* \[ окне\]
</dt> <dd>

Причина отключения.

</dd> <dt>

*екстендеддисконнектреасон* \[ окне\]
</dt> <dd>

Содержит подробные сведения о том, почему было инициировано отключение.

</dd> <dt>

*пбстреррормсг* \[ заполняет\]
</dt> <dd>

Указатель на переменную **BSTR** , которая получает текст сообщения об ошибке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient5 определен как 4eb5335b-6429-477d-B922-e06a28ecd8bf<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





