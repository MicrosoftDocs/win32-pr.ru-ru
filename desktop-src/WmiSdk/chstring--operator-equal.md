---
description: Оператор присваивания Чстринг (=) повторно инициализирует существующий объект Чстринг новыми данными.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'Чстринг:: operator = (Чстринг. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dde67bbf0f1a7326074bc7638cdd6b256ad763e115ad12e2c193e6bcdc66605e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131786"
---
# <a name="chstringoperator"></a>Чстринг:: operator =

\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Оператор присваивания [**чстринг**](chstring.md) (=) повторно инициализирует существующий объект чстринг новыми данными.

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*стрингсрк*, *p*
</dt> <dd>

Присваивает [**чстринг**](chstring.md) строку этому объекту.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*канал*
</dt> <dd>

Присваивает символ этому объекту.

</dd> <dt>

<span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*лпсз*, *ПСЗ*
</dt> <dd>

Присваивает этому объекту **строку, завершающуюся нулем.**

</dd> </dl>

## <a name="remarks"></a>Remarks

Если строка назначения (то есть левая часть) уже достаточно велика для хранения новых данных, выделение памяти не выполняется. Однако исключения памяти могут возникать при каждом использовании оператора присваивания, поскольку для хранения результирующего объекта [**чстринг**](chstring.md) часто выделяется новое хранилище.

## <a name="examples"></a>Примеры

В следующем примере кода показано использование **чстринг:: operator =**:


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Заголовок<br/>                   | <dl> <dt>Чстринг. h (включение Фвкоммон. h)</dt> </dl>                                                    |
| Библиотека<br/>                  | <dl> <dt>Фрамедин. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**чстринг**](chstring.md)
</dt> </dl>

 

