---
description: Добавляет строку в верхнюю часть списка недавно использовавшихся (MRU).
title: Функция AddMRUStringW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: 4ac72c44b670466f10cd708b81b1a84f93a349afcb0d81473ed5e6578c20617a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861596"
---
# <a name="addmrustringw-function"></a>Функция AddMRUStringW

\[эта функция доступна в Windows XP с пакетом обновления 2 (sp2) и Windows Server 2003. Он может быть изменен или недоступен в последующих версиях Windows. \]

Добавляет строку в верхнюю часть списка недавно использовавшихся (MRU).

## <a name="syntax"></a>Синтаксис


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмру* \[ окне\]
</dt> <dd>

Тип: **Handle**

Маркер списка MRU.

</dd> <dt>

*сзстринг* \[ окне\]
</dt> <dd>

Тип: **LPCTSTR**

Указатель на данные. Это может быть либо строка, либо, если список MRU был создан с помощью **\_ двоичного** флага MRU, двоичных данных. В случае двоичных данных первый **DWORD** указывает на его размер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **int**

При успешном выполнении возвращает неотрицательное значение – 1 в противном случае.

## <a name="remarks"></a>Remarks

Эта функция не включена в общедоступный заголовок или библиотеку. Доступ к нему можно получить с помощью [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) или извлечь из comctl32.dll по порядковому номеру, 401 для **аддмрустрингв**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                     |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (версия 5,0 или более поздняя)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Аддмрустрингв** (Юникод)<br/>                                                                         |



 

