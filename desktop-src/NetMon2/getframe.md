---
description: Функция noframes возвращает маркер в заданный кадр в пределах записи.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Функция noframes (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5f6f992c0c61978e2de6f90755852c9e29d6ac51d7ae7f2405ef981ed695c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779254"
---
# <a name="getframe-function"></a>Функция NOFRAMES

Функция **noframes** возвращает маркер в заданный кадр в пределах записи.

## <a name="syntax"></a>Синтаксис


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хкаптуре* \[ окне\]
</dt> <dd>

Обработчик для записи. Чтобы получить маркер записи, вызовите функцию [жетфрамекаптурехандле](getframecapturehandle.md) .

</dd> <dt>

*Фраменумбер* \[ окне\]
</dt> <dd>

Число (от нуля) кадра. Номер первого кадра в записи равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является обработкой кадра.

Если функция завершилась неудачно (т. е. Если *хкаптуре* является недопустимым или номер кадра выходит за пределы диапазона), возвращается значение **null**.

## <a name="remarks"></a>Remarks

Используйте функцию **noframes** для получения маркера кадра, необходимого при размещении экземпляров свойства. Функции, используемые для размещения экземпляров свойств, — это [финдпропертинстанце](findpropertyinstance.md) , которые находят первый экземпляр, и [финдпропертинстанцерестарт](findpropertyinstancerestart.md) , который находит следующий экземпляр.

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **noframes** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[финдпропертинстанце](findpropertyinstance.md)
</dt> <dt>

[финдпропертинстанцерестарт](findpropertyinstancerestart.md)
</dt> </dl>

 

 




