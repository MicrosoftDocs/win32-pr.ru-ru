---
description: Представляет параметры принтера.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Структура PRINTER_OPTIONS (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693179"
---
# <a name="printer_options-structure"></a><span data-ttu-id="607f4-103">\_Структура параметров принтера</span><span class="sxs-lookup"><span data-stu-id="607f4-103">PRINTER\_OPTIONS structure</span></span>

<span data-ttu-id="607f4-104">Представляет параметры принтера.</span><span class="sxs-lookup"><span data-stu-id="607f4-104">Represents printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="607f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="607f4-105">Syntax</span></span>


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="607f4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="607f4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="607f4-107">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="607f4-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="607f4-108">Размер структуры **\_ параметров принтера** .</span><span class="sxs-lookup"><span data-stu-id="607f4-108">The size of the **PRINTER\_OPTIONS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="607f4-109">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="607f4-109">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="607f4-110">Набор [**\_ \_ флагов параметров принтера**](printer-option-flags.md) , указывающих, как маркер принтера, возвращаемого [**OpenPrinter2**](openprinter2.md) , будет использоваться другими функциями.</span><span class="sxs-lookup"><span data-stu-id="607f4-110">A set of [**PRINTER\_OPTION\_FLAGS**](printer-option-flags.md) that specifies how the handle to a printer returned by [**OpenPrinter2**](openprinter2.md) will be used by other functions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="607f4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="607f4-111">Requirements</span></span>



| <span data-ttu-id="607f4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="607f4-112">Requirement</span></span> | <span data-ttu-id="607f4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="607f4-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="607f4-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="607f4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="607f4-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="607f4-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="607f4-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="607f4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="607f4-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="607f4-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="607f4-118">Header</span><span class="sxs-lookup"><span data-stu-id="607f4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="607f4-119"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="607f4-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607f4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="607f4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607f4-121">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="607f4-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="607f4-122">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="607f4-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="607f4-123">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="607f4-123">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="607f4-124">**\_ \_ флаги параметров принтера**</span><span class="sxs-lookup"><span data-stu-id="607f4-124">**PRINTER\_OPTION\_FLAGS**</span></span>](printer-option-flags.md)
</dt> </dl>

 

 




