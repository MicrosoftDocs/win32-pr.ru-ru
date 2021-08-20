---
description: Содержит сведения о цифровой подписи.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Структура SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3dc76db36cd752e22bbcd4d2f6672f7359dad882346b764fef0f4d12ef0901f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973398"
---
# <a name="signer_signature_info-structure"></a>\_ \_ Структура сведений о подписи подписывания

Структура **сведений о \_ подписи \_ подписывания** содержит сведения о цифровой подписи.

> [!Note]  
> Эта структура не определена ни в одном файле заголовка. Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер структуры в байтах.

</dd> <dt>

**алгидхаш**
</dt> <dd>

Хэш-алгоритм, используемый для цифровой подписи.

</dd> <dt>

**дваттрчоице**
</dt> <dd>

Указывает, содержит ли подпись атрибуты [*Authenticode*](../secgloss/a-gly.md) . Этот элемент может иметь одно или несколько следующих значений.



| Значение                                                                                                                                                                                                                                      | Значение                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <dt>**\_ Подписавший ДВУХФАКТОРНОЙ \_ attr**</dt> <dt>1</dt> </dl> | Сигнатура содержит атрибуты [*Authenticode*](../secgloss/a-gly.md) .<br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <dt>**\_ Подписавший НЕТ \_ attr**</dt> <dt>0</dt> </dl>                   | Подпись не имеет атрибутов [*Authenticode*](../secgloss/a-gly.md) .<br/> |



 

</dd> <dt>

**паттраускоде**
</dt> <dd>

Задает атрибуты для подписи [*Authenticode*](../secgloss/a-gly.md) . Этот элемент необходим, если значение элемента **дваттрчоице** — **подписывающий \_ двухфакторной \_ attr**.

</dd> <dt>

**псаусентикатед**
</dt> <dd>

Указанные пользователем атрибуты, добавленные в цифровую подпись.

</dd> <dt>

**псунаусентикатед**
</dt> <dd>

Пользовательские атрибуты, не прошедшие проверку подлинности, добавлены в цифровую подпись.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сигнерсигн**](signersign.md)
</dt> <dt>

[**сигнерсигнекс**](signersignex.md)
</dt> </dl>

 

 
