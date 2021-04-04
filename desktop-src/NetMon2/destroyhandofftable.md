---
description: Функция Дестройхандоффтабле уничтожает таблицу, созданную с помощью Креатехандоффтабле.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Функция Дестройхандоффтабле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998408"
---
# <a name="destroyhandofftable-function"></a>Функция Дестройхандоффтабле

Функция **дестройхандоффтабле** уничтожает таблицу, созданную с помощью **креатехандоффтабле**.

## <a name="syntax"></a>Синтаксис


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хтабле* \[ окне\]
</dt> <dd>

Обработчик для уничтоженной перегрузки таблицы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




