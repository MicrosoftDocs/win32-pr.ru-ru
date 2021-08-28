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
ms.openlocfilehash: 44303a568a9f7775893033edc512e8a916004c43207277e308e1d4826d9f9537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161563"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбжетфилеаттрибутес**](sdbgetfileattributes.md)
</dt> </dl>

 

 




