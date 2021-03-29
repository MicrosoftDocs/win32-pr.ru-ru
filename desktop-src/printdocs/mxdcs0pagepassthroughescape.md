---
description: МКСДК \_ S0PAGE \_ сквозная \_ \_ Структура t представляет собой структуру escape-последовательности мксдк \_ t, \_ \_ объединенную с \_ структурой мксдк S0PAGE \_ Data \_ t.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: Структура MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346485"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a><span data-ttu-id="a0117-103">МКСДК \_ S0PAGE \_ сквозная \_ Escape- \_ Структура T</span><span class="sxs-lookup"><span data-stu-id="a0117-103">MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T structure</span></span>

<span data-ttu-id="a0117-104">**Мксдк \_ S0PAGE \_ сквозная \_ Структура \_ t** представляет собой структуру [**escape-последовательности мксдк \_ \_ \_ t**](mxdcescapeheader.md) , объединенную с структурой [**мксдк \_ S0PAGE \_ Data \_ t**](mxdcs0pagedata.md) .</span><span class="sxs-lookup"><span data-stu-id="a0117-104">The **MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_S0PAGE\_DATA\_T**](mxdcs0pagedata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0117-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0117-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="a0117-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a0117-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0117-107">**мксдцескапе**</span><span class="sxs-lookup"><span data-stu-id="a0117-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="a0117-108">Структура [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) с набором элементов **opcode** , равным **мксдкоп \_ Set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="a0117-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to **MXDCOP\_SET\_S0PAGE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0117-109">**xpsS0PageData**</span><span class="sxs-lookup"><span data-stu-id="a0117-109">**xpsS0PageData**</span></span>
</dt> <dd>

<span data-ttu-id="a0117-110">Структура [**MxdcS0PageData**](mxdcs0pagedata.md) , представляющая страницу XPS-документа.</span><span class="sxs-lookup"><span data-stu-id="a0117-110">An [**MxdcS0PageData**](mxdcs0pagedata.md) structure that represents an XPS-document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0117-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0117-111">Remarks</span></span>

<span data-ttu-id="a0117-112">Эта структура передается в параметре *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) при вызове с помощью escape-escape-последовательности [**Мксдк \_**](mxdc-escape.md) , а элемент **кода операции** в структуре мксдк в виде заголовка в виде [**\_ \_ \_ T**](mxdcescapeheader.md) — **мксдкоп \_ Set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="a0117-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE**.</span></span> <span data-ttu-id="a0117-113">В результате конвертер XML-документов Microsoft (МКСДК) передает страницу на принтер, не обрабатывая его.</span><span class="sxs-lookup"><span data-stu-id="a0117-113">The result is that the Microsoft XML Document Converter (MXDC) passes the page through to the printer without processing it.</span></span>

<span data-ttu-id="a0117-114">Выделите память для экранирования, как показано ниже, задайте необходимые поля, а затем вызовите [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="a0117-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="a0117-115">Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен быть между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="a0117-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="a0117-116">Вызывающее приложение отвечает за проверку XML страницы документа XPS.</span><span class="sxs-lookup"><span data-stu-id="a0117-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="a0117-117">Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с **мксдкоп \_ Set \_ S0PAGE \_ Resource** как **код операции** для каждого ресурса на странице, прежде чем вызывать его с **мксдкоп \_ Set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="a0117-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0117-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a0117-118">Requirements</span></span>



| <span data-ttu-id="a0117-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a0117-119">Requirement</span></span> | <span data-ttu-id="a0117-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a0117-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a0117-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0117-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0117-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0117-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0117-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0117-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0117-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0117-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a0117-125">Header</span><span class="sxs-lookup"><span data-stu-id="a0117-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0117-126"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0117-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0117-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0117-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0117-128">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="a0117-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a0117-129">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="a0117-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="a0117-130">[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0117-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a0117-131">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="a0117-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="a0117-132">**Escape-МКСДК \_**</span><span class="sxs-lookup"><span data-stu-id="a0117-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

