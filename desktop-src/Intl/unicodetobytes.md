---
UID: ''
title: Функция Уникодетобитес
description: Преобразует символы Юникода в кодировку GB18030 байт.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 01109763644dc04aeb398e5fc64e221cd5f3d18870df2654fa5348bc163a277c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764737"
---
# <a name="unicodetobytes-function"></a>Функция Уникодетобитес

## <a name="description"></a>Описание

Не рекомендуется. Преобразует символы Юникода в кодировку GB18030 байт.

**Примечание** .  при преобразовании символов юникода в кодировку GB18030 байты приложение, запускаемое в Windows Vista и более поздних версий, должно использовать функцию [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a>Параметры

### <a name="lpwidecharstr-in"></a>Лпвидечарстр [in]

Указатель на строку в Юникоде для преобразования.

### <a name="cchwidechar-in"></a>Кчвидечар [in]

Число символов в строке Юникода для преобразования.

### <a name="lpmultibytestr-in"></a>Лпмултибитестр [in]

Указатель на целевой многобайтовый буфер.
Если *лпмултибитестр* имеет значение 0, возвращается число байтов в результатах GB18030 и преобразование не выполняется.

### <a name="cchmultibyte-in"></a>Кчмултибите [in]

Число байтов целевого многобайтового буфера.
Если *кчмултибите* имеет значение 0, возвращается число байтов в результатах GB18030 и преобразование не выполняется.

## <a name="returns"></a>Возвращаемое значение

Возвращает количество байтов многобайтовых символов, создаваемых в случае успеха.

## <a name="remarks"></a>Remarks

## <a name="see-also"></a>См. также раздел

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
