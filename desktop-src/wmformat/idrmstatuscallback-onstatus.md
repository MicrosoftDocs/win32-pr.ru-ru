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
ms.openlocfilehash: 2c9f8c0424752ababe684b426d78001f2783d62db9781fe3d6a23ed002e91773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847458"
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



 

## <a name="remarks"></a>Remarks

Нет.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип данных attr с атрибутом DRM \_**](drm-attr-datatype.md)
</dt> <dt>

[**Интерфейс Идрмстатускаллбакк**](idrmstatuscallback.md)
</dt> </dl>

 

 





