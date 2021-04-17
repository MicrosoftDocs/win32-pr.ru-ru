---
description: Структура ПРОВИДОР \_ info \_ 2 добавляет поставщик печати в список порядка поставщиков печати.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Структура PROVIDOR_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684140"
---
# <a name="providor_info_2-structure"></a><span data-ttu-id="32483-103">\_Структура провидор info \_ 2</span><span class="sxs-lookup"><span data-stu-id="32483-103">PROVIDOR\_INFO\_2 structure</span></span>

<span data-ttu-id="32483-104">Структура **провидор \_ info \_ 2** добавляет поставщик печати в список порядка поставщиков печати.</span><span class="sxs-lookup"><span data-stu-id="32483-104">The **PROVIDOR\_INFO\_2** structure appends a print provider to the print provider order list.</span></span>

## <a name="syntax"></a><span data-ttu-id="32483-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32483-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="32483-106">Члены</span><span class="sxs-lookup"><span data-stu-id="32483-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="32483-107">**пордер**</span><span class="sxs-lookup"><span data-stu-id="32483-107">**pOrder**</span></span>
</dt> <dd>

<span data-ttu-id="32483-108">Указатель на строку, завершающуюся нулем, которая указывает имя поставщика печати.</span><span class="sxs-lookup"><span data-stu-id="32483-108">Pointer to a null-terminated string that specifies the name of the print provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32483-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32483-109">Remarks</span></span>

<span data-ttu-id="32483-110">Эта структура используется при вызове [**аддпринтпровидор**](addprintprovidor.md), уровень 2 для добавления указанного поставщика печати в конец списка порядка поставщиков печати.</span><span class="sxs-lookup"><span data-stu-id="32483-110">This structure is used when calling [**AddPrintProvidor**](addprintprovidor.md), level 2, to add the specified print provider to the end of the print provider order list.</span></span> <span data-ttu-id="32483-111">Поставщик будет немедленно использоваться для маршрутизации, если вызов будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="32483-111">The provider is immediately used for routing if the call succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="32483-112">Требования</span><span class="sxs-lookup"><span data-stu-id="32483-112">Requirements</span></span>



| <span data-ttu-id="32483-113">Требование</span><span class="sxs-lookup"><span data-stu-id="32483-113">Requirement</span></span> | <span data-ttu-id="32483-114">Значение</span><span class="sxs-lookup"><span data-stu-id="32483-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32483-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32483-115">Minimum supported client</span></span><br/> | <span data-ttu-id="32483-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="32483-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="32483-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32483-117">Minimum supported server</span></span><br/> | <span data-ttu-id="32483-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="32483-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="32483-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="32483-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="32483-120"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32483-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="32483-121">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="32483-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="32483-122">**\_ Провидор \_ info \_ 2W** (Юникод) и **\_ провидор \_ сведения \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="32483-122">**\_PROVIDOR\_INFO\_2W** (Unicode) and **\_PROVIDOR\_INFO\_2A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="32483-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32483-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32483-124">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="32483-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="32483-125">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="32483-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="32483-126">**аддпринтпровидор**</span><span class="sxs-lookup"><span data-stu-id="32483-126">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




