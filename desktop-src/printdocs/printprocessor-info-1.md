---
description: В \_ структуре принтпроцессор info \_ 1 указывается имя установленного обработчика печати.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: Структура PRINTPROCESSOR_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693402"
---
# <a name="printprocessor_info_1-structure"></a><span data-ttu-id="fbd79-103">\_Структура принтпроцессор info \_ 1</span><span class="sxs-lookup"><span data-stu-id="fbd79-103">PRINTPROCESSOR\_INFO\_1 structure</span></span>

<span data-ttu-id="fbd79-104">В структуре **принтпроцессор \_ info \_ 1** указывается имя установленного обработчика печати.</span><span class="sxs-lookup"><span data-stu-id="fbd79-104">The **PRINTPROCESSOR\_INFO\_1** structure specifies the name of an installed print processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbd79-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="fbd79-106">Члены</span><span class="sxs-lookup"><span data-stu-id="fbd79-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fbd79-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="fbd79-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="fbd79-108">Указатель на строку, завершающуюся нулем, которая указывает имя установленного обработчика печати.</span><span class="sxs-lookup"><span data-stu-id="fbd79-108">Pointer to a null-terminated string that specifies the name of an installed print processor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbd79-109">Требования</span><span class="sxs-lookup"><span data-stu-id="fbd79-109">Requirements</span></span>



| <span data-ttu-id="fbd79-110">Требование</span><span class="sxs-lookup"><span data-stu-id="fbd79-110">Requirement</span></span> | <span data-ttu-id="fbd79-111">Значение</span><span class="sxs-lookup"><span data-stu-id="fbd79-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd79-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbd79-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fbd79-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fbd79-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fbd79-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbd79-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fbd79-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fbd79-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fbd79-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fbd79-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbd79-117"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbd79-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fbd79-118">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="fbd79-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fbd79-119">**\_ \_ Сведения о принтпроцессор \_ 1W** (Юникод) и **\_ принтпроцессор \_ info \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fbd79-119">**\_PRINTPROCESSOR\_INFO\_1W** (Unicode) and **\_PRINTPROCESSOR\_INFO\_1A** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="fbd79-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbd79-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd79-121">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="fbd79-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fbd79-122">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="fbd79-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="fbd79-123">**енумпринтпроцессорс**</span><span class="sxs-lookup"><span data-stu-id="fbd79-123">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

 




