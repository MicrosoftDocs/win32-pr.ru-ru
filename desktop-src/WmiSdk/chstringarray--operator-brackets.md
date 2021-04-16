---
description: Эти операторы индексов задают или получают элемент по указанному индексу. Эти операторы являются удобным заменой для методов SetAt и GetAt.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'Чстрингаррай:: operator [] (Чстрарр. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712673"
---
# <a name="chstringarrayoperator--"></a>Чстрингаррай:: operator \[\]

\[Класс [**чстрингаррай**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Эти операторы индексов задают или получают элемент по указанному индексу. Эти операторы являются удобным заменой для методов [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) и [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*ниндекс*
</dt> <dd>

Целочисленный индекс, который больше или равен нулю и меньше или равен значению, возвращаемому функцией [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>Возвращаемые значения

Операторы подстрочных индексов возвращают элемент указателя [**чстринг**](chstring.md) в данный момент в этом индексе.

## <a name="remarks"></a>Комментарии

Можно использовать первый оператор, который вызывает для массивов, которые не являются **константами**, либо справа (r-Value), либо слева (l-значение) оператора присваивания. Вторая, которая вызывает **константные** массивы, может использоваться только справа.

Отладочная версия библиотеки утверждает, находится ли индекс (в левой или правой части инструкции присваивания) вне границ.

## <a name="examples"></a>Примеры

В следующем примере кода показано использование [**оператора чстрингаррай: \[ \] : operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Чстрарр. h (включение Фвкоммон. h)</dt> </dl>                                                    |
| Библиотека<br/>                  | <dl> <dt>Фрамедин. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Чстрингаррай:: Add**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**Чстрингаррай:: GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**Чстрингаррай:: SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

