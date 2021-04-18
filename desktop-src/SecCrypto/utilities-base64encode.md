---
description: Кодирует строку в кодировке Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Метод Utilities. Base64Encode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685377"
---
# <a name="utilitiesbase64encode-method"></a>Метод Utilities. Base64Encode

\[Метод **Base64Encode** доступен для использования в операционных системах, указанных в разделе требования.\]

Метод **Base64Encode** кодирует строку в кодировке Base64.

## <a name="syntax"></a>Синтаксис


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сркстринг* \[ окне\]
</dt> <dd>

Строка для кодирования в кодировке Base64.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Строка в кодировке Base64.

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

 

 




