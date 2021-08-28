---
description: маркер среда выполнения Windows строки.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (HString. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b43c92d439cec10c0d1683efb1e8ceafd8165a35c3c8aa9a1b35150e43a33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121574"
---
# <a name="hstring"></a>HSTRING

маркер среда выполнения Windows строки.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Remarks

используйте **HSTRING** для представления неизменяемых строк в среда выполнения Windows.

JavaScript и другие языки, такие как C \# и Microsoft Visual Basic, могут использовать строки, представленные с помощью **HSTRING**. В следующей таблице показано, как **HString** представлен на других языках.



| Язык программирования                                                                    | Строковое представление                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | класс [WinRT:: HString](/uwp/cpp-ref-for-winrt/hstring)     |
| Расширения компонентов Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | Класс [Platform:: String](/cpp/cppcx/platform-string-class) |
| JavaScript                                                                              | String - объект                                              |
| .NET Framework                                                                          | Класс System. String                                        |



 

Обработчик **HString** является стандартным типом обработчика. Семантически, **HString** , содержащий значение **null** , представляет пустую строку, которая состоит из нулевых символов содержимого и завершающего **нуль** -символа. Создание строки через [**виндовскреатестринг**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) с нулевым числом символов приведет к созданию значения **null** для этого обработчика. При вызове [**виндовсжетстрингравбуффер**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) со значением **null** возвращается указатель на пустую строку, за которым следует только завершающий символ **nul** . Не существует уникального значения, представляющего неинициализированный **HString** .

Вызовите функцию [**виндовскреатестринг**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) , чтобы создать новый **HString**, и вызовите функцию [**виндовсделетестринг**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) для освобождения ссылки на память резервной строки. Вызовите функцию [**виндовскреатестрингреференце**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , чтобы создать ссылку на строку, которая также называется *быстрой передачей строки*.

Скопируйте **HString** , вызвав функцию [**виндовсдупликатестринг**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .

Объедините две строки, вызвав функцию [**виндовсконкатстринг**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .

Получите доступ к резервной памяти строки, вызвав функцию [**виндовсжетстрингравбуффер**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .

**HString** может хранить и использовать внедренные символы **NUL** . Используйте функцию [**виндовсстрингхасембеддеднулл**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) для проверки внедренных символов **NUL** перед использованием любых функций, которые могут привести к непредвиденным результатам. например, большинство функций Windows используют **лпквстр** в качестве входного параметра и вычисляют длину строки только до тех пор, пока не встретится первое значение **NUL** .

Резервная строка должна оставаться неизменной и завершаться нулем. При вызове кода создает ссылку на строку с помощью функции [**виндовскреатестрингреференце**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , память, которая содержит представление резервной строки, принадлежит вызывающему объекту. среда выполнения Windows полагается на содержимое исходной строки, чтобы остаться без изменений. при передаче ссылки на строку в среда выполнения Windows, вызывающий объект следит за тем, чтобы содержимое строки было неизменным, а **NUL** была прервана на время вызова. среда выполнения Windows освобождает все ссылки на ссылку на строку, когда вызов возвращает.

При получении **HString** в качестве выходного параметра рекомендуется присвоить этому обработчику **значение NULL** по завершении работы с ним.

Вызовите функцию [**виндовспреаллокатестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) , чтобы выделить изменяемый буфер строк, который можно использовать для создания неизменяемого **HString**. Завершив заполнение буфера, вызовите функцию [**виндовспромотестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) , чтобы создать **HString**. Этот шаблон двухстраничного конструкции позволяет реализовать функции, аналогичные "построителю строк".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>HString. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>


</dt> <dt>

[**виндовскреатестринг**](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[**виндовсделетестринг**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[**виндовсдупликатестринг**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[**виндовспреаллокатестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
