---
description: В структуре "сведения о ПОРТе 2" указан \_ \_ поддерживаемый порт принтера.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Структура PORT_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702546"
---
# <a name="port_info_2-structure"></a><span data-ttu-id="a648f-103">\_Сведения о порте \_ 2 Структура</span><span class="sxs-lookup"><span data-stu-id="a648f-103">PORT\_INFO\_2 structure</span></span>

<span data-ttu-id="a648f-104">В структуре " **\_ сведения о порте \_ 2** " указан поддерживаемый порт принтера.</span><span class="sxs-lookup"><span data-stu-id="a648f-104">The **PORT\_INFO\_2** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a648f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a648f-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a><span data-ttu-id="a648f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a648f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a648f-107">**ппортнаме**</span><span class="sxs-lookup"><span data-stu-id="a648f-107">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="a648f-108">Указатель на строку, завершающуюся нулем, которая определяет поддерживаемый порт принтера (например, "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="a648f-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> <dt>

<span data-ttu-id="a648f-109">**пмониторнаме**</span><span class="sxs-lookup"><span data-stu-id="a648f-109">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="a648f-110">Указатель на строку, завершающуюся нулем, которая определяет установленный монитор (например, "монитор PJL").</span><span class="sxs-lookup"><span data-stu-id="a648f-110">Pointer to a null-terminated string that identifies an installed monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="a648f-111">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a648f-111">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a648f-112">**пдескриптион**</span><span class="sxs-lookup"><span data-stu-id="a648f-112">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="a648f-113">Указатель на строку, завершающуюся нулем, которая более подробно описывает порт (например, если **ппортнаме** имеет значение LPT1:, **пдескриптион** — "порт принтера").</span><span class="sxs-lookup"><span data-stu-id="a648f-113">Pointer to a null-terminated string that describes the port in more detail (for example, if **pPortName** is "LPT1:", **pDescription** is "printer port").</span></span> <span data-ttu-id="a648f-114">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a648f-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a648f-115">**фпорттипе**</span><span class="sxs-lookup"><span data-stu-id="a648f-115">**fPortType**</span></span>
</dt> <dd>

<span data-ttu-id="a648f-116">Битовая маска, описывающая тип порта.</span><span class="sxs-lookup"><span data-stu-id="a648f-116">Bitmask describing the type of port.</span></span> <span data-ttu-id="a648f-117">Этот элемент может быть сочетанием следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a648f-117">This member can be a combination of the following values:</span></span>

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

<span data-ttu-id="a648f-118">**\_запись типа \_ порта**</span><span class="sxs-lookup"><span data-stu-id="a648f-118">**PORT\_TYPE\_WRITE**</span></span>
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

<span data-ttu-id="a648f-119">**\_Чтение типа \_ порта**</span><span class="sxs-lookup"><span data-stu-id="a648f-119">**PORT\_TYPE\_READ**</span></span>
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

<span data-ttu-id="a648f-120">**\_ПЕРЕнаправленный тип порта \_**</span><span class="sxs-lookup"><span data-stu-id="a648f-120">**PORT\_TYPE\_REDIRECTED**</span></span>
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

<span data-ttu-id="a648f-121">**\_тип порта \_ \_ подключен к сети**</span><span class="sxs-lookup"><span data-stu-id="a648f-121">**PORT\_TYPE\_NET\_ATTACHED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="a648f-122">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a648f-122">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a648f-123">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a648f-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a648f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a648f-124">Remarks</span></span>

<span data-ttu-id="a648f-125">Используйте структуру **порт \_ \_ 2** при вызове [**енумпортс**](enumports.md) , если установлено несколько мониторов, поддерживающих одни и те же порты.</span><span class="sxs-lookup"><span data-stu-id="a648f-125">Use the **PORT\_INFO\_2** structure when calling [**EnumPorts**](enumports.md) if there are multiple monitors installed that support the same ports.</span></span>

<span data-ttu-id="a648f-126">Элемент **фпорттипе** можно запросить для определения сведений о порте.</span><span class="sxs-lookup"><span data-stu-id="a648f-126">The **fPortType** member can be queried to determine information about the port.</span></span> <span data-ttu-id="a648f-127">Обратите внимание, что параметры порта не влияют на атрибуты принтера (как они возвращаются элементом **Attributes** [**\_ сведений о принтере \_ 2**](printer-info-2.md)).</span><span class="sxs-lookup"><span data-stu-id="a648f-127">Note that port settings do not influence printer attributes (as returned by the **Attributes** member of [**PRINTER\_INFO\_2**](printer-info-2.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a648f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a648f-128">Requirements</span></span>



| <span data-ttu-id="a648f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a648f-129">Requirement</span></span> | <span data-ttu-id="a648f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a648f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a648f-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a648f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a648f-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a648f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a648f-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a648f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a648f-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a648f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a648f-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a648f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a648f-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a648f-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a648f-137">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="a648f-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a648f-138">**\_ \_ Сведения о \_ порте 2W** (Юникод) и **\_ \_ сведения о порте \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a648f-138">**\_PORT\_INFO\_2W** (Unicode) and **\_PORT\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="a648f-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a648f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a648f-140">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="a648f-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a648f-141">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="a648f-141">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a648f-142">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="a648f-142">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




