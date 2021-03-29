---
title: Функция Мфандлеклосе (Мпклиент. h)
description: Закрывает маркер, возвращенный Мпманажеропен, Мпсканстарт, Мпсреатопен или Мпупдатестарт.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Функции Мфандлеклосе устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535141"
---
# <a name="mphandleclose-function"></a>Функция Мфандлеклосе

Закрывает маркер, возвращенный [**мпманажеропен**](mpmanageropen.md), [**мпсканстарт**](mpscanstart.md), [**мпсреатопен**](mpthreatopen.md)или [**мпупдатестарт**](mpupdatestart.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмфандле* \[ окне\]
</dt> <dd>

Тип: **мфандле**

Закрываемый обработчик.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если функция выполнена успешно, возвращается значение **S \_**.

Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** . Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.

Функция может вернуть следующую конкретную ошибку:

| Код возврата             | Описание                      |
|-------------------------|----------------------------------|
| \_ \_ Недопустимый маркер "E Win" \_ | Указан недопустимый маркер. |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мперрормессажеформат**](mperrormessageformat.md)
</dt> <dt>

[**мпманажеропен**](mpmanageropen.md)
</dt> <dt>

[**мпсканстарт**](mpscanstart.md)
</dt> <dt>

[**мпсреатопен**](mpthreatopen.md)
</dt> </dl>

 

 





