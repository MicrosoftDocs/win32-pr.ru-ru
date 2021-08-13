---
title: Метод IMsRdpClient7 Жетстатустекст (OpenService. h)
description: Получает текст состояния для указанного кода состояния.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстатустекст
- Службы удаленных рабочих столов метода Жетстатустекст, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Жетстатустекст
- Службы удаленных рабочих столов метода Жетстатустекст, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Жетстатустекст
- Службы удаленных рабочих столов метода Жетстатустекст, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Жетстатустекст
- Службы удаленных рабочих столов метода Жетстатустекст, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Жетстатустекст
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ecccb6535afec2d32ff0466428af36c432bc981a1bc23cfa24161ca969a80e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119285194"
---
# <a name="imsrdpclient7getstatustext-method"></a>Метод IMsRdpClient7:: Жетстатустекст

Получает текст состояния для указанного кода состояния.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*StatusCode* \[ окне\]
</dt> <dd>

Значение **uint** , указывающее код состояния, для которого извлекается текст.

</dd> <dt>

*пбстрстатустекст* \[ out, retval\]
</dt> <dd>

Адрес объекта **BSTR** , который получает текст состояния.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                     |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Header<br/>                   | <dl> <dt>OpenService. h</dt> </dl> |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpClient7 определен как b2a5b5ce-3461-444a-91d4-add26d070638<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





