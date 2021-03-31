---
description: Функция Експертмеморисизе Возвращает объем памяти, выделенной функцией Експерталлокмемори.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Функция Експертмеморисизе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896786"
---
# <a name="expertmemorysize-function"></a>Функция Експертмеморисизе

Функция **експертмеморисизе** Возвращает объем памяти, выделенной функцией [експерталлокмемори](expertallocmemory.md) .

## <a name="syntax"></a>Синтаксис


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хексперткэй* \[ окне\]
</dt> <dd>

Уникальный идентификатор эксперта. Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .

</dd> <dt>

*поригиналмемори* \[ окне\]
</dt> <dd>

Указатель на адрес в памяти эксперта, выделенного [експерталлокмемори](expertallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает объем выделенной памяти в байтах.

## <a name="remarks"></a>Комментарии

Сведения о типе данных «size», возвращаемом **експертмеморисизе** , см. в разделе Типы данных. **\_**

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




