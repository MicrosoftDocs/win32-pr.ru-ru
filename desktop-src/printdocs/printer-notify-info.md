---
description: '\_Структура сведений об уведомлении принтера \_ содержит сведения о принтерах, возвращаемых функцией финднекстпринтерчанженотификатион. Эта функция возвращает эти сведения после выполнения операции ожидания на объекте уведомления об изменении принтера.'
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Структура PRINTER_NOTIFY_INFO (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683648"
---
# <a name="printer_notify_info-structure"></a><span data-ttu-id="7d7e2-104">\_Структура сведений об уведомлении принтера \_</span><span class="sxs-lookup"><span data-stu-id="7d7e2-104">PRINTER\_NOTIFY\_INFO structure</span></span>

<span data-ttu-id="7d7e2-105">Структура **\_ \_ сведений об уведомлении принтера** содержит сведения о принтерах, возвращаемых функцией [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="7d7e2-105">The **PRINTER\_NOTIFY\_INFO** structure contains printer information returned by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="7d7e2-106">Эта функция возвращает эти сведения после выполнения операции ожидания на объекте уведомления об изменении принтера.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-106">The function returns this information after a wait operation on a printer change notification object has been satisfied.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d7e2-107">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a><span data-ttu-id="7d7e2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7d7e2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d7e2-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="7d7e2-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="7d7e2-110">Версия этой структуры.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-110">The version of this structure.</span></span> <span data-ttu-id="7d7e2-111">Установите для этого элемента значение 2.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-111">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="7d7e2-112">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="7d7e2-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="7d7e2-113">Битовый флаг, указывающий состояние структуры уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-113">A bit flag that indicates the state of the notification structure.</span></span> <span data-ttu-id="7d7e2-114">Если \_ \_ установлен бит уведомление об \_ ОТброшенном принтере, это означает, что некоторые уведомления пришлось отменять.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-114">If the PRINTER\_NOTIFY\_INFO\_DISCARDED bit is set, it indicates that some notifications had to be discarded.</span></span>

</dd> <dt>

<span data-ttu-id="7d7e2-115">**Количество**</span><span class="sxs-lookup"><span data-stu-id="7d7e2-115">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="7d7e2-116">Число элементов [**\_ \_ \_ данных об уведомлении принтера**](printer-notify-info-data.md) в массиве **адата** .</span><span class="sxs-lookup"><span data-stu-id="7d7e2-116">The number of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) elements in the **aData** array.</span></span>

</dd> <dt>

<span data-ttu-id="7d7e2-117">**адата**</span><span class="sxs-lookup"><span data-stu-id="7d7e2-117">**aData**</span></span>
</dt> <dd>

<span data-ttu-id="7d7e2-118">Массив структур [**\_ \_ \_ данных с уведомлением принтера**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="7d7e2-118">An array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="7d7e2-119">Каждый элемент массива определяет одно поле задания или сведения о принтере и предоставляет текущие данные для этого поля.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-119">Each element of the array identifies a single job or printer information field, and provides the current data for that field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d7e2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d7e2-120">Remarks</span></span>

<span data-ttu-id="7d7e2-121">Если элемент **flags** имеет \_ установленный бит уведомления о принтерах \_ \_ , это указывает на то, что произошло переполнение или ошибка, а уведомления могли быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-121">If the **Flags** member has the PRINTER\_NOTIFY\_INFO\_DISCARDED bit set, this indicates that an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="7d7e2-122">В этом случае необходимо вызвать [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md) и указать \_ \_ \_ флаг обновления параметров принтера для получения всех текущих данных.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-122">In this case, you must call [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) and specify the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag to retrieve all current information.</span></span> <span data-ttu-id="7d7e2-123">Пока вы не запрашиваете эту операцию обновления, система не будет отправлять дополнительные уведомления для этого объекта уведомления об изменении.</span><span class="sxs-lookup"><span data-stu-id="7d7e2-123">Until you request this refresh operation, the system will not send additional notifications for this change notification object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d7e2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7d7e2-124">Requirements</span></span>



| <span data-ttu-id="7d7e2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7d7e2-125">Requirement</span></span> | <span data-ttu-id="7d7e2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7d7e2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7e2-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d7e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7d7e2-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d7e2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7d7e2-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d7e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7d7e2-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d7e2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7d7e2-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7d7e2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d7e2-132"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e2-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d7e2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d7e2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d7e2-134">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="7d7e2-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7d7e2-135">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="7d7e2-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7d7e2-136">**финднекстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="7d7e2-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="7d7e2-137">**\_данные уведомления \_ принтера \_**</span><span class="sxs-lookup"><span data-stu-id="7d7e2-137">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> </dl>

 

 




