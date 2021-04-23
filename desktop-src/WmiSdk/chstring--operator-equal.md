---
description: Оператор присваивания Чстринг (=) повторно инициализирует существующий объект Чстринг новыми данными.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'Чстринг:: operator = (Чстринг. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080896"
---
# <a name="chstringoperator"></a><span data-ttu-id="e31e7-103">Чстринг:: operator =</span><span class="sxs-lookup"><span data-stu-id="e31e7-103">CHString::operator=</span></span>

<span data-ttu-id="e31e7-104">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="e31e7-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="e31e7-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="e31e7-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="e31e7-106">Оператор присваивания [**чстринг**](chstring.md) (=) повторно инициализирует существующий объект чстринг новыми данными.</span><span class="sxs-lookup"><span data-stu-id="e31e7-106">The [**CHString**](chstring.md) assignment (=) operator reinitializes an existing CHString object with new data.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="e31e7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e31e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31e7-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*стрингсрк*, *p*</span><span class="sxs-lookup"><span data-stu-id="e31e7-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span></span>
</dt> <dd>

<span data-ttu-id="e31e7-109">Присваивает [**чстринг**](chstring.md) строку этому объекту.</span><span class="sxs-lookup"><span data-stu-id="e31e7-109">Assigns a [**CHString**](chstring.md) string to this object.</span></span>

</dd> <dt>

<span data-ttu-id="e31e7-110"><span id="ch"></span><span id="CH"></span>*канал*</span><span class="sxs-lookup"><span data-stu-id="e31e7-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="e31e7-111">Присваивает символ этому объекту.</span><span class="sxs-lookup"><span data-stu-id="e31e7-111">Assigns a character to this object.</span></span>

</dd> <dt>

<span data-ttu-id="e31e7-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*лпсз*, *ПСЗ*</span><span class="sxs-lookup"><span data-stu-id="e31e7-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*</span></span>
</dt> <dd>

<span data-ttu-id="e31e7-113">Присваивает этому объекту **строку, завершающуюся нулем.**</span><span class="sxs-lookup"><span data-stu-id="e31e7-113">Assigns a **NULL**-terminated string to this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e31e7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e31e7-114">Remarks</span></span>

<span data-ttu-id="e31e7-115">Если строка назначения (то есть левая часть) уже достаточно велика для хранения новых данных, выделение памяти не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e31e7-115">If the destination string (that is, the left side) is already large enough to store the new data, no new memory allocation is performed.</span></span> <span data-ttu-id="e31e7-116">Однако исключения памяти могут возникать при каждом использовании оператора присваивания, поскольку для хранения результирующего объекта [**чстринг**](chstring.md) часто выделяется новое хранилище.</span><span class="sxs-lookup"><span data-stu-id="e31e7-116">However, memory exceptions can occur whenever you use the assignment operator because new storage is often allocated to hold the resulting [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="e31e7-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="e31e7-117">Examples</span></span>

<span data-ttu-id="e31e7-118">В следующем примере кода показано использование **чстринг:: operator =**:</span><span class="sxs-lookup"><span data-stu-id="e31e7-118">The following code example shows the use of **CHString::operator =**:</span></span>


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a><span data-ttu-id="e31e7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e31e7-119">Requirements</span></span>



| <span data-ttu-id="e31e7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e31e7-120">Requirement</span></span> | <span data-ttu-id="e31e7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e31e7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31e7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e31e7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e31e7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e31e7-123">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e31e7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e31e7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e31e7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e31e7-125">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e31e7-126">Header</span><span class="sxs-lookup"><span data-stu-id="e31e7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e31e7-127"><dt>Чстринг. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-127"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e31e7-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e31e7-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="e31e7-129"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-129"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="e31e7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e31e7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e31e7-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31e7-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e31e7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31e7-133">**чстринг**</span><span class="sxs-lookup"><span data-stu-id="e31e7-133">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

