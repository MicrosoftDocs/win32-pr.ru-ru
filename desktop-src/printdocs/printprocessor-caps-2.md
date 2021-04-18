---
description: Представляет сведения о принтера.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Структура PRINTPROCESSOR_CAPS_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693403"
---
# <a name="printprocessor_caps_2-structure"></a><span data-ttu-id="b47b8-103">\_Структура принтпроцессор Cap \_ 2</span><span class="sxs-lookup"><span data-stu-id="b47b8-103">PRINTPROCESSOR\_CAPS\_2 structure</span></span>

<span data-ttu-id="b47b8-104">Представляет сведения о принтера.</span><span class="sxs-lookup"><span data-stu-id="b47b8-104">Represents printer capability information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b47b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b47b8-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a><span data-ttu-id="b47b8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b47b8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b47b8-107">**двлевел**</span><span class="sxs-lookup"><span data-stu-id="b47b8-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="b47b8-108">Значение, указывающее номер версии структуры.</span><span class="sxs-lookup"><span data-stu-id="b47b8-108">A value that indicates the structure's version number.</span></span>

</dd> <dt>

<span data-ttu-id="b47b8-109">**двнупоптионс**</span><span class="sxs-lookup"><span data-stu-id="b47b8-109">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="b47b8-110">Битовая маска, представляющая различные числа страниц документа, которые принтер может печатать на одной стороне физического листа.</span><span class="sxs-lookup"><span data-stu-id="b47b8-110">A bit mask representing the various numbers of document pages the printer can print on a single side of a physical sheet.</span></span> <span data-ttu-id="b47b8-111">Младший значащий бит представляет одну страницу документа на каждой стороне, следующий бит представляет две страницы документа на стороне и т. д.</span><span class="sxs-lookup"><span data-stu-id="b47b8-111">The least significant bit represents one document page per side, the next bit represents 2 document pages per side, and so on.</span></span> <span data-ttu-id="b47b8-112">Например, 0x0000810B указывает, что принтер поддерживает 1, 2, 4, 9 и 16 страниц документа на физическую сторону.</span><span class="sxs-lookup"><span data-stu-id="b47b8-112">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical side.</span></span>

</dd> <dt>

<span data-ttu-id="b47b8-113">**двпажеордерфлагс**</span><span class="sxs-lookup"><span data-stu-id="b47b8-113">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b47b8-114">Значение флага, указывающее порядок, в котором будут печататься страницы.</span><span class="sxs-lookup"><span data-stu-id="b47b8-114">A flag value that indicates the order in which pages will be printed.</span></span> <span data-ttu-id="b47b8-115">Это может быть **Обычная \_ Печать**, **обратная \_ Печать** или **буклетная \_ Печать**.</span><span class="sxs-lookup"><span data-stu-id="b47b8-115">It can be **NORMAL\_PRINT**, **REVERSE\_PRINT**, or **BOOKLET\_PRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="b47b8-116">**двнумберофкопиес**</span><span class="sxs-lookup"><span data-stu-id="b47b8-116">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="b47b8-117">Максимальное число копий, которое может быть обработано принтером.</span><span class="sxs-lookup"><span data-stu-id="b47b8-117">The maximum number of copies the printer can handle.</span></span>

</dd> <dt>

<span data-ttu-id="b47b8-118">**двнупдиректионкапс**</span><span class="sxs-lookup"><span data-stu-id="b47b8-118">**dwNupDirectionCaps**</span></span>
</dt> <dd>

<span data-ttu-id="b47b8-119">Доступные закономерности при печати нескольких страниц документа на одной стороне листа бумаги.</span><span class="sxs-lookup"><span data-stu-id="b47b8-119">The available patterns when multiple document pages are printed on the same side of a sheet of paper.</span></span> <span data-ttu-id="b47b8-120">Возможны следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b47b8-120">The possible flags are the following:</span></span>



