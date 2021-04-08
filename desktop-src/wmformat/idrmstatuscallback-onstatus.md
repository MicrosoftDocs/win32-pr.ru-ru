---
title: Идрмстатускаллбакк OnStatus, метод
description: Метод OnStatus получает сообщения о состоянии от асинхронных процессов DRM.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Метод OnStatus формат Windows Media
- Метод OnStatus формат Windows Media Format, интерфейс Идрмстатускаллбакк
- Интерфейс Идрмстатускаллбакк Windows Media Format, метод OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068860"
---
# <a name="idrmstatuscallbackonstatus-method"></a>Метод Идрмстатускаллбакк:: OnStatus

Метод **OnStatus** получает сообщения о состоянии от асинхронных процессов DRM.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Состояние* \[ окне\]
</dt> <dd>

Код состояния. Коды сообщений определяются в типе **перечисления \_ состояния Msdrm** .

</dd> <dt>

*HR* \[ окне\]
</dt> <dd>

Код возврата, который поддерживает сообщение о состоянии.

</dd> <dt>

*двтипе* \[ окне\]
</dt> <dd>

Тип данных, на который указывает *pValue*. Задайте одно из значений перечисления [**\_ \_ DATATYPE attr DRM**](drm-attr-datatype.md) .

</dd> <dt>

*pValue* \[ окне\]
</dt> <dd>

Указатель на данные, связанные с сообщением о состоянии. Тип данных определяется значением параметра *двтипе* . Дополнительные сведения см. в описании перечисления [**\_ \_ DATATYPE attr DRM**](drm-attr-datatype.md) .

</dd> <dt>

*пвконтекст* \[ окне\]
</dt> <dd>

Необязательный параметр, который можно использовать для обнаружения объекта, отправившего сообщение. Установив *пвконтекст* при регистрации этого обратного вызова, можно использовать один и тот же обратный вызов для обработки нескольких асинхронных процессов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип данных attr с атрибутом DRM \_**](drm-attr-datatype.md)
</dt> <dt>

[**Интерфейс Идрмстатускаллбакк**](idrmstatuscallback.md)
</dt> </dl>

 

 





