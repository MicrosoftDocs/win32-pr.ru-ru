---
description: Задает кэширование маркера для принтера, открытого с помощью OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Перечисление PRINTER_OPTION_FLAGS (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266017"
---
# <a name="printer_option_flags-enumeration"></a><span data-ttu-id="dbd65-103">\_ \_ Перечисление флагов параметров принтера</span><span class="sxs-lookup"><span data-stu-id="dbd65-103">PRINTER\_OPTION\_FLAGS enumeration</span></span>

<span data-ttu-id="dbd65-104">Задает кэширование маркера для принтера, открытого с помощью [**OpenPrinter2**](openprinter2.md).</span><span class="sxs-lookup"><span data-stu-id="dbd65-104">Specifies the caching of a handle for a printer opened with [**OpenPrinter2**](openprinter2.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbd65-105">Syntax</span></span>


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="dbd65-106">Константы</span><span class="sxs-lookup"><span data-stu-id="dbd65-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dbd65-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**\_вариант принтера \_ без \_ кэша**</span><span class="sxs-lookup"><span data-stu-id="dbd65-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**PRINTER\_OPTION\_NO\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="dbd65-108">Этот маркер не кэшируется.</span><span class="sxs-lookup"><span data-stu-id="dbd65-108">The handle is not cached.</span></span> <span data-ttu-id="dbd65-109">Все функции, применяемые к маркеру, возвращенному [**OpenPrinter2**](openprinter2.md) , будут отправлены на удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="dbd65-109">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="dbd65-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_кэш параметров \_ принтера**</span><span class="sxs-lookup"><span data-stu-id="dbd65-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**PRINTER\_OPTION\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="dbd65-111">Этот маркер кэшируется.</span><span class="sxs-lookup"><span data-stu-id="dbd65-111">The handle is cached.</span></span> <span data-ttu-id="dbd65-112">Все функции, применяемые к маркеру, возвращаемому функцией [**OpenPrinter2**](openprinter2.md) , переходят в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="dbd65-112">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the local cache.</span></span>

</dd> <dt>

<span data-ttu-id="dbd65-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**\_параметр принтера \_ \_ изменение клиента**</span><span class="sxs-lookup"><span data-stu-id="dbd65-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**PRINTER\_OPTION\_CLIENT\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="dbd65-114">Маркер, возвращенный [**OpenPrinter2**](openprinter2.md) , может использоваться [**сетпринтер**](setprinter.md) для переименования подключения к принтеру.</span><span class="sxs-lookup"><span data-stu-id="dbd65-114">The handle returned by [**OpenPrinter2**](openprinter2.md) can be used by [**SetPrinter**](setprinter.md) to rename the printer connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbd65-115">Требования</span><span class="sxs-lookup"><span data-stu-id="dbd65-115">Requirements</span></span>



| <span data-ttu-id="dbd65-116">Требование</span><span class="sxs-lookup"><span data-stu-id="dbd65-116">Requirement</span></span> | <span data-ttu-id="dbd65-117">Значение</span><span class="sxs-lookup"><span data-stu-id="dbd65-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd65-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbd65-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dbd65-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbd65-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="dbd65-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbd65-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dbd65-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbd65-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dbd65-122">Header</span><span class="sxs-lookup"><span data-stu-id="dbd65-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbd65-123"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbd65-123"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbd65-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbd65-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd65-125">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="dbd65-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dbd65-126">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="dbd65-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="dbd65-127">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="dbd65-127">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="dbd65-128">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="dbd65-128">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