| <span data-ttu-id="b47b8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b47b8-121">Value</span></span>                     | <span data-ttu-id="b47b8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b47b8-122">Meaning</span></span>                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47b8-123">ППКАПС \_ вправо, \_ затем \_ вниз</span><span class="sxs-lookup"><span data-stu-id="b47b8-123">PPCAPS\_RIGHT\_THEN\_DOWN</span></span> | <span data-ttu-id="b47b8-124">Страницы отображаются в строках справа налево, каждая последующая строка под ее предшественником.</span><span class="sxs-lookup"><span data-stu-id="b47b8-124">Pages appear in rows from right to left, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="b47b8-125">ППКАПС \_ вниз, \_ затем \_ вправо</span><span class="sxs-lookup"><span data-stu-id="b47b8-125">PPCAPS\_DOWN\_THEN\_RIGHT</span></span> | <span data-ttu-id="b47b8-126">Страницы отображаются в столбцах сверху вниз, каждый последующий столбец справа от его предшественника.</span><span class="sxs-lookup"><span data-stu-id="b47b8-126">Pages appear in columns from top to bottom, each subsequent column to the right of its predecessor.</span></span> |
| <span data-ttu-id="b47b8-127">ППКАПС \_ влево, \_ затем \_ вниз</span><span class="sxs-lookup"><span data-stu-id="b47b8-127">PPCAPS\_LEFT\_THEN\_DOWN</span></span>  | <span data-ttu-id="b47b8-128">Страницы отображаются в строках слева направо, каждая последующая строка под ее предшественником.</span><span class="sxs-lookup"><span data-stu-id="b47b8-128">Pages appear in rows from left to right, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="b47b8-129">ППКАПС \_ вниз, \_ затем \_ влево</span><span class="sxs-lookup"><span data-stu-id="b47b8-129">PPCAPS\_DOWN\_THEN\_LEFT</span></span>  | <span data-ttu-id="b47b8-130">Страницы отображаются в столбцах сверху вниз, каждый последующий столбец слева от его предшественника.</span><span class="sxs-lookup"><span data-stu-id="b47b8-130">Pages appear in columns from top to bottom, each subsequent column to the left of its predecessor.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b47b8-131">**двнупбордеркапс**</span><span class="sxs-lookup"><span data-stu-id="b47b8-131">**dwNupBorderCaps**</span></span>
</dt> <dd>

<span data-ttu-id="b47b8-132">Может быть только ППКАПС \_ границей. \_ это означает, что при печати нескольких страниц документа на одной стороне физического листа принтер может сообщить, следует ли печатать границу вокруг области изображения каждой страницы документа.</span><span class="sxs-lookup"><span data-stu-id="b47b8-132">Can be only PPCAPS\_BORDER\_PRINT, indicating that, when multiple document pages are being printed on a single side of a physical sheet, the printer can be told whether or not to print a border around the imageable area of each document page.</span></span>

</dd> <dt>

<span data-ttu-id="b47b8-133">**двбуклесандлингкапс**</span><span class="sxs-lookup"><span data-stu-id="b47b8-133">**dwBookletHandlingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="b47b8-134">Может быть только ППКАПСная \_ брошюра \_ , указывающая, что принтер может печатать стиль буклета.</span><span class="sxs-lookup"><span data-stu-id="b47b8-134">Can only be PPCAPS\_BOOKLET\_EDGE, indicating that the printer can print booklet style.</span></span>

<span data-ttu-id="b47b8-135"></dd> <dt>**двдуплексхандлингкапс**</dt> </span><span class="sxs-lookup"><span data-stu-id="b47b8-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span></span><dd> 

