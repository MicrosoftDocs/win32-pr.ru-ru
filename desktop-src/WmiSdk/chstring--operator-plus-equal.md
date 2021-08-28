---
description: Оператор объединения + = соединяет символы до конца этой строки. Оператор принимает другой объект Чстринг, указатель на символ или отдельный символ.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'Чстринг:: operator + = (Чстринг. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316f5272c7b5a4ef5b59e93dd480ade215e3279ea754f1da5432448d46fcce17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679883"
---
# <a name="chstringoperator"></a>Чстринг:: operator + =

\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Оператор объединения + = соединяет символы до конца этой строки. Оператор принимает другой объект [**чстринг**](chstring.md) , указатель на символ или отдельный символ.

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="string"></span><span id="STRING"></span>*Строка*
</dt> <dd>

Строка [**чстринг**](chstring.md) , которая объединяется с этой строкой.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*канал*
</dt> <dd>

Символ для сцепления с этой строкой.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*лпсз*
</dt> <dd>

Указатель на строку **,** завершающуюся нулем, для сцепления с этой строкой.

</dd> </dl>

## <a name="remarks"></a>Remarks

Имейте в виду, что при использовании этого оператора объединения могут возникать исключения памяти, так как для символов, добавляемых в этот объект [**чстринг**](chstring.md) , может быть выделено новое хранилище.

## <a name="examples"></a>Примеры

В следующем примере показано использование **чстринг:: operator + =**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Заголовок<br/>                   | <dl> <dt>Чстринг. h (включение Фвкоммон. h)</dt> </dl>                                                    |
| Библиотека<br/>                  | <dl> <dt>Фрамедин. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**чстринг**](chstring.md)
</dt> </dl>

 

