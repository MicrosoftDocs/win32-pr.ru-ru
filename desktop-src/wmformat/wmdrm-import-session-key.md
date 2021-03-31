---
title: Структура WMDRM_IMPORT_SESSION_KEY (Дрмекстерналс. h)
description: '\_ \_ Структура ключа сеанса импорта WMDRM \_ содержит ключ сеанса для импорта защищенного содержимого.'
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- Формат WMDRM_IMPORT_SESSION_KEY структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136982"
---
# <a name="wmdrm_import_session_key-structure"></a>\_ \_ Структура ключа сеанса импорта WMDRM \_

Структура **\_ \_ \_ ключа сеанса импорта WMDRM** содержит ключ сеанса для импорта защищенного содержимого.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкэйтипе**
</dt> <dd>

Тип ключа сеанса. Установите для параметра WMDRM \_ KEYTYPE \_ RC4.

</dd> <dt>

**cbKey**
</dt> <dd>

Размер ключа сеанса в байтах. Это значение может быть таким же, насколько вам необходимо, учитывая ограничения одной операции RSA OAEP для всего сообщения (Эта структура и ключ сеанса).

</dd> <dt>

**ргбкэй**
</dt> <dd>

Адрес буфера, содержащего ключ сеанса. Размер буфера должен совпадать со значением **cbKey**. Данные в буфере — это значение ключа, созданное случайным образом.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура, включая буфер, содержащий ключ сеанса, должна быть зашифрована с помощью открытого ключа компьютера Windows Media DRM и включена в элемент **пбенкриптедсессионкэймессаже** структуры [**\_ \_ \_ структуры импорта WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

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

 

 





