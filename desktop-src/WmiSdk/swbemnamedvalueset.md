---
description: Объект Свбемнамедвалуесет — это коллекция объектов Свбемнамедвалуе.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Объект Свбемнамедвалуесет (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701961"
---
# <a name="swbemnamedvalueset-object"></a>Объект Свбемнамедвалуесет

Объект **свбемнамедвалуесет** — это коллекция объектов [**свбемнамедвалуе**](swbemnamedvalue.md) . Методы и свойства **свбемнамедвалуесет** используются для отправки дополнительных сведений поставщикам при отправке определенных вызовов WMI. Все вызовы в [**SwbemServices**](swbemservices.md)и некоторые вызовы в [**SWbemObject**](swbemobject.md)принимают необязательный параметр, который является объектом этого типа. Клиент может добавить сведения в объект **свбемнамедвалуесет** и отправить объект **свбемнамедвалуесет** с вызовом в качестве одного из параметров. Этот объект может быть создан вызовом метода **CreateObject** VBScript.

Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).

> [!Note]  
> Важно! если возможно, не используйте этот механизм, так как он может нарушить унифицированную модель доступа, которая является основанием инструментария WMI. Если поставщик использует этот механизм, важно, чтобы этот механизм использовался как можно реже. Если поставщику требуется большой объем строго специфической контекстной информации для ответа на запрос, все клиенты должны быть написаны для предоставления этих сведений. Этот механизм позволяет при необходимости получить доступ к таким поставщикам.

 

Объект **свбемнамедвалуесет** — это коллекция элементов [**свбемнамедвалуе**](swbemnamedvalue.md) . Эти элементы добавляются в коллекцию с помощью метода [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) . Они удаляются с помощью метода [**свбемнамедвалуесет. Remove**](swbemnamedvalueset-remove.md) и извлекаются с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) . Вы можете получить доступ к методам, чтобы заполнить любые сведения о контексте, необходимые для динамического поставщика. После вызова одного из методов [**SwbemServices**](swbemservices.md) можно повторно использовать объект **свбемнамедвалуесет** для другого вызова.

Базовый поставщик определяет сведения, содержащиеся в объекте **свбемнамедвалуесет** . Инструментарий WMI не использует эти сведения, но просто пересылает его поставщику. Поставщики должны публиковать сведения о контексте, необходимые им для запросов на обслуживание.

## <a name="members"></a>Элементы

Объект **свбемнамедвалуесет** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **свбемнамедвалуесет** содержит эти методы.



| Метод                                            | Описание                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Включить**](swbemnamedvalueset-add.md)             | Добавляет объект [**свбемнамедвалуе**](swbemnamedvalue.md) в коллекцию.<br/>                                                  |
| [**Клонировать**](swbemnamedvalueset-clone.md)         | Создает копию этой коллекции **свбемнамедвалуесет** .<br/>                                                                       |
| [**DeleteAll**](swbemnamedvalueset-deleteall.md) | Удаляет все элементы из коллекции, делая объект **свбемнамедвалуесет** пустым.<br/>                                        |
| [**Элемент**](swbemnamedvalueset-item.md)           | Извлекает объект [**свбемнамедвалуе**](swbemnamedvalue.md) из коллекции. Это метод объекта по умолчанию.<br/> |
| [**Отменит**](swbemnamedvalueset-remove.md)       | Удаляет объект [**свбемнамедвалуе**](swbemnamedvalue.md) из коллекции.<br/>                                             |



 

### <a name="properties"></a>Свойства

Объект **свбемнамедвалуесет** имеет следующие свойства.



| Свойство                                             | Тип доступа          | Описание                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Расчета**](swbemnamedvalueset-count.md)<br/> | Только для чтения<br/> | Количество элементов в коллекции.<br/> |



 

## <a name="examples"></a>Примеры

В следующем примере VBScript демонстрируется работа с именованными наборами значений в случае, если именованное значение является типом массива.


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



В следующем образце Perl показано управление именованными наборами значений в случае, если именованное значение является типом массива.


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМНАМЕДВАЛУЕСЕТ CLSID<br/>                                                    |
| IID<br/>                      | IID \_ исвбемнамедвалуесет<br/>                                                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




