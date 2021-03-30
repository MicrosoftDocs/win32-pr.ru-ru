---
description: Оператор + конкатенации соединяет две строки и возвращает объект Чстринг.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'Чстринг:: operator + (Чстринг. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815984"
---
# <a name="chstringoperator"></a>Чстринг:: operator +

\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Оператор + конкатенации соединяет две строки и возвращает объект [**чстринг**](chstring.md) .

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*
</dt> <dd>

[**Чстринг**](chstring.md) строки, которые объединяются.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*канал*
</dt> <dd>

Символ, который объединяется со строкой или строкой, которая объединяется с символом.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*лпсз*
</dt> <dd>

Указатель на строку символов, завершающуюся **нулем**.

</dd> </dl>

## <a name="return-values"></a>Возвращаемые значения

Этот оператор объединения возвращает объект [**чстринг**](chstring.md) , который является временным результатом объединения. Это возвращаемое значение позволяет объединить несколько сцеплений в одном выражении.

## <a name="remarks"></a>Комментарии

Одна из двух строк аргумента должна быть объектом [**чстринг**](chstring.md) . другой может быть указателем символа или символом. Имейте в виду, что исключения памяти могут возникать при использовании оператора объединения, так как для хранения временных данных может быть выделено новое хранилище.

## <a name="examples"></a>Примеры

В следующем примере кода показано использование **чстринг:: operator +**:


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Чстринг. h (включение Фвкоммон. h)</dt> </dl>                                                    |
| Библиотека<br/>                  | <dl> <dt>Фрамедин. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**чстринг**](chstring.md)
</dt> </dl>

 

