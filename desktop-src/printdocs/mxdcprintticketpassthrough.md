---
description: '\_ \_ Структура данных мксдк PRINTTICKET \_ содержит билет на печать документа XPS, который содержит параметры принтера и печати, для передачи в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.'
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: Структура MXDC_PRINTTICKET_DATA_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909579"
---
# <a name="mxdc_printticket_data_t-structure"></a><span data-ttu-id="ca721-103">\_ \_ Структура T данных мксдк PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="ca721-103">MXDC\_PRINTTICKET\_DATA\_T structure</span></span>

<span data-ttu-id="ca721-104">Структура **\_ данных мксдк \_ PRINTTICKET \_** содержит билет на печать документа XPS, который содержит параметры принтера и печати, для передачи в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.</span><span class="sxs-lookup"><span data-stu-id="ca721-104">The **MXDC\_PRINTTICKET\_DATA\_T** structure holds an XPS document print ticket, which contains printer and print job settings, to pass to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca721-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca721-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a><span data-ttu-id="ca721-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ca721-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca721-107">**двдатасизе**</span><span class="sxs-lookup"><span data-stu-id="ca721-107">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="ca721-108">Размер билета на печать в байтах.</span><span class="sxs-lookup"><span data-stu-id="ca721-108">The size of the print ticket in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ca721-109">**бдата**</span><span class="sxs-lookup"><span data-stu-id="ca721-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="ca721-110">Билет на печать документа XPS.</span><span class="sxs-lookup"><span data-stu-id="ca721-110">The XPS document print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca721-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca721-111">Remarks</span></span>

<span data-ttu-id="ca721-112">Эта структура добавляется в структуру [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) , для которой в качестве элемента **кода операции** задана **\_ \_ фиксированная \_ страница мксдкоп PrintTicket**, **\_ \_ фиксированный \_ документ PrintTicket мксдкоп** или **\_ \_ фиксированная \_ \_ последовательность документов PrintTicket мксдкоп** , чтобы сделать структуру [**мксдк \_ PrintTicket \_ \_ T**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="ca721-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that has the **opCode** member set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ** to make an [**MXDC\_PRINTTICKET\_ESCAPE\_T**](mxdcprintticketescape.md) structure.</span></span> <span data-ttu-id="ca721-113">Затем **Структура \_ \_ Escape- \_ последовательности мксдк PRINTTICKET** передается в параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) при вызове с escape-Escape- [**размксдк \_**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="ca721-113">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="ca721-114">В результате записывается билет на печать в файл документа XPS.</span><span class="sxs-lookup"><span data-stu-id="ca721-114">The effect is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="ca721-115">Если для **кода операции** задана **\_ \_ фиксированная \_ страница мксдкоп PRINTTICKET**, вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="ca721-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="ca721-116">Если для **кода операции** задано значение фиксированного **\_ \_ \_ документа мксдкоп PrintTicket** или **мксдкоп \_ PrintTicket \_ \_ \_**, то вызов **екстескапе** должен осуществляться между вызовом [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) и вызовом [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="ca721-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca721-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ca721-117">Requirements</span></span>



| <span data-ttu-id="ca721-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ca721-118">Requirement</span></span> | <span data-ttu-id="ca721-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ca721-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ca721-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca721-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca721-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca721-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca721-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca721-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca721-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca721-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ca721-124">Header</span><span class="sxs-lookup"><span data-stu-id="ca721-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca721-125"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca721-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca721-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca721-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca721-127">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="ca721-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ca721-128">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="ca721-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="ca721-129">[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca721-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ca721-130">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="ca721-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="ca721-131">**Escape-МКСДК \_**</span><span class="sxs-lookup"><span data-stu-id="ca721-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

