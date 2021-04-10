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
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143789"
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

## <a name="remarks"></a>Комментарии

Используйте функцию **noframes** для получения маркера кадра, необходимого при размещении экземпляров свойства. Функции, используемые для размещения экземпляров свойств, — это [финдпропертинстанце](findpropertyinstance.md) , которые находят первый экземпляр, и [финдпропертинстанцерестарт](findpropertyinstancerestart.md) , который находит следующий экземпляр.

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **noframes** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[финдпропертинстанце](findpropertyinstance.md)
</dt> <dt>

[финдпропертинстанцерестарт](findpropertyinstancerestart.md)
</dt> </dl>

 

 




