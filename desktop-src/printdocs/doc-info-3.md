---
description: '\_ \_ Структура документа info 3 описывает документ, который будет напечатан.'
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Структура DOC_INFO_3 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711938"
---
# <a name="doc_info_3-structure"></a><span data-ttu-id="7371c-103">\_Структура документа info \_ 3</span><span class="sxs-lookup"><span data-stu-id="7371c-103">DOC\_INFO\_3 structure</span></span>

<span data-ttu-id="7371c-104">Структура **документа \_ info \_ 3** описывает документ, который будет напечатан.</span><span class="sxs-lookup"><span data-stu-id="7371c-104">The **DOC\_INFO\_3** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7371c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7371c-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a><span data-ttu-id="7371c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7371c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7371c-107">**пдокнаме**</span><span class="sxs-lookup"><span data-stu-id="7371c-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="7371c-108">Указатель на строку, завершающуюся нулем, которая указывает имя документа.</span><span class="sxs-lookup"><span data-stu-id="7371c-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="7371c-109">**паутпутфиле**</span><span class="sxs-lookup"><span data-stu-id="7371c-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="7371c-110">Указатель на строку, завершающуюся нулем, которая указывает имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="7371c-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="7371c-111">**пдататипе**</span><span class="sxs-lookup"><span data-stu-id="7371c-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="7371c-112">Указатель на строку, завершающуюся нулем, которая определяет тип данных, используемых для записи документа.</span><span class="sxs-lookup"><span data-stu-id="7371c-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="7371c-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="7371c-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7371c-114">Метки.</span><span class="sxs-lookup"><span data-stu-id="7371c-114">Flags.</span></span> <span data-ttu-id="7371c-115">В настоящее время он может иметь **значение NULL** или быть следующим.</span><span class="sxs-lookup"><span data-stu-id="7371c-115">Currently, it can be **NULL** or the following.</span></span>



| <span data-ttu-id="7371c-116">Flag</span><span class="sxs-lookup"><span data-stu-id="7371c-116">Flag</span></span>                 | <span data-ttu-id="7371c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7371c-117">Meaning</span></span>                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7371c-118">DI \_ меморимап \_ запись</span><span class="sxs-lookup"><span data-stu-id="7371c-118">DI\_MEMORYMAP\_WRITE</span></span> | <span data-ttu-id="7371c-119">Приводит к тому, что [**стартдокпринтер**](startdocprinter.md) не использует [**AddJob**](addjob.md) и [**ScheduleJob**](schedulejob.md) для локальной печати.</span><span class="sxs-lookup"><span data-stu-id="7371c-119">Causes [**StartDocPrinter**](startdocprinter.md) to not use [**AddJob**](addjob.md) and [**ScheduleJob**](schedulejob.md) for local printing.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7371c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7371c-120">Remarks</span></span>

<span data-ttu-id="7371c-121">Параметр "DI \_ меморимап \_ Write" в **документе \_ info \_ 3** является оптимизацией.</span><span class="sxs-lookup"><span data-stu-id="7371c-121">The DI\_MEMORYMAP\_WRITE setting in **DOC\_INFO\_3** is an optimization.</span></span> <span data-ttu-id="7371c-122">Это позволяет GDI сопоставлять файлы очереди в приложении и ускорить запись.</span><span class="sxs-lookup"><span data-stu-id="7371c-122">This allows GDI to map spool files in the application and speed up the recording.</span></span>

## <a name="requirements"></a><span data-ttu-id="7371c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7371c-123">Requirements</span></span>



| <span data-ttu-id="7371c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7371c-124">Requirement</span></span> | <span data-ttu-id="7371c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7371c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7371c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7371c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7371c-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7371c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7371c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7371c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7371c-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7371c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7371c-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7371c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7371c-131"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7371c-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7371c-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="7371c-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7371c-133">**\_ Doc \_ info \_ «кто** (Юникод) и **\_ \_ сведения о документе \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7371c-133">**\_DOC\_INFO\_3W** (Unicode) and **\_DOC\_INFO\_3A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="7371c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7371c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7371c-135">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="7371c-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7371c-136">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="7371c-136">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7371c-137">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="7371c-137">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="7371c-138">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="7371c-138">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="7371c-139">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="7371c-139">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




