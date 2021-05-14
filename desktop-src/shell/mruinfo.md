---
description: Содержит сведения, определяющие новый список недавно использованных (MRU) списков. Используется Креатемрулиств.
title: Структура МРУИНФО
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840765"
---
# <a name="mruinfo-structure"></a>Структура МРУИНФО

Содержит сведения, определяющие новый список недавно использованных (MRU) списков. Используется [**креатемрулиств**](createmrulist.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Размер структуры.

</dd> <dt>

**Компания**
</dt> <dd>

Тип: **uint**

</dd> <dd>

Максимальное число записей в списке MRU.

</dd> <dt>

**ффлагс**
</dt> <dd>

Тип: **uint**

</dd> <dd>

Один или несколько следующих флагов.

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ ДВОИЧный** (0x0001)


</dt> <dd>

Данные хранятся в реестре в виде двоичных данных, а не строковых данных.

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ КАЧЕВРИТЕ** (0x0002)


</dt> <dd>

Запись изменений в версию MRU, сохраненную в реестре, только при добавлении нового элемента или освобождении ресурсов списка MRU из памяти. Обратите внимание, что активная версия MRU в памяти обновляется немедленно в ответ на любые изменения в содержании или упорядочении.

</dd> </dl> </dd> <dt>

**hKey**
</dt> <dd>

Тип: **hKey**

</dd> <dd>

Обработчик текущего открытого ключа или одно из следующих предопределенных значений, по которым сохраняются данные MRU.

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**HKEY \_ текущего \_ пользователя**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**HKEY \_ локальный \_ компьютер**
</dt> </dl> </dd> <dt>

**лпсзсубкэй**
</dt> <dd>

Тип: **LPCTSTR**

</dd> <dd>

Подраздел, в котором сохраняются данные MRU.

</dd> <dt>

**лпфнкомпаре**
</dt> <dd>

Тип: **[ **мрукмппрок**](mrucmpproc.md)**

</dd> <dd>

Указатель на необязательную функцию сравнения данных, которую можно использовать для определения наличия элемента в списке MRU. Это полезно, если список MRU был создан с помощью флага **\_ двоичного файла MRU** . Если этот член имеет **значение NULL**, используются стандартные функции сравнения строк. для двоичных данных используется прямое сравнение памяти.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура не определена в файле заголовка. Его необходимо определить самостоятельно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |
| Имя в кодировке Юникод и ANSI<br/>   | **Мруинфов** (Юникод) и **мруинфоа** (ANSI)<br/>  |



 

 




