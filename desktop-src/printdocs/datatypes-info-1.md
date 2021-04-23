---
description: '\_ \_ Структура Data info 1 содержит сведения о типе данных, который используется для записи задания печати.'
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: Структура DATATYPES_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264460"
---
# <a name="datatypes_info_1-structure"></a><span data-ttu-id="e3a27-103">Структура данных с \_ информацией \_ 1</span><span class="sxs-lookup"><span data-stu-id="e3a27-103">DATATYPES\_INFO\_1 structure</span></span>

<span data-ttu-id="e3a27-104">Структура Data **\_ info \_ 1** содержит сведения о типе данных, который используется для записи задания печати.</span><span class="sxs-lookup"><span data-stu-id="e3a27-104">The **DATATYPES\_INFO\_1** structure contains information about the data type used to record a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3a27-105">Syntax</span></span>


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a><span data-ttu-id="e3a27-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e3a27-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3a27-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="e3a27-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="e3a27-108">Указатель на строку, завершающуюся нулем, которая определяет тип данных, используемый для записи задания печати.</span><span class="sxs-lookup"><span data-stu-id="e3a27-108">Pointer to a null-terminated string that identifies the data type used to record a print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3a27-109">Требования</span><span class="sxs-lookup"><span data-stu-id="e3a27-109">Requirements</span></span>



| <span data-ttu-id="e3a27-110">Требование</span><span class="sxs-lookup"><span data-stu-id="e3a27-110">Requirement</span></span> | <span data-ttu-id="e3a27-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e3a27-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a27-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3a27-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a27-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3a27-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e3a27-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3a27-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a27-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3a27-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e3a27-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e3a27-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a27-117"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a27-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e3a27-118">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="e3a27-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e3a27-119">Сведения о **\_ типах \_ данных \_ 1W** (Юникод) и **\_ типы данных \_ \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e3a27-119">**\_DATATYPES\_INFO\_1W** (Unicode) and **\_DATATYPES\_INFO\_1A** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="e3a27-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3a27-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a27-121">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="e3a27-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e3a27-122">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="e3a27-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e3a27-123">**енумпринтпроцессордататипес**</span><span class="sxs-lookup"><span data-stu-id="e3a27-123">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




