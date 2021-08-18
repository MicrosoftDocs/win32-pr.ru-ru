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
ms.openlocfilehash: d34cdff6d17ad6ce60dd40478b56c9718be0863295422d2e5c60fee2c437dc6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844063"
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

## <a name="remarks"></a>Remarks

эта структура, в том числе буфер, содержащий ключ сеанса, должна быть зашифрована с помощью Windows открытого ключа компьютера DRM Media и включена в элемент **пбенкриптедсессионкэймессаже** структуры [**\_ \_ \_ структуры импорта WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                      |
| Версия<br/>                  | Windows Пакет SDK для формата мультимедиа 11<br/>                                                    |
| Header<br/>                   | <dl> <dt>Дрмекстерналс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





