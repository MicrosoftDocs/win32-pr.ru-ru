---
title: Метод Ибаккграундкоперрор-Error (Deliveryoptimization. h)
description: Извлекает код ошибки и определяет контекст, в котором произошла ошибка.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Метод метода с ошибками
- Метод Ибаккграундкоперрор, интерфейс
- Интерфейс Ибаккграундкоперрор, метод method
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988564"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>Метод Ибаккграундкоперрор:: Error

Извлекает код ошибки и определяет контекст, в котором произошла ошибка.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекст* \[ заполняет\]
</dt> <dd>

Контекст, в котором произошла ошибка. Список значений контекста см. в разделе Перечисление [**BG_ERROR_CONTEXT**](bg-error-context.md) .

</dd> <dt>

*перроркоде* \[ заполняет\]
</dt> <dd>

Код ошибки произошедшей ошибки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **S_OK** при успешном или одном из стандартных значений HRESULT com при ошибке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError определен как 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкоперрор**](ibackgroundcopyerror.md)
</dt> <dt>

[**Ибаккграундкоперрор:: onfile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





