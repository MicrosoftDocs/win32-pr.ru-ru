---
description: Используется для определения наличия элемента в списке последних использованных элементов.
title: Функция обратного вызова МРУКМППРОК
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991311"
---
# <a name="mrucmpproc-callback-function"></a>Функция обратного вызова МРУКМППРОК

Используется для определения наличия элемента в списке последних использованных элементов.

## <a name="syntax"></a>Синтаксис


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pString1* 
</dt> <dd>

Тип: **LPCTSTR**

Первая строка.

</dd> <dt>

*pString2* 
</dt> <dd>

Тип: **LPCTSTR**

Вторая строка для сравнения с первой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **int**

Возвращает 0, если элементы идентичны, в противном случае — ненулевое значение.

## <a name="remarks"></a>Примечания

Эту функцию можно дополнительно указать для использования в структуре [**мруинфо**](mruinfo.md) , передаваемой в [**креатемрулиств**](createmrulist.md). Это полезно, если список MRU был создан с помощью флага **\_ двоичного файла MRU** . Если эта функция не задана, используются стандартные функции сравнения строк.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>      |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>            |
| Имя в кодировке Юникод и ANSI<br/>   | **Мрукмппрокв** (Юникод) и **мрукмппрока** (ANSI)<br/> |



 

 




