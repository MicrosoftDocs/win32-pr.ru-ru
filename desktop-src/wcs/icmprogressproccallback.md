---
title: Функция обратного вызова ICMProgressProcCallback
description: Функция Икмпрогресспроккаллбакк является предоставляемой приложением функцией обратного вызова, которая сообщает о ходе выполнения и позволяет приложению отменить обработку цвета.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- функция обратного вызова икмпрогресспроккаллбакк Windows цветовая система
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d697bb09b4871f6debb1a41a7ecc3e795307ee544ec30bfaf4b5b44ba0328578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117671390"
---
# <a name="icmprogressproccallback-callback-function"></a>Функция обратного вызова ICMProgressProcCallback

Функция **икмпрогресспроккаллбакк** является предоставляемой приложением функцией обратного вызова, которая сообщает о ходе выполнения и позволяет приложению отменить обработку цвета.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улмакс* 
</dt> <dd>

Задает максимальное значение счетчика хода выполнения (используется для оценки завершения обработки растрового изображения).

</dd> <dt>

*улкуррент* 
</dt> <dd>

Задает текущее значение счетчика хода выполнения (при делении на максимальное значение) представляет собой приблизительную оценку процента завершения.

</dd> <dt>

*улкаллбаккдата* 
</dt> <dd>

Указывает данные, передаваемые приложением функции ICM2, которая затем передает ее функции обратного вызова. Такие данные можно использовать, например, для указания битовой карты и процесса, о ходе которого сообщается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , чтобы продолжить обработку растрового изображения. Для отмены обработки возвращается значение **false** . Если обработка отменена, то вызывающая функция возвращает ноль для обозначения сбоя, хотя выходной буфер может быть заполнен частично.

## <a name="remarks"></a>Remarks

Имя этой функции обратного вызова предоставляется приложением. Ряд функций WCS, включая [**транслатебитмапбитс**](/windows/win32/api/icm/nf-icm-translatebitmapbits) и [**чеккбитмапбитс**](/windows/win32/api/icm/nf-icm-checkbitmapbits), периодически Вызывайте эту функцию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>ICM. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основные понятия управления цветом](basic-color-management-concepts.md)
</dt> <dt>

[Функции](functions.md)
</dt> <dt>

[**транслатебитмапбитс**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**чеккбитмапбитс**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
