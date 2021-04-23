---
description: '\_ \_ Структура документа с информацией 1 описывает документ, который будет напечатан.'
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Структура DOC_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264339"
---
# <a name="doc_info_1-structure"></a><span data-ttu-id="9bfcf-103">\_Структура сведений о документе \_ 1</span><span class="sxs-lookup"><span data-stu-id="9bfcf-103">DOC\_INFO\_1 structure</span></span>

<span data-ttu-id="9bfcf-104">Структура документа с **\_ информацией \_ 1** описывает документ, который будет напечатан.</span><span class="sxs-lookup"><span data-stu-id="9bfcf-104">The **DOC\_INFO\_1** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bfcf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bfcf-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a><span data-ttu-id="9bfcf-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9bfcf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9bfcf-107">**пдокнаме**</span><span class="sxs-lookup"><span data-stu-id="9bfcf-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="9bfcf-108">Указатель на строку, завершающуюся нулем, которая указывает имя документа.</span><span class="sxs-lookup"><span data-stu-id="9bfcf-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="9bfcf-109">**паутпутфиле**</span><span class="sxs-lookup"><span data-stu-id="9bfcf-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="9bfcf-110">Указатель на строку, завершающуюся нулем, которая указывает имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="9bfcf-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span> <span data-ttu-id="9bfcf-111">Для печати на принтере установите значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9bfcf-111">To print to a printer, set this to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9bfcf-112">**пдататипе**</span><span class="sxs-lookup"><span data-stu-id="9bfcf-112">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="9bfcf-113">Указатель на строку, завершающуюся нулем, которая определяет тип данных, используемых для записи документа.</span><span class="sxs-lookup"><span data-stu-id="9bfcf-113">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bfcf-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9bfcf-114">Requirements</span></span>



| <span data-ttu-id="9bfcf-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9bfcf-115">Requirement</span></span> | <span data-ttu-id="9bfcf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9bfcf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bfcf-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bfcf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9bfcf-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bfcf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9bfcf-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bfcf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9bfcf-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bfcf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9bfcf-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9bfcf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bfcf-122"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bfcf-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9bfcf-123">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="9bfcf-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9bfcf-124">**\_ \_ Сведения о \_ документации: 1W** (Юникод) и **\_ doc \_ info \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9bfcf-124">**\_DOC\_INFO\_1W** (Unicode) and **\_DOC\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="9bfcf-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bfcf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bfcf-126">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="9bfcf-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9bfcf-127">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="9bfcf-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9bfcf-128">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="9bfcf-128">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




