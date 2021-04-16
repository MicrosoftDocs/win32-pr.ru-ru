---
description: '\_ \_ Структура типа параметров уведомления принтера \_ указывает набор полей принтера или сведений о задании, которые будут отслеживаться объектом уведомления об изменении принтера. Вызов функции Финдфирстпринтерчанженотификатион указывает \_ \_ структуру параметров принтера notify, которая содержит массив \_ параметров уведомлений принтера \_ \_ .'
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Структура PRINTER_NOTIFY_OPTIONS_TYPE (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712159"
---
# <a name="printer_notify_options_type-structure"></a><span data-ttu-id="4f688-103">\_ \_ Структура типа параметров уведомления принтера \_</span><span class="sxs-lookup"><span data-stu-id="4f688-103">PRINTER\_NOTIFY\_OPTIONS\_TYPE structure</span></span>

<span data-ttu-id="4f688-104">Структура **\_ \_ \_ типа параметров уведомления принтера** указывает набор полей принтера или сведений о задании, которые будут отслеживаться объектом уведомления об изменении принтера.</span><span class="sxs-lookup"><span data-stu-id="4f688-104">The **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structure specifies the set of printer or job information fields to be monitored by a printer change notification object.</span></span>

<span data-ttu-id="4f688-105">Вызов функции [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) указывает структуру [**\_ \_ параметров принтера notify**](printer-notify-options.md) , которая содержит массив **\_ \_ параметров \_ уведомлений принтера** .</span><span class="sxs-lookup"><span data-stu-id="4f688-105">A call to the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function specifies a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure, which contains an array of **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f688-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f688-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a><span data-ttu-id="4f688-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4f688-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f688-108">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4f688-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="4f688-109">Отслеживаемый тип.</span><span class="sxs-lookup"><span data-stu-id="4f688-109">The type to be watched.</span></span> <span data-ttu-id="4f688-110">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4f688-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="4f688-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4f688-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="4f688-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4f688-112">Meaning</span></span>                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="4f688-113"><dt>**Задание \_ УВЕДОМЛЕНИЕ \_ типа**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="4f688-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="4f688-114">Указывает, что поля, указанные в массиве **пфиелдс** , \_ являются \_ константами полей уведомления о задании \_ \* .</span><span class="sxs-lookup"><span data-stu-id="4f688-114">Indicates that the fields specified in the **pFields** array are JOB\_NOTIFY\_FIELD\_\* constants.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="4f688-115"><dt>**Принтер \_ УВЕДОМЛЕНИЕ \_ типа**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="4f688-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="4f688-116">Указывает, что поля, указанные в массиве **пфиелдс** , \_ являются \_ константами полей уведомления принтера \_ \* .</span><span class="sxs-lookup"><span data-stu-id="4f688-116">Indicates that the fields specified in the **pFields** array are PRINTER\_NOTIFY\_FIELD\_\* constants.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4f688-117">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="4f688-117">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="4f688-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4f688-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4f688-119">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="4f688-119">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="4f688-120">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4f688-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4f688-121">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="4f688-121">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="4f688-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4f688-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4f688-123">**Количество**</span><span class="sxs-lookup"><span data-stu-id="4f688-123">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="4f688-124">Число элементов в массиве **пфиелдс** .</span><span class="sxs-lookup"><span data-stu-id="4f688-124">The number of elements in the **pFields** array.</span></span>

</dd> <dt>

<span data-ttu-id="4f688-125">**пфиелдс**</span><span class="sxs-lookup"><span data-stu-id="4f688-125">**pFields**</span></span>
</dt> <dd>

<span data-ttu-id="4f688-126">Указатель на массив значений.</span><span class="sxs-lookup"><span data-stu-id="4f688-126">A pointer to an array of values.</span></span> <span data-ttu-id="4f688-127">Каждый элемент массива указывает интересующее задание или поле сведений о принтере.</span><span class="sxs-lookup"><span data-stu-id="4f688-127">Each element of the array specifies a job or printer information field of interest.</span></span> <span data-ttu-id="4f688-128">Список поддерживаемых полей сведений о принтерах и заданиях см. в разделе Структура [**\_ \_ \_ данных уведомления принтера**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="4f688-128">For a list of supported printer and job information fields, see the [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f688-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4f688-129">Requirements</span></span>



| <span data-ttu-id="4f688-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4f688-130">Requirement</span></span> | <span data-ttu-id="4f688-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4f688-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f688-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f688-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4f688-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f688-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4f688-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f688-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4f688-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f688-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4f688-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4f688-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f688-137"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f688-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f688-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f688-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f688-139">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="4f688-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4f688-140">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="4f688-140">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4f688-141">**финдфирстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="4f688-141">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="4f688-142">**\_данные уведомления \_ принтера \_**</span><span class="sxs-lookup"><span data-stu-id="4f688-142">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="4f688-143">**\_Параметры уведомления \_ принтера**</span><span class="sxs-lookup"><span data-stu-id="4f688-143">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

 




