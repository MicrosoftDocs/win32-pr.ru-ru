---
title: Метод Ивмдрминдивидуализатионстатус-Status (Вмдрмсдк. h)
description: Метод WebMethod извлекает подробные сведения о ходе процесса индивидуализации.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Метод WebMethod формат Windows Media Format
- Метод WebMethod формат Windows Media Format, интерфейс Ивмдрминдивидуализатионстатус
- Интерфейс Ивмдрминдивидуализатионстатус интерфейса Windows Media Format, методического состояния
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704478"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a>Метод Ивмдрминдивидуализатионстатус:: with Status

Метод **WebMethod извлекает** подробные сведения о ходе процесса индивидуализации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстатус* \[ заполняет\]
</dt> <dd>

Получает структуру [**\_ \_ состояния WM индивидуализируйте**](drmwm-individualize-status.md) , содержащую подробные сведения о состоянии попытки индивидуализации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрминдивидуализатионстатус**](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





