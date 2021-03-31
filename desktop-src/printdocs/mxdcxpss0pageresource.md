---
description: Структура МКСДК \_ XPS \_ S0PAGE \_ Resource \_ T содержит сведения о ресурсе, например изображение или шрифт, который связан со страницей документа XPS и передается в выходной файл конвертера документов Microsoft XPS (мксдк).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: Структура MXDC_XPS_S0PAGE_RESOURCE_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910488"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a><span data-ttu-id="1ad83-103">\_Структура мксдк XPS \_ S0PAGE \_ Resource \_ T</span><span class="sxs-lookup"><span data-stu-id="1ad83-103">MXDC\_XPS\_S0PAGE\_RESOURCE\_T structure</span></span>

<span data-ttu-id="1ad83-104">Структура **мксдк \_ XPS \_ S0PAGE \_ Resource \_ T** содержит сведения о ресурсе, например изображение или шрифт, который связан со страницей документа XPS и передается в выходной файл конвертера документов Microsoft XPS (мксдк).</span><span class="sxs-lookup"><span data-stu-id="1ad83-104">The **MXDC\_XPS\_S0PAGE\_RESOURCE\_T** structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad83-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ad83-105">Syntax</span></span>


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a><span data-ttu-id="1ad83-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1ad83-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ad83-107">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="1ad83-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="1ad83-108">Общий размер этой структуры и ресурса, на который она указывает.</span><span class="sxs-lookup"><span data-stu-id="1ad83-108">The total size of this structure and the resource to which it points.</span></span>

</dd> <dt>

<span data-ttu-id="1ad83-109">**двресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="1ad83-109">**dwResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="1ad83-110">Значение типа [**мксдк \_ S0 \_ \_ перечисление страниц**](mxdcs0pageenums.md) , указывающее тип ресурса, например изображение TIFF или шрифт TrueType.</span><span class="sxs-lookup"><span data-stu-id="1ad83-110">A value of type [**MXDC\_S0\_PAGE\_ENUMS**](mxdcs0pageenums.md) indicating the type of resource, such as TIFF image or TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="1ad83-111">**сзури**</span><span class="sxs-lookup"><span data-stu-id="1ad83-111">**szUri**</span></span>
</dt> <dd>

<span data-ttu-id="1ad83-112">Универсальный код ресурса (URI) для данного ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ad83-112">The URI of the resource.</span></span> <span data-ttu-id="1ad83-113">Это не может быть более 260 байт.</span><span class="sxs-lookup"><span data-stu-id="1ad83-113">This cannot be more than 260 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1ad83-114">**двдатасизе**</span><span class="sxs-lookup"><span data-stu-id="1ad83-114">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="1ad83-115">Размер ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="1ad83-115">The size of the resource in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1ad83-116">**бдата**</span><span class="sxs-lookup"><span data-stu-id="1ad83-116">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="1ad83-117">Данные ресурса в массиве байтов с размером 1 + Размер ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ad83-117">The data of the resource in an array of bytes with size 1 + the size of the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ad83-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ad83-118">Remarks</span></span>

<span data-ttu-id="1ad83-119">Эта структура добавляется в структуру [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) (для которой в качестве **кода операции** задано значение **мксдкоп \_ Set \_ S0PAGERESOURCE**), чтобы сделать [**мксдк \_ S0PAGE \_ ресурса \_ \_ t**](mxdcs0pageresourceescape.md) -структурой.</span><span class="sxs-lookup"><span data-stu-id="1ad83-119">This structure is appended to a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (that has its **opCode** set to **MXDCOP\_SET\_S0PAGERESOURCE**) to make an [**MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T**](mxdcs0pageresourceescape.md) structure.</span></span> <span data-ttu-id="1ad83-120">Полученная **Структура \_ \_ Escape- \_ последовательности \_ ресурсов мксдк S0PAGE** передается в параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , которая вызывается с помощью escape- [**последовательности \_ мксдк**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad83-120">The resulting **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is then passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function that it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="1ad83-121">Результатом является отправка ресурса в МКСДК для преобразования и его запись в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="1ad83-121">The effect is to send the resource to the MXDC for conversion and to be written to the output file.</span></span>

<span data-ttu-id="1ad83-122">Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен быть между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Однако между вызовами **StartPage** и **EndPage** может быть несколько таких вызовов.</span><span class="sxs-lookup"><span data-stu-id="1ad83-122">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however there can be more than one such calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="1ad83-123">Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с **кодом операции** **\_ \_ S0PAGE \_ ресурса мксдкоп Set** для каждого ресурса на странице перед вызовом **екстескапе** с **мксдкоп \_ Set \_ S0PAGE** **.**</span><span class="sxs-lookup"><span data-stu-id="1ad83-123">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE** **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad83-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1ad83-124">Requirements</span></span>



| <span data-ttu-id="1ad83-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1ad83-125">Requirement</span></span> | <span data-ttu-id="1ad83-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad83-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1ad83-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ad83-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad83-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ad83-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ad83-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ad83-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad83-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ad83-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1ad83-131">Header</span><span class="sxs-lookup"><span data-stu-id="1ad83-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad83-132"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ad83-132"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad83-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ad83-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad83-134">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="1ad83-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1ad83-135">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="1ad83-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="1ad83-136">[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ad83-136">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1ad83-137">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="1ad83-137">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="1ad83-138">**Escape-МКСДК \_**</span><span class="sxs-lookup"><span data-stu-id="1ad83-138">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

