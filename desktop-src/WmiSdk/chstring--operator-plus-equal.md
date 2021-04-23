---
description: Оператор объединения + = соединяет символы до конца этой строки. Оператор принимает другой объект Чстринг, указатель на символ или отдельный символ.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'Чстринг:: operator + = (Чстринг. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712117"
---
# <a name="chstringoperator"></a><span data-ttu-id="afd6d-104">Чстринг:: operator + =</span><span class="sxs-lookup"><span data-stu-id="afd6d-104">CHString::operator+=</span></span>

<span data-ttu-id="afd6d-105">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="afd6d-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="afd6d-106">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="afd6d-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="afd6d-107">Оператор объединения + = соединяет символы до конца этой строки.</span><span class="sxs-lookup"><span data-stu-id="afd6d-107">The += concatenation operator joins characters to the end of this string.</span></span> <span data-ttu-id="afd6d-108">Оператор принимает другой объект [**чстринг**](chstring.md) , указатель на символ или отдельный символ.</span><span class="sxs-lookup"><span data-stu-id="afd6d-108">The operator accepts another [**CHString**](chstring.md) object, a character pointer, or a single character.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="afd6d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="afd6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd6d-110"><span id="string"></span><span id="STRING"></span>*Строка*</span><span class="sxs-lookup"><span data-stu-id="afd6d-110"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="afd6d-111">Строка [**чстринг**](chstring.md) , которая объединяется с этой строкой.</span><span class="sxs-lookup"><span data-stu-id="afd6d-111">A [**CHString**](chstring.md) string that concatenates to this string.</span></span>

</dd> <dt>

<span data-ttu-id="afd6d-112"><span id="ch"></span><span id="CH"></span>*канал*</span><span class="sxs-lookup"><span data-stu-id="afd6d-112"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="afd6d-113">Символ для сцепления с этой строкой.</span><span class="sxs-lookup"><span data-stu-id="afd6d-113">A character to concatenate to this string.</span></span>

</dd> <dt>

<span data-ttu-id="afd6d-114"><span id="lpsz"></span><span id="LPSZ"></span>*лпсз*</span><span class="sxs-lookup"><span data-stu-id="afd6d-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="afd6d-115">Указатель на строку **,** завершающуюся нулем, для сцепления с этой строкой.</span><span class="sxs-lookup"><span data-stu-id="afd6d-115">Pointer to a **NULL**-terminated string to concatenate to this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afd6d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afd6d-116">Remarks</span></span>

<span data-ttu-id="afd6d-117">Имейте в виду, что при использовании этого оператора объединения могут возникать исключения памяти, так как для символов, добавляемых в этот объект [**чстринг**](chstring.md) , может быть выделено новое хранилище.</span><span class="sxs-lookup"><span data-stu-id="afd6d-117">Be aware that memory exceptions can occur whenever you use this concatenation operator because new storage may be allocated for characters added to this [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="afd6d-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="afd6d-118">Examples</span></span>

<span data-ttu-id="afd6d-119">В следующем примере показано использование **чстринг:: operator + =**:</span><span class="sxs-lookup"><span data-stu-id="afd6d-119">The following example shows the use of **CHString::operator +=**:</span></span>


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a><span data-ttu-id="afd6d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="afd6d-120">Requirements</span></span>



| <span data-ttu-id="afd6d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="afd6d-121">Requirement</span></span> | <span data-ttu-id="afd6d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="afd6d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afd6d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afd6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="afd6d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afd6d-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="afd6d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afd6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="afd6d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afd6d-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="afd6d-127">Header</span><span class="sxs-lookup"><span data-stu-id="afd6d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="afd6d-128"><dt>Чстринг. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afd6d-128"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="afd6d-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="afd6d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="afd6d-130"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afd6d-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="afd6d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="afd6d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afd6d-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afd6d-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afd6d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afd6d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd6d-134">**чстринг**</span><span class="sxs-lookup"><span data-stu-id="afd6d-134">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

