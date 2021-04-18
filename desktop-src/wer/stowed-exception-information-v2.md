---
title: Структура STOWED_EXCEPTION_INFORMATION_V2
description: Содержит сведения об исключении заполнения.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 структуры отчеты об ошибках Windows
- PSTOWED_EXCEPTION_INFORMATION_V2 отчеты об ошибках Windows указателя на структуру
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701087"
---
# <a name="stowed_exception_information_v2-structure"></a>\_ \_ Структура сведений об исключении заполнения \_ v2

Содержит сведения об исключении заполнения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a>Члены

<dl> <dt>

**Header**
</dt> <dd>

Тип: **[ **\_ \_ \_ заголовок сведений об исключении заполнения**](stowed-exception-information-header.md)**

</dd> <dd>

Структура [**\_ \_ \_ заголовка сведений об исключении заполнения**](stowed-exception-information-header.md) , содержащая сведения для этой родительской структуры.

</dd> <dt>

**ResultCode**
</dt> <dd>

Тип: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Код [**HRESULT**](/windows/desktop/WinProg/windows-data-types) для исключения заполнения.

</dd> <dt>

**ексцептионформ**
</dt> <dd>

Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

2-разрядное значение, идентифицирующее форму исключения.



| Значение                                                                                                                                                                                                                                                                  | Значение                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <dt>**Заполнения \_ \_ \_ Двоичные данные формы исключений**</dt> <dt>0x01</dt> </dl> | Это значение указывает, что форма исключения является двоичной.<br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <dt>**Заполнения \_ \_ \_ Текст формы исключения**</dt> <dt>0x02</dt> </dl>       | Это значение указывает, что в качестве исключения используется текст.<br/>   |



 

</dd> <dt>

**Tидентификатор**
</dt> <dd>

Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

30-разрядное значение, идентифицирующее поток, вызвавший исключение. При сохранении значение перемещается вправо на 2 бита. Чтобы преобразовать его обратно в допустимый идентификатор потока, сдвиньте значение влево на 2. Пример:

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

(*безымянная структура*)
</dt> <dd>

Члены этой вложенной структуры являются допустимыми только в том случае, если для элемента **ексцептионформ** задано значение **заполнения в \_ \_ виде \_ двоичной формы исключений**.

<dl> <dt>

**ексцептионаддресс**
</dt> <dd>

Тип: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Указатель, содержащий адрес исключения.

</dd> <dt>

**стакктрацевордсизе**
</dt> <dd>

Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Размер (в байтах) каждого слова в трассировке стека, на которое указывает элемент **StackTrace** . Это значение равно 4 для 32-разрядных платформ и 8 для 64-разрядных платформ.

</dd> <dt>

**стакктрацевордс**
</dt> <dd>

Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Количество слов в трассировке стека, на которое указывает элемент **StackTrace** . Число слов равно числу элементов в массиве.

</dd> <dt>

**StackTrace**
</dt> <dd>

Тип: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Указатель на блок памяти, содержащий трассировку стека.

</dd> </dl> </dd> <dt>

(*безымянная структура*)
</dt> <dd>

Элемент этой вложенной структуры допустим только в том случае, если для элемента **ексцептионформ** задано значение **заполнения в \_ \_ виде \_ текста формы исключения**.

<dl> <dt>

**ErrorText**
</dt> <dd>

Тип: **[ **пвстр**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Указатель на строку, завершающуюся нулем, которая содержит текст ошибки исключения.

</dd> </dl> </dd> <dt>

**нестедексцептионтипе**
</dt> <dd>

Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

32-разрядное значение, указывающее тип объекта, на который указывает элемент **нестедексцептион** . Определите значение с помощью этого макроса типа swap-Definition, который предполагается с прямым порядком байтов:

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

Ниже приведены некоторые общие определения типов.



| Значение                                                                                                                                                                                                                                                                                                                           | Значение                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <dt>**Заполнения \_ \_Вложенный \_ тип исключения \_ None**</dt> <dt>(0x00000000)</dt> </dl>                                  | Это значение указывает на отсутствие вложенного объекта исключения.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <dt>**Заполнения \_ \_Вложенный \_ тип исключения \_ Win32**</dt> <dt>заполнения \_ Exception \_ Nested \_ Type (' W32E ')</dt> </dl>    | Это значение указывает, что элемент **нестедексцептион** указывает на объект [**\_ записи исключения**](/windows/desktop/api/winnt/ns-winnt-exception_record) .<br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <dt>**Заполнения \_ EXCEPTION Nested \_ \_ Type \_ заполнения**</dt> <dt>заполнения \_ \_ Nested \_ Type (' стов ')</dt> </dl> | Это значение указывает, что элемент **нестедексцептион** указывает на другой объект исключения заполнения. Другим объектом исключения заполнения может быть объект **\_ сведений об исключении заполнения \_ \_ версии 2** или другая версия с допустимым **элементом заголовка** , то есть элементом **заголовка** , содержащим допустимый [**\_ \_ \_ заголовок сведений об исключении заполнения**](stowed-exception-information-header.md).<br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <dt>**Заполнения \_ ИСКЛЮЧЕНИЕ вложенного типа \_ \_ \_ CLR**</dt> заполнения Exception Nested Type <dt> \_ \_ \_ (' файле clr1 ')</dt> </dl>          | Это значение указывает, что элемент **нестедексцептион** указывает на объект исключения "файле clr1".<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <dt>**Заполнения \_ EXCEPTION Nested \_ \_ Type \_ Leo**</dt> <dt>заполнения \_ \_ Nested \_ Type (' LEO1 ')</dt> </dl>          | Это значение указывает, что элемент **нестедексцептион** указывает на объект исключения языка.<br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

**нестедексцептион**
</dt> <dd>

Тип: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Указатель на тип вложенного исключения. Тип объекта указывается членом **нестедексцептионтипе** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Заполнения \_ Заголовок сведений об ИСКЛЮЧЕНии \_ \_ v2** и заполнения в настоящее время не определен в заголовке, который является общедоступным, поэтому необходимо определить их в исходном коде, прежде чем использовать их. [**\_ \_ \_**](stowed-exception-information-header.md)

Структура **\_ \_ сведений об исключении \_ заполнения** версии 1 идентична этой структуре, за исключением того, что она не содержит членов **нестедексцептионтипе** и **нестедексцептион** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                         |
| Header<br/>                   | <dl> <dt>Нет</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_запись исключения**](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[**\_ \_ заголовок сведений об ИСКЛЮЧЕНии заполнения \_**](stowed-exception-information-header.md)
</dt> </dl>

 