| <span data-ttu-id="b47b8-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b47b8-136">Value</span></span>                                         | <span data-ttu-id="b47b8-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b47b8-137">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47b8-138">ППКАПС \_ обратные \_ страницы \_ на \_ обратный \_ дуплекс</span><span class="sxs-lookup"><span data-stu-id="b47b8-138">PPCAPS\_REVERSE\_PAGES\_FOR\_REVERSE\_DUPLEX</span></span>  | <span data-ttu-id="b47b8-139">При печати в обратных и дуплексных режимах процессор может печатать порядок каждой пары страниц, поэтому вместо печати в порядке 4, 3, 2, 1, они будут напечатаны в порядке 3, 4, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="b47b8-139">When printing in reverse order and duplexing, the processor can print swap the order of each pair of pages, so instead of printing in order 4,3,2,1, they will print in the order 3,4,1,2.</span></span>                                                                                                       |
| <span data-ttu-id="b47b8-140">ППКАПС \_ не \_ Отправить \_ Дополнительные \_ страницы \_ для \_ дуплексного</span><span class="sxs-lookup"><span data-stu-id="b47b8-140">PPCAPS\_DONT\_SEND\_EXTRA\_PAGES\_FOR\_DUPLEX</span></span> | <span data-ttu-id="b47b8-141">При использовании двусторонней обработки обработчик заданий печати может давать не отправку дополнительной страницы при нечетном числе страниц документа.</span><span class="sxs-lookup"><span data-stu-id="b47b8-141">When duplexing, the Print Processor can be told not to send an extra page when there is an odd number of document pages.</span></span> <span data-ttu-id="b47b8-142">Процессор будет принимать значение так, как это возможно, но в тех случаях, когда ненужная пустая страница может привести к неправильному выходу, дополнительные страницы все еще могут быть отправлены.</span><span class="sxs-lookup"><span data-stu-id="b47b8-142">The processor will honor the value as best as it can, but in cases where preventing an extra blank page would cause improper output, the extra pages may still be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b47b8-143">**двскалингкапс**</span><span class="sxs-lookup"><span data-stu-id="b47b8-143">**dwScalingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="b47b8-144">Может быть только ППКАПС \_ квадратным \_ масштабированием, указывая, что принтер может масштабировать изображение страницы.</span><span class="sxs-lookup"><span data-stu-id="b47b8-144">Can only be PPCAPS\_SQUARE\_SCALING, indicating that the printer can scale the page image.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b47b8-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b47b8-145">Remarks</span></span>

<span data-ttu-id="b47b8-146">Значения всех членов структуры предоставляются функцией **жетпринтпроцессоркапабилитиес** , которая описана в комплекте драйверов для Windows.</span><span class="sxs-lookup"><span data-stu-id="b47b8-146">Values for all structure members are supplied by the **GetPrintProcessorCapabilities** function which is documented in the Windows Driver Kit.</span></span>

<span data-ttu-id="b47b8-147">Когда приложение вызывает [**жетпринтердата**](getprinterdata.md), диспетчер очереди вызовов вызывает функцию **жетпринтпроцессоркапабилитиес** обработчика заданий печати и задает имя значения, имеющего формат _DataType_ **принтпроккапс \_**, где *DataType* — это имя входного типа данных.</span><span class="sxs-lookup"><span data-stu-id="b47b8-147">When an application calls [**GetPrinterData**](getprinterdata.md), the spooler calls a print processor's **GetPrintProcessorCapabilities** function and specifies a value name that has a format of **PrintProcCaps\_**_datatype_, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b47b8-148">Требования</span><span class="sxs-lookup"><span data-stu-id="b47b8-148">Requirements</span></span>



| <span data-ttu-id="b47b8-149">Требование</span><span class="sxs-lookup"><span data-stu-id="b47b8-149">Requirement</span></span> | <span data-ttu-id="b47b8-150">Значение</span><span class="sxs-lookup"><span data-stu-id="b47b8-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47b8-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b47b8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b47b8-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b47b8-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b47b8-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b47b8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b47b8-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b47b8-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b47b8-155">Header</span><span class="sxs-lookup"><span data-stu-id="b47b8-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="b47b8-156"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b47b8-156"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b47b8-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b47b8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47b8-158">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="b47b8-158">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b47b8-159">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="b47b8-159">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b47b8-160">**жетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="b47b8-160">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

 




