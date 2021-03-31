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
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804061"
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

Введите: **LPWSTR \** _

Расположение, в которое будет помещена вновь выделенная строка. Если строка больше не нужна, она должна быть освобождена с помощью [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

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



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

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

 

