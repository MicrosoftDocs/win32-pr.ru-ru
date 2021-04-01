---
description: Преобразует указанные данные атрибута в формат XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: Функция Сдбформататтрибуте
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895253"
---
# <a name="sdbformatattribute-function"></a>Функция Сдбформататтрибуте

Преобразует указанные данные атрибута в формат XML.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паттринфо* \[ окне\]
</dt> <dd>

Структура [**аттринфо**](attrinfo.md) .

</dd> <dt>

*пчбуффер* \[ заполняет\]
</dt> <dd>

Выходной буфер.

</dd> <dt>

*двбуфферсизе* \[ окне\]
</dt> <dd>

Размер буфера *пчбуффер* в символах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **значение true** при успешном выполнении или **значение false** , если буфер слишком мал или не найден атрибут.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбжетфилеаттрибутес**](sdbgetfileattributes.md)
</dt> </dl>

 

 




