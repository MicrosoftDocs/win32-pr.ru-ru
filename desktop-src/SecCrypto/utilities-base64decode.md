---
description: Декодирует строку из Base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Метод Utilities. Base64Decode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688813"
---
# <a name="utilitiesbase64decode-method"></a>Метод Utilities. Base64Decode

\[Метод **Base64Decode** доступен для использования в операционных системах, указанных в разделе требования.\]

Метод **Base64Decode** декодирует строку из Base64.

## <a name="syntax"></a>Синтаксис


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Енкодедстринг* \[ окне\]
</dt> <dd>

Строка в кодировке Base64 для декодирования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Декодированная строка.

## <a name="remarks"></a>Комментарии

Кодировка base64 — это схема, используемая для передачи двоичных данных. Base64 обрабатывает данные в виде 24-разрядных групп, сопоставляя эти данные с четырьмя закодированными символами. Кодировка base64 иногда называется кодировкой 3 – 4. Каждый 6 бит 24-разрядной группы используется в качестве индекса в таблице сопоставления (в кодировке Base64) для получения символа для закодированных данных. Закодированные данные имеют длину строк, которая ограничена 76 символами.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Служебные программы**](utilities.md)
</dt> </dl>

 

 




