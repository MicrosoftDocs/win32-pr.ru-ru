---
title: Структура STOWED_EXCEPTION_INFORMATION_HEADER
description: Содержит сведения, определяющие родительскую структуру.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER структуры отчеты об ошибках Windows
- PSTOWED_EXCEPTION_INFORMATION_HEADER отчеты об ошибках Windows указателя на структуру
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071932"
---
# <a name="stowed_exception_information_header-structure"></a><span data-ttu-id="8fbf3-105">\_ \_ Структура заголовка сведений об ИСКЛЮЧЕНии заполнения \_</span><span class="sxs-lookup"><span data-stu-id="8fbf3-105">STOWED\_EXCEPTION\_INFORMATION\_HEADER structure</span></span>

<span data-ttu-id="8fbf3-106">Содержит сведения, определяющие родительскую структуру.</span><span class="sxs-lookup"><span data-stu-id="8fbf3-106">Contains info that identifies the parent structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbf3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fbf3-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a><span data-ttu-id="8fbf3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8fbf3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8fbf3-109">**Размер**</span><span class="sxs-lookup"><span data-stu-id="8fbf3-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="8fbf3-110">Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8fbf3-110">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8fbf3-111">Размер родительской структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="8fbf3-111">Size, in bytes, of the parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="8fbf3-112">**Образец**</span><span class="sxs-lookup"><span data-stu-id="8fbf3-112">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="8fbf3-113">Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8fbf3-113">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8fbf3-114">32-разрядное значение, указывающее сигнатуру родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="8fbf3-114">A 32-bit value that specifies the signature of the parent structure.</span></span>



| <span data-ttu-id="8fbf3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbf3-115">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="8fbf3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbf3-116">Meaning</span></span>                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <span data-ttu-id="8fbf3-117"><dt>**Заполнения \_ \_Сведения об исключении \_ v1, \_ подпись**</dt> <dt>"SE01"</dt></span><span class="sxs-lookup"><span data-stu-id="8fbf3-117"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V1\_SIGNATURE**</dt> <dt>'SE01'</dt></span></span> </dl> | <span data-ttu-id="8fbf3-118">Это значение указывает, что родительским объектом является структура **заполнения \_ исключения \_ \_ v1** .</span><span class="sxs-lookup"><span data-stu-id="8fbf3-118">This value indicates that the parent is a **STOWED\_EXCEPTION\_INFORMATION\_V1** structure.</span></span><br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <span data-ttu-id="8fbf3-119"><dt>**Заполнения \_ \_Сведения об исключении \_ v2 \_ сигнатура**</dt> <dt>"SE02"</dt></span><span class="sxs-lookup"><span data-stu-id="8fbf3-119"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V2\_SIGNATURE**</dt> <dt>'SE02'</dt></span></span> </dl> | <span data-ttu-id="8fbf3-120">Это значение указывает, что родительским объектом является структура [**заполнения \_ исключения \_ \_ v2**](stowed-exception-information-v2.md) .</span><span class="sxs-lookup"><span data-stu-id="8fbf3-120">This value indicates that the parent is a [**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) structure.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fbf3-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fbf3-121">Remarks</span></span>

<span data-ttu-id="8fbf3-122">[**Заполнения \_ Заголовок сведений об ИСКЛЮЧЕНии \_ \_ v2**](stowed-exception-information-v2.md) и заполнения в настоящее время не определен в заголовке, который является общедоступным, поэтому необходимо определить их в исходном коде, прежде чем использовать их. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fbf3-122">[**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) and **STOWED\_EXCEPTION\_INFORMATION\_HEADER** currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="8fbf3-123">Структура **\_ \_ сведений об исключении \_ заполнения** версии 1 идентична этой структуре, за исключением того, что она не содержит членов **нестедексцептионтипе** и **нестедексцептион** .</span><span class="sxs-lookup"><span data-stu-id="8fbf3-123">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fbf3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8fbf3-124">Requirements</span></span>



| <span data-ttu-id="8fbf3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8fbf3-125">Requirement</span></span> | <span data-ttu-id="8fbf3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbf3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8fbf3-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fbf3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbf3-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8fbf3-128">Windows 8 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8fbf3-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fbf3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbf3-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8fbf3-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8fbf3-131">Header</span><span class="sxs-lookup"><span data-stu-id="8fbf3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fbf3-132"><dt>Нет</dt></span><span class="sxs-lookup"><span data-stu-id="8fbf3-132"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fbf3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fbf3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbf3-134">**\_Сведения об исключении заполнения \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="8fbf3-134">**STOWED\_EXCEPTION\_INFORMATION\_V2**</span></span>](stowed-exception-information-v2.md)
</dt> </dl>

 

