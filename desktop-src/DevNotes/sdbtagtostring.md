---
description: Извлекает отображаемое имя указанного ТЕГА.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: Функция Сдбтагтостринг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 22ddb526e332b335e88ecc7aaa770615220f6b0dde838386093e2813fe964e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044844"
---
# <a name="sdbtagtostring-function"></a>Функция Сдбтагтостринг

Извлекает отображаемое имя указанного ТЕГА.

## <a name="syntax"></a>Синтаксис


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тег* \[ окне\]
</dt> <dd>

ТЕГ.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает указатель на строку, завершающуюся нулем, или "Инвалидтаг".

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ТЕГАМИ**](tag.md)
</dt> </dl>

 

 




