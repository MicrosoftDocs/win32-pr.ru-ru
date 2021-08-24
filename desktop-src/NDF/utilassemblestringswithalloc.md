---
title: Функция Утилассемблестрингсвисаллок (Ндаттрибутилс. h)
description: Выделяет строку и форматирует ее с помощью строк, предоставленных таблицей строк. Эта функция использует Стрингкчпринтф для создания форматированной строки.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- Утилассемблестрингсвисаллок функция NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38473f45e2bd4c53b964bb38ec285cdf3eea091a96d72684c1d801b949f4d0a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801734"
---
# <a name="utilassemblestringswithalloc-function"></a>Функция Утилассемблестрингсвисаллок

Функция **утилассемблестрингсвисаллок** выделяет строку и форматирует ее с помощью строк, предоставленных таблицей строк. Эта функция использует [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) для создания форматированной строки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Буфер* \[ заполняет\]
</dt> <dd>

Тип: **LPWSTR \***

Расположение, в которое будет помещена вновь выделенная строка. Если строка больше не нужна, она должна быть освобождена с помощью [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*Буффермакс* \[ окне\]
</dt> <dd>

Тип: **uint**

Максимально допустимое число символов в строке, выделенной *буфером*. Если полученная Форматированная строка длиннее, чем указанное число символов, она усекается и завершается нулем.

> [!Note]  
> Этот параметр не может иметь значение 0.

 

</dd> <dt>

*Инпутформат* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Строковый ресурс из таблицы строк, представляющей параметр формата, переданный в [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa). Он создается с помощью [**макеинтресаурце**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

Формат строки ресурса должен указывать либо параметр формата, принимающий расширенную строку, либо параметр формата, исключая длинную строку без знака и широкие строки.

</dd> <dt>

*InputString* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Строковый ресурс из таблицы строк, представляющей аргумент, передаваемый в [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) вместо широкой строки в параметре format. Он создается с помощью [**макеинтресаурце**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

</dd> <dt>

*Аддитионаларгумент* \[ окне\]
</dt> <dd>

Тип: **Boolean**

Значение true, если *аддитионалвалуе* следует передать в качестве первого аргумента форматирования в [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); в противном случае передается значение false (и будет передана только строка ресурса, определенная *InputString* ).

</dd> <dt>

*Аддитионалвалуе* \[ окне\]
</dt> <dd>

Тип: **ulong**

Значение, которое передается в качестве первого аргумента форматирования в [**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) , если *аддитионаларгумент* имеет значение true.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возможные возвращаемые значения включают, но не ограничиваются следующим.



| Код возврата                                                                                  | Описание                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Операция успешно выполнена.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Один или несколько параметров указаны неправильно.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**утилстрингкопивисаллок**](utilstringcopywithalloc.md)
</dt> <dt>

[**утиллоадстрингвисаллок**](utilloadstringwithalloc.md)
</dt> <dt>

[**стрингкчпринтф**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[**макеинтресаурце**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

