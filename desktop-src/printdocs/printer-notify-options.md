---
description: '\_ \_ Структура параметров уведомления принтера задает параметры для объекта уведомления об изменении, который наблюдает за принтером или сервером печати.'
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Структура PRINTER_NOTIFY_OPTIONS (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719552"
---
# <a name="printer_notify_options-structure"></a><span data-ttu-id="f268e-103">\_ \_ Структура параметров уведомления принтера</span><span class="sxs-lookup"><span data-stu-id="f268e-103">PRINTER\_NOTIFY\_OPTIONS structure</span></span>

<span data-ttu-id="f268e-104">Структура **\_ \_ параметров уведомления принтера** задает параметры для объекта уведомления об изменении, который наблюдает за принтером или сервером печати.</span><span class="sxs-lookup"><span data-stu-id="f268e-104">The **PRINTER\_NOTIFY\_OPTIONS** structure specifies options for a change notification object that monitors a printer or print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f268e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f268e-105">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="f268e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f268e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f268e-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="f268e-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="f268e-108">Версия этой структуры.</span><span class="sxs-lookup"><span data-stu-id="f268e-108">The version of this structure.</span></span> <span data-ttu-id="f268e-109">Установите для этого элемента значение 2.</span><span class="sxs-lookup"><span data-stu-id="f268e-109">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="f268e-110">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="f268e-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f268e-111">Битовый флаг.</span><span class="sxs-lookup"><span data-stu-id="f268e-111">A bit flag.</span></span> <span data-ttu-id="f268e-112">Если установить \_ \_ \_ флаг обновления параметров для принтера в вызове функции [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md) , функция будет выводить текущие данные для всех отслеживаемых полей сведений о принтерах.</span><span class="sxs-lookup"><span data-stu-id="f268e-112">If you set the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag in a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function, the function provides current data for all monitored printer information fields.</span></span> <span data-ttu-id="f268e-113">Функция [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) игнорирует элемент **flags** .</span><span class="sxs-lookup"><span data-stu-id="f268e-113">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function ignores the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="f268e-114">**Количество**</span><span class="sxs-lookup"><span data-stu-id="f268e-114">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="f268e-115">Число элементов в массиве **птипес** .</span><span class="sxs-lookup"><span data-stu-id="f268e-115">The number of elements in the **pTypes** array.</span></span>

</dd> <dt>

<span data-ttu-id="f268e-116">**птипес**</span><span class="sxs-lookup"><span data-stu-id="f268e-116">**pTypes**</span></span>
</dt> <dd>

<span data-ttu-id="f268e-117">Указатель на массив [**\_ параметров уведомлений принтера \_ \_ тип**](printer-notify-options-type.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="f268e-117">A pointer to an array of [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md) structures.</span></span> <span data-ttu-id="f268e-118">Используйте один элемент этого массива, чтобы указать поля сведений о принтере, которые нужно отслеживать, и один элемент, чтобы указать поля сведений о задании для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="f268e-118">Use one element of this array to specify the printer information fields to monitor, and one element to specify the job information fields to monitor.</span></span> <span data-ttu-id="f268e-119">Можно отслеживать как сведения о принтерах, так и сведения о заданиях.</span><span class="sxs-lookup"><span data-stu-id="f268e-119">You can monitor either printer information, job information, or both.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f268e-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f268e-120">Remarks</span></span>

<span data-ttu-id="f268e-121">Используйте эту структуру с функцией [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) , чтобы указать набор полей принтера или сведений о задании для отслеживания изменений.</span><span class="sxs-lookup"><span data-stu-id="f268e-121">Use this structure with the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function to specify the set of printer or job information fields to monitor for change.</span></span>

<span data-ttu-id="f268e-122">Используйте эту структуру с функцией [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md) , чтобы запросить текущие данные для всех отслеживаемых полей принтера и сведений о задании.</span><span class="sxs-lookup"><span data-stu-id="f268e-122">Use this structure with the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to request the current data for all monitored printer and job information fields.</span></span> <span data-ttu-id="f268e-123">В этом случае элемент **flags** указывает \_ \_ \_ флаг обновления параметров принтера, а функция не учитывает другие члены структуры.</span><span class="sxs-lookup"><span data-stu-id="f268e-123">In this case, the **Flags** member specifies the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag, and the function ignores the other structure members.</span></span>

## <a name="requirements"></a><span data-ttu-id="f268e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f268e-124">Requirements</span></span>



| <span data-ttu-id="f268e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f268e-125">Requirement</span></span> | <span data-ttu-id="f268e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f268e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f268e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f268e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f268e-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f268e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f268e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f268e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f268e-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f268e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f268e-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f268e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f268e-132"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f268e-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f268e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f268e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f268e-134">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="f268e-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f268e-135">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="f268e-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f268e-136">**финдфирстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="f268e-136">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="f268e-137">**финднекстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="f268e-137">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="f268e-138">**\_ \_ тип параметров уведомления \_ принтера**</span><span class="sxs-lookup"><span data-stu-id="f268e-138">**PRINTER\_NOTIFY\_OPTIONS\_TYPE**</span></span>](printer-notify-options-type.md)
</dt> </dl>

 

 




