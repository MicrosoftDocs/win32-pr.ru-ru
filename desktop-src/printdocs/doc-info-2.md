---
description: В \_ структуре doc info \_ описывается документ, который будет напечатан.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Структура DOC_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693420"
---
# <a name="doc_info_2-structure"></a><span data-ttu-id="27589-103">\_Структура сведений о документе \_ 2</span><span class="sxs-lookup"><span data-stu-id="27589-103">DOC\_INFO\_2 structure</span></span>

<span data-ttu-id="27589-104">В **структуре \_ doc \_ info** описывается документ, который будет напечатан.</span><span class="sxs-lookup"><span data-stu-id="27589-104">The **DOC\_INFO\_2** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="27589-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27589-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a><span data-ttu-id="27589-106">Члены</span><span class="sxs-lookup"><span data-stu-id="27589-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="27589-107">**пдокнаме**</span><span class="sxs-lookup"><span data-stu-id="27589-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="27589-108">Указатель на строку, завершающуюся нулем, которая указывает имя документа.</span><span class="sxs-lookup"><span data-stu-id="27589-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="27589-109">**паутпутфиле**</span><span class="sxs-lookup"><span data-stu-id="27589-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="27589-110">Указатель на строку, завершающуюся нулем, которая указывает имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="27589-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="27589-111">**пдататипе**</span><span class="sxs-lookup"><span data-stu-id="27589-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="27589-112">Указатель на строку, завершающуюся нулем, которая определяет тип данных, используемых для записи документа.</span><span class="sxs-lookup"><span data-stu-id="27589-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="27589-113">**двмоде**</span><span class="sxs-lookup"><span data-stu-id="27589-113">**dwMode**</span></span>
</dt> <dd>

<span data-ttu-id="27589-114">Информирует диспетчер очереди печати о характере данных, которые следует отслеживать.</span><span class="sxs-lookup"><span data-stu-id="27589-114">Informs the print spooler of the nature of the data to follow.</span></span> <span data-ttu-id="27589-115">Если это значение равно нулю, диспетчер очереди печати рассматривает данные, отправленные последующими вызовами [**вритепринтер**](writeprinter.md) , как обычные задания печати (независимо от того, зависит ли оно от свойства принтера).</span><span class="sxs-lookup"><span data-stu-id="27589-115">If this value is zero, the print spooler treats the data sent by subsequent calls to [**WritePrinter**](writeprinter.md) as a normal print job (whether or not it is spooled depends on the printer property).</span></span> <span data-ttu-id="27589-116">Если это значение — \_ канал di, то открывается только канал связи.</span><span class="sxs-lookup"><span data-stu-id="27589-116">If this value is DI\_CHANNEL, only a communications channel is opened.</span></span> <span data-ttu-id="27589-117">В этом случае данные, передаваемые в последующие вызовы **вритепринтер** , отправляются на принтер или последующие вызовы [**реадпринтер**](readprinter.md) получать данные с принтера.</span><span class="sxs-lookup"><span data-stu-id="27589-117">In this case, the data passed into subsequent calls to **WritePrinter** is sent to the printer or subsequent calls to [**ReadPrinter**](readprinter.md) retrieve data from the printer.</span></span> <span data-ttu-id="27589-118">Этот режим действует до тех пор, пока не будет вызван [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .</span><span class="sxs-lookup"><span data-stu-id="27589-118">This mode remains effective until [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) is called.</span></span>

</dd> <dt>

<span data-ttu-id="27589-119">**JobId**</span><span class="sxs-lookup"><span data-stu-id="27589-119">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="27589-120">Зарезервировано для внутреннего использования; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="27589-120">Reserved for internal use; should be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27589-121">Требования</span><span class="sxs-lookup"><span data-stu-id="27589-121">Requirements</span></span>



| <span data-ttu-id="27589-122">Требование</span><span class="sxs-lookup"><span data-stu-id="27589-122">Requirement</span></span> | <span data-ttu-id="27589-123">Значение</span><span class="sxs-lookup"><span data-stu-id="27589-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27589-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27589-124">Minimum supported client</span></span><br/> | <span data-ttu-id="27589-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="27589-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="27589-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27589-126">Minimum supported server</span></span><br/> | <span data-ttu-id="27589-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="27589-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27589-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="27589-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="27589-129"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27589-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="27589-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="27589-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="27589-131">**\_ Doc \_ info \_ 2W** (Юникод) и **\_ doc \_ info \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="27589-131">**\_DOC\_INFO\_2W** (Unicode) and **\_DOC\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="27589-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27589-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27589-133">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="27589-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="27589-134">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="27589-134">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="27589-135">**енддок**</span><span class="sxs-lookup"><span data-stu-id="27589-135">**EndDoc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[<span data-ttu-id="27589-136">**реадпринтер**</span><span class="sxs-lookup"><span data-stu-id="27589-136">**ReadPrinter**</span></span>](readprinter.md)
</dt> <dt>

[<span data-ttu-id="27589-137">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="27589-137">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="27589-138">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="27589-138">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




