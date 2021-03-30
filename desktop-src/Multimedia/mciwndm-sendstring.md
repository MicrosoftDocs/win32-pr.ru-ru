---
title: Сообщение MCIWNDM_SENDSTRING (VFW. h)
description: Сообщение МЦИВНДМ \_ сендстринг отправляет команду MCI в виде строки на устройство, связанное с окном мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндсендстринг.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803016"
---
# <a name="mciwndm_sendstring-message"></a>\_Сообщение мЦивндм сендстринг

Сообщение **мЦивндм \_ сендстринг** отправляет команду MCI в виде строки на устройство, связанное с окном мЦивнд. Это сообщение можно отправить явно или с помощью макроса [**мЦивндсендстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*SZ*
</dt> <dd>

Строка команды для отправки на устройство MCI.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Обработчик сообщений для **мЦивндм \_ сендстринг** добавляет псевдоним устройства к команде MCI, отправляемой на устройство. Поэтому не следует использовать псевдоним в команде MCI, которую вы выпустили с помощью **мЦивндм \_ сендстринг**.

Чтобы получить возвращаемую строку, которая содержит результат выполнения команды, отправьте сообщение [**мЦивндм \_ ретурнстринг**](mciwndm-returnstring.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндсендстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Строки команд мультимедиа](multimedia-command-strings.md)
</dt> </dl>

 

 





