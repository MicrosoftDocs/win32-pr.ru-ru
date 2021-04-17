---
title: Структура DRM_PLAYLIST_CONTENT_ID (Дрмекстерналс. h)
description: '\_ \_ Структура идентификатора содержимого списка воспроизведения DRM \_ содержит сведения о содержимом, которое должно быть скопировано на компакт-диск в процессе записи списка воспроизведения.'
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- Формат DRM_PLAYLIST_CONTENT_ID структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701066"
---
# <a name="drm_playlist_content_id-structure"></a>\_ \_ Структура идентификатора содержимого списка воспроизведения DRM \_

Структура **\_ \_ \_ идентификатора содержимого списка воспроизведения DRM** содержит сведения о содержимом, которое должно быть скопировано на компакт-диск в процессе записи списка воспроизведения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**lpcwszV2Header**
</dt> <dd>

Заголовок DRM. Используйте этот элемент, если содержимое защищено с помощью Windows Media DRM версии 2 или более поздней.

</dd> <dt>

**lpcszV1KID**
</dt> <dd>

идентификатор ключа; Используйте этот элемент, если содержимое защищено с помощью Windows Media DRM версии 1.

</dd> <dt>

**пбосердата**
</dt> <dd>

Буфер, содержащий дополнительные данные.

</dd> <dt>

**кбосердата**
</dt> <dd>

Размер буфера **пбосердата** в байтах.

</dd> <dt>

**двуникуеидфорсессион**
</dt> <dd>

Уникальный идентификатор содержимого, которое будет использоваться в текущем сеансе.

</dd> <dt>

**дввалидфиелдс**
</dt> <dd>

**DWORD** , указывающий допустимые поля этой структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                      |
| Версия<br/>                  | Пакет SDK для Windows Media Format 11<br/>                                                    |
| Header<br/>                   | <dl> <dt>Дрмекстерналс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





