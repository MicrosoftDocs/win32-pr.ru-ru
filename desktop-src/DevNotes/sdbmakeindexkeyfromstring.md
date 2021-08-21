---
description: Создает ключ из строки.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Функция Сдбмакеиндекскэйфромстринг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3298b0e038218aecb9676c596e7dbad09acbbdd4441d0f1cd79c3ec2a0188720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161227"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>Функция Сдбмакеиндекскэйфромстринг

Создает ключ из строки.

## <a name="syntax"></a>Синтаксис


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзкэй* \[ окне\]
</dt> <dd>

Строка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает ключ или значение 0, если возникает ошибка.

## <a name="remarks"></a>Remarks

Стандартный ключ индекса — первые восемь символов строки, преобразованный в верхний регистр, а затем приведенный к значению **улонглонг** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




