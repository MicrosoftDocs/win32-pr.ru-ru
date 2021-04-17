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
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496095"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ТЕГАМИ**](tag.md)
</dt> </dl>

 

 




