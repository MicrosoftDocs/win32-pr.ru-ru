---
description: Функция Жетнетворкинфофромблоб извлекает сведения о сети из заданного большого двоичного объекта.
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: Функция Жетнетворкинфофромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674490"
---
# <a name="getnetworkinfofromblob-function"></a>Функция Жетнетворкинфофромблоб

Функция **жетнетворкинфофромблоб** извлекает сведения о сети из заданного большого двоичного объекта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик для большого двоичного объекта.

</dd> <dt>

*лпнетворкинфо* \[ в, out\]
</dt> <dd>

Указатель на выделенную пользователем структуру [нетворкинфо](networkinfo.md) , которая заполняется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция **жетнетворкинфофромблоб** выполнена успешно, возвращается значение нмерр \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.

## <a name="remarks"></a>Комментарии

Сведения о сети хранятся в разделе **нетворкинфо** большого двоичного объекта категории **владельца** BLOB-объекта НПП.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[сетнетворкинфоинблоб](setnetworkinfoinblob.md)
</dt> <dt>

[жетбулфромблоб](getboolfromblob.md)
</dt> <dt>

[жетклассидфромблоб](getclassidfromblob.md)
</dt> <dt>

[жетдвордфромблоб](getdwordfromblob.md)
</dt> <dt>

[жетмакаддрессфромблоб](getmacaddressfromblob.md)
</dt> <dt>

[жетнппаддрессфилтерфромблоб](getnppaddressfilterfromblob.md)
</dt> <dt>

[жетнпппаттернфилтерфромблоб](getnpppatternfilterfromblob.md)
</dt> <dt>

[жетнпптригжерфромблоб](getnpptriggerfromblob.md)
</dt> <dt>

[жетстрингфромблоб](getstringfromblob.md)
</dt> <dt>

[жетстрингсфромблоб](getstringsfromblob.md)
</dt> </dl>

 

 




