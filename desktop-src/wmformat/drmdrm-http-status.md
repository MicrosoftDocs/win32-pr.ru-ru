---
title: Перечисление DRM_HTTP_STATUS (Вмдрмсдк. h)
description: '\_ \_ Тип перечисления состояния HTTP DRM определяет диапазон состояний HTTP для запроса DRM.'
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- Формат Windows Media DRM_HTTP_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708494"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>Перечисление DRM_HTTP_STATUS (Вмдрмсдк. h)

Тип **перечисления \_ \_ состояния HTTP DRM** определяет диапазон состояний HTTP для запроса DRM.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_НОТИНИТИАТЕД HTTP**
</dt> <dd>

Операции HTTP не инициированы.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_подключение HTTP**
</dt> <dd>

Устанавливается соединение.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP- \_ запрос**
</dt> <dd>

Выполняется запрос данных.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_Получение HTTP**
</dt> <dd>

Данные получаются.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ завершено**
</dt> <dd>

Операции HTTP завершены.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](drmwm-individualize-status.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](drm-enumeration-types.md)
</dt> </dl>

 

 





