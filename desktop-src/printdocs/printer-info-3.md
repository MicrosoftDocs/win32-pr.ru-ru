---
description: В структуре "сведения о ПРИНТЕРе \_ \_ 3" указаны сведения о безопасности принтера.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Структура PRINTER_INFO_3 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719632"
---
# <a name="printer_info_3-structure"></a><span data-ttu-id="cee1a-103">\_Сведения о принтере \_ 3 структура</span><span class="sxs-lookup"><span data-stu-id="cee1a-103">PRINTER\_INFO\_3 structure</span></span>

<span data-ttu-id="cee1a-104">В структуре " **сведения о принтере \_ \_ 3** " указаны сведения о безопасности принтера.</span><span class="sxs-lookup"><span data-stu-id="cee1a-104">The **PRINTER\_INFO\_3** structure specifies printer security information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cee1a-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="cee1a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="cee1a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cee1a-107">**псекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="cee1a-107">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="cee1a-108">Указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , указывающую сведения о безопасности принтера.</span><span class="sxs-lookup"><span data-stu-id="cee1a-108">Pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that specifies a printer's security information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cee1a-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cee1a-109">Remarks</span></span>

<span data-ttu-id="cee1a-110">Структура **принтера \_ info \_ 3** позволяет приложению получить и установить дескриптор безопасности принтера.</span><span class="sxs-lookup"><span data-stu-id="cee1a-110">The **PRINTER\_INFO\_3** structure lets an application get and set a printer's security descriptor.</span></span> <span data-ttu-id="cee1a-111">Вызывающий объект может сделать это, даже если у него отсутствуют определенные разрешения принтера, если у него есть стандартные права, описанные в [**сетпринтер**](setprinter.md) и в средстве [**печати**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="cee1a-111">The caller may do so even if it lacks specific printer permissions, as long as it has the standard rights described in [**SetPrinter**](setprinter.md) and [**GetPrinter**](getprinter.md).</span></span> <span data-ttu-id="cee1a-112">Таким образом, приложение может временно запретить доступ к принтеру, одновременно позволяя владельцу принтера получить доступ к списку управления доступом принтера.</span><span class="sxs-lookup"><span data-stu-id="cee1a-112">Thus, an application may temporarily deny all access to a printer, while allowing the owner of the printer to have access to the printer's discretionary ACL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee1a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cee1a-113">Requirements</span></span>



| <span data-ttu-id="cee1a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cee1a-114">Requirement</span></span> | <span data-ttu-id="cee1a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cee1a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee1a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cee1a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cee1a-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cee1a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cee1a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cee1a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cee1a-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cee1a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cee1a-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cee1a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cee1a-121"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cee1a-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee1a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cee1a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee1a-123">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="cee1a-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cee1a-124">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="cee1a-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="cee1a-125">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="cee1a-125">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="cee1a-126">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="cee1a-126">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="cee1a-127">**\_Сведения о принтере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="cee1a-127">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="cee1a-128">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="cee1a-128">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="cee1a-129">**\_Сведения о принтере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="cee1a-129">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="cee1a-130">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="cee1a-130">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

