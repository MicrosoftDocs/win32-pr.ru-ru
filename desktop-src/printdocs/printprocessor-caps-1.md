---
description: Структура ПРИНТПРОЦЕССОР \_ Cap \_ 1 — это формат сведений о возможностях принтера, возвращаемых функцией жетпринтердата в буфере, заданном переменной pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Структура PRINTPROCESSOR_CAPS_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693418"
---
# <a name="printprocessor_caps_1-structure"></a><span data-ttu-id="e9c86-103">\_Структура принтпроцессор Cap \_ 1</span><span class="sxs-lookup"><span data-stu-id="e9c86-103">PRINTPROCESSOR\_CAPS\_1 structure</span></span>

<span data-ttu-id="e9c86-104">Структура **принтпроцессор \_ Cap \_ 1** — это формат сведений о возможностях принтера, возвращаемых функцией [**жетпринтердата**](getprinterdata.md) в буфере, заданном переменной *pData* .</span><span class="sxs-lookup"><span data-stu-id="e9c86-104">The **PRINTPROCESSOR\_CAPS\_1** structure is the format for the printer capability information that is returned by the [**GetPrinterData**](getprinterdata.md) function in the buffer specified by the *pData* variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c86-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9c86-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a><span data-ttu-id="e9c86-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e9c86-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9c86-107">**двлевел**</span><span class="sxs-lookup"><span data-stu-id="e9c86-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="e9c86-108">Номер версии структуры.</span><span class="sxs-lookup"><span data-stu-id="e9c86-108">The structure's version number.</span></span> <span data-ttu-id="e9c86-109">Это значение должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="e9c86-109">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="e9c86-110">**двнупоптионс**</span><span class="sxs-lookup"><span data-stu-id="e9c86-110">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="e9c86-111">Битовая маска, представляющая различные числа страниц документа, которые принтер может печатать на физической странице.</span><span class="sxs-lookup"><span data-stu-id="e9c86-111">A bit mask representing the various numbers of document pages the printer can print on a physical page.</span></span> <span data-ttu-id="e9c86-112">Младший значащий бит представляет 1 страницу документа на странице, следующий бит представляет две страницы документа на странице и т. д.</span><span class="sxs-lookup"><span data-stu-id="e9c86-112">The least significant bit represents 1 document page per page, the next bit represents 2 document pages per page, and so on.</span></span> <span data-ttu-id="e9c86-113">Например, 0x0000810B указывает, что принтер поддерживает 1, 2, 4, 9 и 16 страниц документа на физическую страницу.</span><span class="sxs-lookup"><span data-stu-id="e9c86-113">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical page.</span></span>

</dd> <dt>

<span data-ttu-id="e9c86-114">**двпажеордерфлагс**</span><span class="sxs-lookup"><span data-stu-id="e9c86-114">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e9c86-115">Порядок, в котором будут печататься страницы.</span><span class="sxs-lookup"><span data-stu-id="e9c86-115">The order in which pages will be printed.</span></span> <span data-ttu-id="e9c86-116">Это значение может иметь обычную \_ Печать, обратную \_ Печать или буклетную \_ Печать.</span><span class="sxs-lookup"><span data-stu-id="e9c86-116">This value can be NORMAL\_PRINT, REVERSE\_PRINT, or BOOKLET\_PRINT.</span></span>

</dd> <dt>

<span data-ttu-id="e9c86-117">**двнумберофкопиес**</span><span class="sxs-lookup"><span data-stu-id="e9c86-117">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="e9c86-118">Максимальное число копий, которое может быть обработано принтером.</span><span class="sxs-lookup"><span data-stu-id="e9c86-118">The maximum number of copies the printer can handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9c86-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9c86-119">Remarks</span></span>

<span data-ttu-id="e9c86-120">Значения всех членов структуры предоставляются функцией [**жетпринтпроцессоркапабилитиес**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , которая описана в комплекте драйверов для Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="e9c86-120">Values for all structure members are supplied by the [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function, which is documented in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="e9c86-121">Диспетчер очереди вызовов вызывает функцию [**жетпринтпроцессоркапабилитиес**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) обработчика печати, когда приложение вызывает [**жетпринтердата**](getprinterdata.md), указывая имя значения с форматом типа данных принтпроккапс \_ , где *DataType* — это имя входного типа.</span><span class="sxs-lookup"><span data-stu-id="e9c86-121">The spooler calls a print processor's [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function when an application calls [**GetPrinterData**](getprinterdata.md), specifying a value name with a format of PrintProcCaps\_*datatype*, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c86-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e9c86-122">Requirements</span></span>



| <span data-ttu-id="e9c86-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e9c86-123">Requirement</span></span> | <span data-ttu-id="e9c86-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e9c86-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c86-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9c86-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c86-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e9c86-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e9c86-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9c86-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c86-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e9c86-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e9c86-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e9c86-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c86-130"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9c86-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9c86-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9c86-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c86-132">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="e9c86-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e9c86-133">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="e9c86-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e9c86-134">**жетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="e9c86-134">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

