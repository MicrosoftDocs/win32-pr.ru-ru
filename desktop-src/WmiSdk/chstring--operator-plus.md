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
# <a name="chstringoperator"></a><span data-ttu-id="9d5ed-103">Чстринг:: operator +</span><span class="sxs-lookup"><span data-stu-id="9d5ed-103">CHString::operator+</span></span>

<span data-ttu-id="9d5ed-104">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="9d5ed-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="9d5ed-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="9d5ed-106">Оператор + конкатенации соединяет две строки и возвращает объект [**чстринг**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="9d5ed-106">The + concatenation operator joins two strings and returns a [**CHString**](chstring.md) object.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="9d5ed-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d5ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5ed-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*</span><span class="sxs-lookup"><span data-stu-id="9d5ed-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*</span></span>
</dt> <dd>

<span data-ttu-id="9d5ed-109">[**Чстринг**](chstring.md) строки, которые объединяются.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-109">[**CHString**](chstring.md) strings that are concatenated.</span></span>

</dd> <dt>

<span data-ttu-id="9d5ed-110"><span id="ch"></span><span id="CH"></span>*канал*</span><span class="sxs-lookup"><span data-stu-id="9d5ed-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="9d5ed-111">Символ, который объединяется со строкой или строкой, которая объединяется с символом.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-111">A character that concatenates to a string or a string that concatenates to a character.</span></span>

</dd> <dt>

<span data-ttu-id="9d5ed-112"><span id="lpsz"></span><span id="LPSZ"></span>*лпсз*</span><span class="sxs-lookup"><span data-stu-id="9d5ed-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="9d5ed-113">Указатель на строку символов, завершающуюся **нулем**.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-113">Pointer to a **NULL**-terminated character string.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="9d5ed-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9d5ed-114">Return Values</span></span>

<span data-ttu-id="9d5ed-115">Этот оператор объединения возвращает объект [**чстринг**](chstring.md) , который является временным результатом объединения.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-115">This concatenation operator returns a [**CHString**](chstring.md) object that is the temporary result of the concatenation.</span></span> <span data-ttu-id="9d5ed-116">Это возвращаемое значение позволяет объединить несколько сцеплений в одном выражении.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-116">This return value makes it possible to combine several concatenations in the same expression.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5ed-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d5ed-117">Remarks</span></span>

<span data-ttu-id="9d5ed-118">Одна из двух строк аргумента должна быть объектом [**чстринг**](chstring.md) . другой может быть указателем символа или символом.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-118">One of the two argument strings must be a [**CHString**](chstring.md) object; the other can be a character pointer or a character.</span></span> <span data-ttu-id="9d5ed-119">Имейте в виду, что исключения памяти могут возникать при использовании оператора объединения, так как для хранения временных данных может быть выделено новое хранилище.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-119">Be aware that memory exceptions can occur whenever you use the concatenation operator because new storage may be allocated to hold temporary data.</span></span>

## <a name="examples"></a><span data-ttu-id="9d5ed-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="9d5ed-120">Examples</span></span>

<span data-ttu-id="9d5ed-121">В следующем примере кода показано использование **чстринг:: operator +**:</span><span class="sxs-lookup"><span data-stu-id="9d5ed-121">The following code example shows the use of **CHString::operator +**:</span></span>


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a><span data-ttu-id="9d5ed-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9d5ed-122">Requirements</span></span>



| <span data-ttu-id="9d5ed-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9d5ed-123">Requirement</span></span> | <span data-ttu-id="9d5ed-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9d5ed-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5ed-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d5ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5ed-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d5ed-126">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="9d5ed-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d5ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5ed-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d5ed-128">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="9d5ed-129">Header</span><span class="sxs-lookup"><span data-stu-id="9d5ed-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5ed-130"><dt>Чстринг. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d5ed-130"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9d5ed-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9d5ed-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d5ed-132"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d5ed-132"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="9d5ed-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9d5ed-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d5ed-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d5ed-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d5ed-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d5ed-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5ed-136">**чстринг**</span><span class="sxs-lookup"><span data-stu-id="9d5ed-136">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

