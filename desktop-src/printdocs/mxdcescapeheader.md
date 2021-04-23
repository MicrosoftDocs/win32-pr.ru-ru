---
description: Структура МКСДК \_ Escape- \_ заголовка \_ T содержит код операции для вызова екстескапе с escape-мксдк в \_ качестве параметра нескапе. Он также предоставляет размеры входных и выходных буферов.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: Структура MXDC_ESCAPE_HEADER_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913147"
---
# <a name="mxdc_escape_header_t-structure"></a><span data-ttu-id="0fd9f-104">МКСДК \_ T-структура Escape- \_ заголовка \_</span><span class="sxs-lookup"><span data-stu-id="0fd9f-104">MXDC\_ESCAPE\_HEADER\_T structure</span></span>

<span data-ttu-id="0fd9f-105">Структура **мксдк \_ Escape \_ -заголовка \_ T** содержит код операции для вызова [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с [**\_ escape-мксдк**](mxdc-escape.md) в качестве параметра *нескапе* .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-105">The **MXDC\_ESCAPE\_HEADER\_T** structure holds the operation code for a call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with [**MXDC\_ESCAPE**](mxdc-escape.md) as the *nEscape* parameter.</span></span> <span data-ttu-id="0fd9f-106">Он также предоставляет размеры входных и выходных буферов.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-106">It also provides the sizes of the input and output buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd9f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fd9f-107">Syntax</span></span>


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a><span data-ttu-id="0fd9f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0fd9f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0fd9f-109">**кбинпут**</span><span class="sxs-lookup"><span data-stu-id="0fd9f-109">**cbInput**</span></span>
</dt> <dd>

<span data-ttu-id="0fd9f-110">Размер входного буфера, который будет передан в параметр *лпсзаутдата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-110">The size of the input buffer that will be passed to the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="0fd9f-111">**кбаутпут**</span><span class="sxs-lookup"><span data-stu-id="0fd9f-111">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="0fd9f-112">Размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-112">The size of the output buffer.</span></span> <span data-ttu-id="0fd9f-113">Это то же значение, что и параметр *кбаутпут* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-113">This is the same value as the *cbOutput* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="0fd9f-114">**транслируют**</span><span class="sxs-lookup"><span data-stu-id="0fd9f-114">**opCode**</span></span>
</dt> <dd>

<span data-ttu-id="0fd9f-115">Константа кода, которая сообщает МКСДК, что делать.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-115">The code constant that tells MXDC what to do.</span></span>



| <span data-ttu-id="0fd9f-116">Код операции</span><span class="sxs-lookup"><span data-stu-id="0fd9f-116">Operations code</span></span>                      | <span data-ttu-id="0fd9f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0fd9f-117">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd9f-118">МКСДКОП \_ получить \_ имя файла</span><span class="sxs-lookup"><span data-stu-id="0fd9f-118">MXDCOP\_GET\_FILENAME</span></span>                | <span data-ttu-id="0fd9f-119">Возвращает, в параметре *лпсзаутдата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) либо полный путь к выходному файлу в виде строки, завершающейся нулем, либо размер этой строки.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-119">Returns, in the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function, either the full path of the output file as a zero-terminated string or the size of that string.</span></span> <span data-ttu-id="0fd9f-120">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-120">See Remarks.</span></span>                   |
| <span data-ttu-id="0fd9f-121">\_ \_ фиксированная \_ последовательность документов мксдкоп PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="0fd9f-121">MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ</span></span> | <span data-ttu-id="0fd9f-122">Связывает билет на печать с фиксированной последовательностью документов XPS.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-122">Associates a print ticket with an XPS fixed document sequence.</span></span>                                                                                                                                                         |
| <span data-ttu-id="0fd9f-123">\_ \_ фиксированный документ мксдкоп PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="0fd9f-123">MXDCOP\_PRINTTICKET\_FIXED\_DOC</span></span>      | <span data-ttu-id="0fd9f-124">Связывает билет печати с документом XPS.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-124">Associates a print ticket with an XPS document.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="0fd9f-125">\_ \_ фиксированная страница мксдкоп PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="0fd9f-125">MXDCOP\_PRINTTICKET\_FIXED\_PAGE</span></span>     | <span data-ttu-id="0fd9f-126">Связывает билет на печать со страницей XPS.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-126">Associates a print ticket with an XPS page.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="0fd9f-127">МКСДКОП \_ Set \_ S0PAGE</span><span class="sxs-lookup"><span data-stu-id="0fd9f-127">MXDCOP\_SET\_S0PAGE</span></span>                  | <span data-ttu-id="0fd9f-128">Отправляет в выходные данные разметку XPS текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-128">Sends the XPS markup of the current page to the output.</span></span>                                                                                                                                                                |
| <span data-ttu-id="0fd9f-129">МКСДКОП \_ задать \_ S0PAGE \_ ресурс</span><span class="sxs-lookup"><span data-stu-id="0fd9f-129">MXDCOP\_SET\_S0PAGE\_RESOURCE</span></span>        | <span data-ttu-id="0fd9f-130">Отправляет на выход на страницу ресурс, например изображение или шрифт.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-130">Sends a resource on the page, such as an image or font, to the output.</span></span>                                                                                                                                                 |
| <span data-ttu-id="0fd9f-131">МКСДКОП \_ Set \_ кспспасссру \_ mode</span><span class="sxs-lookup"><span data-stu-id="0fd9f-131">MXDCOP\_SET\_XPSPASSTHRU\_MODE</span></span>       | <span data-ttu-id="0fd9f-132">Помещает МКСДК в сквозное состояние, позволяя приложению записывать XPS непосредственно в выходной файл без какой-либо обработки МКСДК.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-132">Puts the MXDC into a pass-through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="0fd9f-133">Таким образом может быть написан весь документ или даже последовательность документов.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-133">An entire document or even document sequence can be written in this way.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fd9f-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fd9f-134">Remarks</span></span>

<span data-ttu-id="0fd9f-135">Перед вызовом [**\_ escape-последовательности мксдк**](mxdc-escape.md) \_ приложения должны сначала проверить, является ли драйвер Мксдк, вызвав [**ЕКСТЕСКАПЕ**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с помощью escape- [**технологии**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-135">Before calling [**MXDC\_ESCAPE**](mxdc-escape.md),\_applications should first verify that the driver is MXDC by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="0fd9f-136">Если драйвер является МКСДК, функция возвращает строку "", завершающуюся нулем http://schemas.microsoft.com/xps/2005/06 .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-136">If the driver is the MXDC the function returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06".</span></span>

<span data-ttu-id="0fd9f-137">Эта структура всегда находится в начале данных, передаваемых функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) в его параметре *лпсзиндата* .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-137">This structure is always at the beginning of the data passed to the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function in its *lpszInData* parameter.</span></span>

<span data-ttu-id="0fd9f-138">Когда **код операции** -мксдкоп \_ получает \_ имя файла:</span><span class="sxs-lookup"><span data-stu-id="0fd9f-138">When **opCode** is MXDCOP\_GET\_FILENAME:</span></span>

-   <span data-ttu-id="0fd9f-139">Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит только из структуры **escape-заголовка мксдк \_ \_ \_ T** .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-139">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="0fd9f-140">Получите выходное имя файла, вызвав [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) дважды.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-140">Obtain the output filename by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) twice.</span></span>
    1.  <span data-ttu-id="0fd9f-141">В первый раз передайте 4 параметру *Кбаутпут* [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="0fd9f-141">The first time, pass 4 to the *cbOutput* parameter of [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="0fd9f-142">Задайте параметр *лпсзаутдата* , чтобы он указывал на любой выделенный 4 байта памяти.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-142">Set the *lpszOutData* parameter to point to any allocated 4 bytes of memory.</span></span> <span data-ttu-id="0fd9f-143">Размер полного пути к файлу будет возвращен в параметре *лпсзаутдата* объекта **екстескапе**.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-143">The size of the fully qualified file path will be returned in the *lpszOutData* parameter of **ExtEscape**.</span></span>
    2.  <span data-ttu-id="0fd9f-144">Затем вызовите функцию еще раз.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-144">Then call the function again.</span></span> <span data-ttu-id="0fd9f-145">На этот раз оба параметра *кбаутпут* и *кбинпут* заданы как 4 + *DataSize*.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-145">This time set both *cbOutput* and *cbInput* to 4+ *DataSize*.</span></span> <span data-ttu-id="0fd9f-146">Полный путь к файлу будет возвращен в структуре [**мксдкжетфиленамедата**](mxdcgetfilenamedata.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-146">The fully qualified file path will be returned in an [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) structure.</span></span>

<span data-ttu-id="0fd9f-147">Если **код операции** — мксдкоп \_ PrintTicket \_ фиксированный \_ документ \_ Seq или мксдкоп \_ PrintTicket \_ фиксированный \_ документ:</span><span class="sxs-lookup"><span data-stu-id="0fd9f-147">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ or MXDCOP\_PRINTTICKET\_FIXED\_DOC:</span></span>

-   <span data-ttu-id="0fd9f-148">Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит из структуры **escape-заголовка мксдк \_ \_ \_ T** и структуры [**мксдкпринттиккетпасссраугх**](mxdcprintticketpassthrough.md) , Объединенной в структуру [**мксдкпринттиккетескапе**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-148">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="0fd9f-149">Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) и вызовом [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="0fd9f-149">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="0fd9f-150">Если **код операции** — \_ это \_ фиксированная страница мксдкоп PRINTTICKET \_ :</span><span class="sxs-lookup"><span data-stu-id="0fd9f-150">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_PAGE:</span></span>

-   <span data-ttu-id="0fd9f-151">Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит из структуры **escape-заголовка мксдк \_ \_ \_ T** и структуры [**мксдкпринттиккетпасссраугх**](mxdcprintticketpassthrough.md) , Объединенной в структуру [**мксдкпринттиккетескапе**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-151">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="0fd9f-152">Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="0fd9f-152">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="0fd9f-153">Когда **код операции** — мксдкоп \_ Set \_ S0PAGE:</span><span class="sxs-lookup"><span data-stu-id="0fd9f-153">When **opCode** is MXDCOP\_SET\_S0PAGE:</span></span>

-   <span data-ttu-id="0fd9f-154">Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит из структуры **escape-заголовка мксдк \_ \_ \_ T** и структуры [**MxdcS0PageData**](mxdcs0pagedata.md) , Объединенной в структуру [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-154">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcS0PageData**](mxdcs0pagedata.md) structure concatenated into an [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) structure.</span></span>
-   <span data-ttu-id="0fd9f-155">Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="0fd9f-155">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>
-   <span data-ttu-id="0fd9f-156">Вызывающее приложение отвечает за проверку XML.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-156">The calling application is responsible for validating the XML.</span></span>
-   <span data-ttu-id="0fd9f-157">Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с мксдкоп \_ Set \_ S0PAGE \_ Resource как **код операции** для каждого ресурса на странице, прежде чем вызывать его с мксдкоп \_ Set \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-157">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="0fd9f-158">Если **код операции** — мксдкоп \_ Set \_ S0PAGE \_ Resource:</span><span class="sxs-lookup"><span data-stu-id="0fd9f-158">When **opCode** is MXDCOP\_SET\_S0PAGE\_RESOURCE:</span></span>

-   <span data-ttu-id="0fd9f-159">Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит из структуры **escape-заголовка мксдк \_ \_ \_ T** и структуры [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) , Объединенной в структуру [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-159">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) structure concatenated into an [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) structure.</span></span>
-   <span data-ttu-id="0fd9f-160">Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), но между вызовами **StartPage** и **EndPage** может быть несколько таких вызовов.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-160">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), but there can be multiple such calls between the **StartPage** and **EndPage** calls.</span></span>
-   <span data-ttu-id="0fd9f-161">Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с мксдкоп \_ Set \_ S0PAGE \_ Resource как **код операции** для каждого ресурса на странице, прежде чем вызывать его с мксдкоп \_ Set \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-161">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="0fd9f-162">Когда **код операции** — мксдкоп \_ Set \_ кспспасссру \_ mode:</span><span class="sxs-lookup"><span data-stu-id="0fd9f-162">When **opCode** is MXDCOP\_SET\_XPSPASSTHRU\_MODE:</span></span>

-   <span data-ttu-id="0fd9f-163">Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит только из структуры **escape-заголовка мксдк \_ \_ \_ T** .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-163">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="0fd9f-164">Этот вызов должен быть выполнен до вызова [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span><span class="sxs-lookup"><span data-stu-id="0fd9f-164">This call must occur before the call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd9f-165">Требования</span><span class="sxs-lookup"><span data-stu-id="0fd9f-165">Requirements</span></span>



| <span data-ttu-id="0fd9f-166">Требование</span><span class="sxs-lookup"><span data-stu-id="0fd9f-166">Requirement</span></span> | <span data-ttu-id="0fd9f-167">Значение</span><span class="sxs-lookup"><span data-stu-id="0fd9f-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0fd9f-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fd9f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd9f-169">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fd9f-169">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0fd9f-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fd9f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd9f-171">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0fd9f-171">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0fd9f-172">Header</span><span class="sxs-lookup"><span data-stu-id="0fd9f-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd9f-173"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd9f-173"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd9f-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fd9f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd9f-175">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="0fd9f-175">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0fd9f-176">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="0fd9f-176">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="0fd9f-177">[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fd9f-177">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0fd9f-178">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="0fd9f-178">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="0fd9f-179">**Escape-МКСДК \_**</span><span class="sxs-lookup"><span data-stu-id="0fd9f-179">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

