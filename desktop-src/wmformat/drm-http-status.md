---
title: Перечисление DRM_HTTP_STATUS (Дрмекстерналс. h)
description: '\_ \_ Тип перечисления состояния HTTP DRM определяет диапазон состояний для запроса DRM.'
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- Формат Windows Media DRM_HTTP_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e222cbf24e6333c7105e8564a5ad255693340749aeea32d98bd013bcb40995d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586304"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>Перечисление DRM_HTTP_STATUS (Дрмекстерналс. h)

Тип **перечисления \_ \_ состояния HTTP DRM** определяет диапазон состояний для запроса [*DRM*](wmformat-glossary.md) .

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

## <a name="remarks"></a>Remarks

Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](wm-individualize-status.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                      |
| Версия<br/>                  | Windows Пакет SDK для формата мультимедиа 7 или более поздние версии пакета SDK<br/>                       |
| Заголовок<br/>                   | <dl> <dt>Дрмекстерналс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_состояние ИНДИВИДУАЛИЗАЦИИ DRM \_**](drm-individualization-status.md)
</dt> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





