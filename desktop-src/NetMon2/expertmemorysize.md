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
ms.openlocfilehash: 69dae4ca2a7f7a9e3b2f77047475c5dd35f54a3394b4481c2f452a46e983c35e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744274"
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

## <a name="remarks"></a>Remarks

Сведения о типе данных «size», возвращаемом **експертмеморисизе** , см. в разделе Типы данных. **\_**

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




