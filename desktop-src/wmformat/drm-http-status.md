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
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672771"
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

## <a name="remarks"></a>Комментарии

Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](wm-individualize-status.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                      |
| Версия<br/>                  | Пакет SDK для Windows Media Format 7 или более поздние версии пакета SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Дрмекстерналс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_состояние ИНДИВИДУАЛИЗАЦИИ DRM \_**](drm-individualization-status.md)
</dt> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





