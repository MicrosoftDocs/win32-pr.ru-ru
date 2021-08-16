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
ms.openlocfilehash: d147bc877f9694617ec94651f53f4cf438c00de8d752710c3659f24ba4ffe21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810333"
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
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
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

 

 





