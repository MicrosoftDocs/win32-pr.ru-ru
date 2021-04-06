---
description: '\_ \_ Структура данных мксдк S0PAGE \_ содержит страницу документа XPS, которая передается в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.'
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: Структура MXDC_S0PAGE_DATA_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815345"
---
# <a name="mxdc_s0page_data_t-structure"></a><span data-ttu-id="e477e-103">\_ \_ Структура T мксдк данных S0PAGE \_</span><span class="sxs-lookup"><span data-stu-id="e477e-103">MXDC\_S0PAGE\_DATA\_T structure</span></span>

<span data-ttu-id="e477e-104">Структура **\_ данных мксдк \_ S0PAGE \_** содержит страницу документа XPS, которая передается в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.</span><span class="sxs-lookup"><span data-stu-id="e477e-104">The **MXDC\_S0PAGE\_DATA\_T** structure holds an XPS document page to be passed to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e477e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e477e-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a><span data-ttu-id="e477e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e477e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e477e-107">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="e477e-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="e477e-108">Размер выходного буфера **бдата**.</span><span class="sxs-lookup"><span data-stu-id="e477e-108">The size of the output buffer, **bData**.</span></span>

</dd> <dt>

<span data-ttu-id="e477e-109">**бдата**</span><span class="sxs-lookup"><span data-stu-id="e477e-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="e477e-110">Страница документа XPS.</span><span class="sxs-lookup"><span data-stu-id="e477e-110">The XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e477e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e477e-111">Remarks</span></span>

<span data-ttu-id="e477e-112">Эта структура добавляется в структуру [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) (для которой в качестве **кода операции** задано значение Мксдкоп \_ Set \_ S0PAGE), чтобы сделать [**мксдк \_ S0PAGE \_ сквозной \_ Escape \_**](mxdcs0pagepassthroughescape.md) -структурой t.</span><span class="sxs-lookup"><span data-stu-id="e477e-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (which has its **opCode** set to MXDCOP\_SET\_S0PAGE) to make an [**MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T**](mxdcs0pagepassthroughescape.md) structure.</span></span> <span data-ttu-id="e477e-113">Эта структура затем передается в параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) при вызове с помощью escape- [**\_ последовательности мксдк**](mxdc-escape.md) в качестве экранирования.</span><span class="sxs-lookup"><span data-stu-id="e477e-113">That structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with [**MXDC\_ESCAPE**](mxdc-escape.md) as the escape.</span></span> <span data-ttu-id="e477e-114">В результате МКСДК передает страницу в выходные данные без ее обработки.</span><span class="sxs-lookup"><span data-stu-id="e477e-114">The result is that the MXDC passes the page through to the output without processing it.</span></span>

<span data-ttu-id="e477e-115">Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен быть между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="e477e-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="e477e-116">Вызывающее приложение отвечает за проверку XML страницы документа XPS.</span><span class="sxs-lookup"><span data-stu-id="e477e-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="e477e-117">Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с **мксдкоп \_ Set \_ S0PAGE \_ Resource** как **код операции** для каждого ресурса на странице, прежде чем вызывать его с **мксдкоп \_ Set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="e477e-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e477e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e477e-118">Requirements</span></span>



| <span data-ttu-id="e477e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e477e-119">Requirement</span></span> | <span data-ttu-id="e477e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e477e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e477e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e477e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e477e-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e477e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e477e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e477e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e477e-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e477e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e477e-125">Header</span><span class="sxs-lookup"><span data-stu-id="e477e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e477e-126"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="e477e-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e477e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e477e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e477e-128">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="e477e-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e477e-129">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="e477e-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="e477e-130">[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e477e-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e477e-131">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="e477e-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="e477e-132">**Escape-МКСДК \_**</span><span class="sxs-lookup"><span data-stu-id="e477e-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

