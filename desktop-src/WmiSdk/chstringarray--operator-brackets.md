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
# <a name="chstringarrayoperator--"></a><span data-ttu-id="1e0b7-104">Чстрингаррай:: operator \[\]</span><span class="sxs-lookup"><span data-stu-id="1e0b7-104">CHStringArray::operator \[ \]</span></span>

<span data-ttu-id="1e0b7-105">\[Класс [**чстрингаррай**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="1e0b7-105">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="1e0b7-106">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="1e0b7-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="1e0b7-107">Эти операторы индексов задают или получают элемент по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="1e0b7-107">These subscript operators set or get the element at the specified index.</span></span> <span data-ttu-id="1e0b7-108">Эти операторы являются удобным заменой для методов [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) и [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .</span><span class="sxs-lookup"><span data-stu-id="1e0b7-108">These operators are a convenient substitute for the [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) and [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) methods.</span></span>

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a><span data-ttu-id="1e0b7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e0b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e0b7-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*ниндекс*</span><span class="sxs-lookup"><span data-stu-id="1e0b7-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span></span>
</dt> <dd>

<span data-ttu-id="1e0b7-111">Целочисленный индекс, который больше или равен нулю и меньше или равен значению, возвращаемому функцией [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span><span class="sxs-lookup"><span data-stu-id="1e0b7-111">An integer index that is greater than or equal to zero and less than or equal to the value returned by [**GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="1e0b7-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1e0b7-112">Return Values</span></span>

<span data-ttu-id="1e0b7-113">Операторы подстрочных индексов возвращают элемент указателя [**чстринг**](chstring.md) в данный момент в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="1e0b7-113">The subscript operators return the [**CHString**](chstring.md) pointer element currently at this index.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e0b7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e0b7-114">Remarks</span></span>

<span data-ttu-id="1e0b7-115">Можно использовать первый оператор, который вызывает для массивов, которые не являются **константами**, либо справа (r-Value), либо слева (l-значение) оператора присваивания.</span><span class="sxs-lookup"><span data-stu-id="1e0b7-115">You can use the first operator, which calls for arrays that are not **const**, on either the right (r-value) or the left (l-value) side of an assignment statement.</span></span> <span data-ttu-id="1e0b7-116">Вторая, которая вызывает **константные** массивы, может использоваться только справа.</span><span class="sxs-lookup"><span data-stu-id="1e0b7-116">The second, which calls for **const** arrays, can be used only on the right.</span></span>

<span data-ttu-id="1e0b7-117">Отладочная версия библиотеки утверждает, находится ли индекс (в левой или правой части инструкции присваивания) вне границ.</span><span class="sxs-lookup"><span data-stu-id="1e0b7-117">The debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="1e0b7-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="1e0b7-118">Examples</span></span>

<span data-ttu-id="1e0b7-119">В следующем примере кода показано использование [**оператора чстрингаррай: \[ \] : operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1e0b7-119">The following code example shows the use of [**CHStringArray::operator \[\]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1e0b7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1e0b7-120">Requirements</span></span>



| <span data-ttu-id="1e0b7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1e0b7-121">Requirement</span></span> | <span data-ttu-id="1e0b7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1e0b7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0b7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e0b7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1e0b7-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0b7-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="1e0b7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e0b7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1e0b7-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e0b7-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="1e0b7-127">Header</span><span class="sxs-lookup"><span data-stu-id="1e0b7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e0b7-128"><dt>Чстрарр. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e0b7-128"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1e0b7-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e0b7-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e0b7-130"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e0b7-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="1e0b7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1e0b7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e0b7-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e0b7-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e0b7-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e0b7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0b7-134">**Чстрингаррай:: Add**</span><span class="sxs-lookup"><span data-stu-id="1e0b7-134">**CHStringArray::Add**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

<span data-ttu-id="1e0b7-135">[**Чстрингаррай:: GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="1e0b7-135">[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
</dt> <dt>

<span data-ttu-id="1e0b7-136">[**Чстрингаррай:: SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="1e0b7-136">[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
</dt> </dl>

