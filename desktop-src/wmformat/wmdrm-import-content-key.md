---
title: Структура WMDRM_IMPORT_CONTENT_KEY (Дрмекстерналс. h)
description: '\_ \_ Структура ключа содержимого для импорта WMDRM \_ хранит ключ содержимого, используемый при импорте защищенного содержимого.'
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- Формат WMDRM_IMPORT_CONTENT_KEY структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414865"
---
# <a name="wmdrm_import_content_key-structure"></a>\_ \_ Структура ключа содержимого для импорта WMDRM \_

Структура **\_ \_ \_ ключа содержимого для импорта WMDRM** хранит ключ содержимого, используемый при импорте защищенного содержимого.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Версия.

</dd> <dt>

**кбструктсизе**
</dt> <dd>

Размер структуры в байтах.

</dd> <dt>

**двивкэйтипе**
</dt> <dd>

Тип ключа вектора инициализации. Установите для параметра WMDRM \_ KEYTYPE \_ RC4.

</dd> <dt>

**кбивкэй**
</dt> <dd>

Размер ключа вектора инициализации в байтах.

</dd> <dt>

**двконтенткэйтипе**
</dt> <dd>

Тип ключа содержимого. Задайте значение WMDRM \_ KEYTYPE \_ коктейль.

</dd> <dt>

**кбконтенткэй**
</dt> <dd>

Размер ключа содержимого в байтах.

</dd> <dt>

**ргбкэйдата**
</dt> <dd>

Адрес буфера, содержащего ключ содержимого. Размер буфера должен совпадать со значением **кбконтенткэй**. Этот ключ должен соответствовать ключу, импортированному из сообщения лицензии КСМР.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура, включая буфер, содержащий ключ сеанса, должна быть зашифрована с помощью ключа сеанса и включена в элемент **пбенкриптедкэймессаже** структуры [**\_ \_ \_ структуры импорта WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

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

 

 





