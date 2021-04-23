---
description: '\_ \_ Структура escape-последовательности мксдк PRINTTICKET \_ t представляет собой мксдкную структуру \_ \_ заголовка \_ t, объединяющую \_ структуру данных мксдк PrintTicket \_ \_ t.'
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: Структура MXDC_PRINTTICKET_ESCAPE_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651142"
---
# <a name="mxdc_printticket_escape_t-structure"></a><span data-ttu-id="29bc5-103">\_ \_ Структура Escape- \_ T мксдк PRINTTICKET</span><span class="sxs-lookup"><span data-stu-id="29bc5-103">MXDC\_PRINTTICKET\_ESCAPE\_T structure</span></span>

<span data-ttu-id="29bc5-104">Структура **\_ Escape- \_ последовательности мксдк PRINTTICKET \_ t** представляет собой [**мксдкную структуру \_ \_ заголовка \_ t**](mxdcescapeheader.md) , объединяющую [**структуру \_ данных мксдк PrintTicket \_ \_ t**](mxdcprintticketpassthrough.md) .</span><span class="sxs-lookup"><span data-stu-id="29bc5-104">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with a [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="29bc5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29bc5-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="29bc5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="29bc5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="29bc5-107">**мксдцескапе**</span><span class="sxs-lookup"><span data-stu-id="29bc5-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="29bc5-108">Структура [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) с набором элементов **opcode** для мксдкоп \_ \_ фиксированной \_ страницы PrintTicket, \_ \_ фиксированный документ PrintTicket мксдкоп или номер \_ \_ \_ фиксированного документа PrintTicket мксдкоп \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="29bc5-108">A [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_PRINTTICKET\_FIXED\_PAGE, MXDCOP\_PRINTTICKET\_FIXED\_DOC, or MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ.</span></span>

</dd> <dt>

<span data-ttu-id="29bc5-109">**принттиккетдата**</span><span class="sxs-lookup"><span data-stu-id="29bc5-109">**printTicketData**</span></span>
</dt> <dd>

<span data-ttu-id="29bc5-110">Структура [**\_ данных мксдк \_ PRINTTICKET \_ T**](mxdcprintticketpassthrough.md) , содержащая билет на печать.</span><span class="sxs-lookup"><span data-stu-id="29bc5-110">A [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure containing the print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29bc5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29bc5-111">Remarks</span></span>

<span data-ttu-id="29bc5-112">Эта структура передается в параметре *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , когда эта функция вызывается с помощью escape **\_ \_ \_ -** экранирования [**мксдк \_**](mxdc-escape.md) , а элемент **кода операции** в структуре [**Escape- \_ \_ заголовка \_ мксдк**](mxdcescapeheader.md) — мксдкоп, фиксированный **\_ \_ \_ документ PrintTicket** или **мксдкоп \_ PrintTicket \_ fixed \_ doc \_ Seq**.</span><span class="sxs-lookup"><span data-stu-id="29bc5-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**.</span></span> <span data-ttu-id="29bc5-113">В результате записывается билет на печать в файл документа XPS.</span><span class="sxs-lookup"><span data-stu-id="29bc5-113">The result is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="29bc5-114">Выделите память для экранирования, как показано ниже, задайте необходимые поля, а затем вызовите [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="29bc5-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="29bc5-115">Если для **кода операции** задана **\_ \_ фиксированная \_ страница мксдкоп PRINTTICKET**, вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="29bc5-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="29bc5-116">Если для **кода операции** задано значение фиксированного **\_ \_ \_ документа мксдкоп PrintTicket** или **мксдкоп \_ PrintTicket \_ \_ \_**, то вызов **екстескапе** должен осуществляться между вызовом [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) и вызовом [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="29bc5-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="29bc5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="29bc5-117">Requirements</span></span>



| <span data-ttu-id="29bc5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="29bc5-118">Requirement</span></span> | <span data-ttu-id="29bc5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="29bc5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="29bc5-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29bc5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="29bc5-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29bc5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29bc5-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29bc5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="29bc5-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29bc5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="29bc5-124">Header</span><span class="sxs-lookup"><span data-stu-id="29bc5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="29bc5-125"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="29bc5-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29bc5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29bc5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29bc5-127">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="29bc5-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="29bc5-128">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="29bc5-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="29bc5-129">[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29bc5-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="29bc5-130">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="29bc5-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="29bc5-131">**Escape-МКСДК \_**</span><span class="sxs-lookup"><span data-stu-id="29bc5-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

