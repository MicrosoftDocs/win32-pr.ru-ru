---
description: '\_Структура значений перечислений принтера \_ задает имя, тип и данные для значения конфигурации принтера, возвращаемого функцией енумпринтердатаекс.'
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Структура PRINTER_ENUM_VALUES (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712242"
---
# <a name="printer_enum_values-structure"></a><span data-ttu-id="f8a97-103">\_Структура значений перечислений принтера \_</span><span class="sxs-lookup"><span data-stu-id="f8a97-103">PRINTER\_ENUM\_VALUES structure</span></span>

<span data-ttu-id="f8a97-104">Структура **\_ \_ значений перечислений принтера** задает имя, тип и данные для значения конфигурации принтера, возвращаемого функцией [**енумпринтердатаекс**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="f8a97-104">The **PRINTER\_ENUM\_VALUES** structure specifies the value name, type, and data for a printer configuration value returned by the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a97-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8a97-105">Syntax</span></span>


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a><span data-ttu-id="f8a97-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f8a97-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8a97-107">**пвалуенаме**</span><span class="sxs-lookup"><span data-stu-id="f8a97-107">**pValueName**</span></span>
</dt> <dd>

<span data-ttu-id="f8a97-108">Указатель на строку, завершающуюся нулем, которая указывает имя извлеченного значения.</span><span class="sxs-lookup"><span data-stu-id="f8a97-108">Pointer to a null-terminated string that specifies the name of the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="f8a97-109">**кбвалуенаме**</span><span class="sxs-lookup"><span data-stu-id="f8a97-109">**cbValueName**</span></span>
</dt> <dd>

<span data-ttu-id="f8a97-110">Число байтов в **пвалуенаме** члене, включая завершающий нуль символа.</span><span class="sxs-lookup"><span data-stu-id="f8a97-110">The number of bytes in the **pValueName** member, including the terminating NULL character.</span></span>

</dd> <dt>

<span data-ttu-id="f8a97-111">**двтипе**</span><span class="sxs-lookup"><span data-stu-id="f8a97-111">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="f8a97-112">Код, указывающий тип данных, на который указывает элемент **pData** .</span><span class="sxs-lookup"><span data-stu-id="f8a97-112">A code indicating the type of data pointed to by the **pData** member.</span></span> <span data-ttu-id="f8a97-113">Список возможных кодов типов см. в разделе [типы значений реестра](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="f8a97-113">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="f8a97-114">**pData**</span><span class="sxs-lookup"><span data-stu-id="f8a97-114">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="f8a97-115">Указатель на буфер, содержащий данные для извлеченного значения.</span><span class="sxs-lookup"><span data-stu-id="f8a97-115">Pointer to a buffer containing the data for the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="f8a97-116">**cbData**</span><span class="sxs-lookup"><span data-stu-id="f8a97-116">**cbData**</span></span>
</dt> <dd>

<span data-ttu-id="f8a97-117">Число байтов, полученных в буфере **pData** .</span><span class="sxs-lookup"><span data-stu-id="f8a97-117">The number of bytes retrieved in the **pData** buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8a97-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f8a97-118">Requirements</span></span>



| <span data-ttu-id="f8a97-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f8a97-119">Requirement</span></span> | <span data-ttu-id="f8a97-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a97-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a97-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8a97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a97-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8a97-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8a97-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8a97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a97-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8a97-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8a97-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f8a97-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a97-126"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8a97-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8a97-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f8a97-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8a97-128">**\_ \_ Перечисление \_ валуесв** (Юникод) и **\_ \_ Перечисление \_ значений принтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8a97-128">**\_PRINTER\_ENUM\_VALUESW** (Unicode) and **\_PRINTER\_ENUM\_VALUESA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f8a97-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8a97-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a97-130">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="f8a97-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8a97-131">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="f8a97-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f8a97-132">**енумпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="f8a97-132">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> </dl>

 

