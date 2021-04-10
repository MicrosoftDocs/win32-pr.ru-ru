---
description: '\_ \_ \_ Escape-структура ресурса мксдк S0PAGE \_ представляет собой структуру t мксдк ~, \_ \_ \_ объединенную с \_ структурой мксдк XPS \_ S0PAGE \_ Resource \_ t.'
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: Структура MXDC_S0PAGE_RESOURCE_ESCAPE_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264449"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a><span data-ttu-id="7e09a-103">\_ \_ Структура переключения ресурсов мксдк S0PAGE \_ \_ T</span><span class="sxs-lookup"><span data-stu-id="7e09a-103">MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T structure</span></span>

<span data-ttu-id="7e09a-104">Escape-структура **\_ \_ ресурса \_ мксдк \_ S0PAGE** представляет собой структуру [**\_ \_ \_ t мксдк**](mxdcescapeheader.md) ~, объединенную с структурой [**мксдк \_ XPS \_ S0PAGE \_ Resource \_ t**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="7e09a-104">The **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e09a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e09a-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="7e09a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7e09a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e09a-107">**мксдцескапе**</span><span class="sxs-lookup"><span data-stu-id="7e09a-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="7e09a-108">Структура [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) с набором элементов **opcode** , равным мксдкоп \_ Set \_ S0PAGE \_ Resource.</span><span class="sxs-lookup"><span data-stu-id="7e09a-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_SET\_S0PAGE\_RESOURCE.</span></span>

</dd> <dt>

<span data-ttu-id="7e09a-109">**xpsS0PageResourcePassthrough**</span><span class="sxs-lookup"><span data-stu-id="7e09a-109">**xpsS0PageResourcePassthrough**</span></span>
</dt> <dd>

<span data-ttu-id="7e09a-110">Структура [**мксдк \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) , представляющая ресурс, например шрифт или файл изображения, на странице документа XPS.</span><span class="sxs-lookup"><span data-stu-id="7e09a-110">An [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure representing a resource, such as a font or image file, on an XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e09a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e09a-111">Remarks</span></span>

<span data-ttu-id="7e09a-112">Эта структура передается в параметре *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , когда эта функция вызывается с помощью escape-экранирования [**Мксдк \_**](mxdc-escape.md) , а элемент **кода операции** в структуре [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) — **мксдкоп \_ Set \_ S0PAGE \_ Resource**.</span><span class="sxs-lookup"><span data-stu-id="7e09a-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape, and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE\_RESOURCE**.</span></span> <span data-ttu-id="7e09a-113">Результатом является ресурс страницы для отправки в МКСДК.</span><span class="sxs-lookup"><span data-stu-id="7e09a-113">The result is a page resource to send to the MXDC.</span></span>

<span data-ttu-id="7e09a-114">Выделите память для экранирования, как показано ниже, задайте необходимые поля, а затем вызовите [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="7e09a-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="7e09a-115">Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен быть между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Однако между вызовами **StartPage** и **EndPage** может быть больше одного из этих вызовов.</span><span class="sxs-lookup"><span data-stu-id="7e09a-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however, there can be more than one of these calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="7e09a-116">Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с **кодом операции** **\_ \_ S0PAGE \_ ресурса мксдкоп Set** для каждого ресурса на странице перед вызовом **екстескапе** с **мксдкоп \_ Set \_ S0PAGE\*\*\*\*.**  </span><span class="sxs-lookup"><span data-stu-id="7e09a-116">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE**  **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e09a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7e09a-117">Requirements</span></span>



| <span data-ttu-id="7e09a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7e09a-118">Requirement</span></span> | <span data-ttu-id="7e09a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7e09a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7e09a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e09a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7e09a-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e09a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7e09a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e09a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7e09a-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7e09a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7e09a-124">Header</span><span class="sxs-lookup"><span data-stu-id="7e09a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e09a-125"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e09a-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e09a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e09a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e09a-127">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="7e09a-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7e09a-128">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="7e09a-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="7e09a-129">[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e09a-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7e09a-130">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="7e09a-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="7e09a-131">**Escape-МКСДК \_**</span><span class="sxs-lookup"><span data-stu-id="7e09a-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

