---
description: '\_Структура запроса ввода-вывода бросить \_ начинает структуру данных управления протоколом.'
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: Структура SCARD_IO_REQUEST (Винсмкрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345322"
---
# <a name="scard_io_request-structure"></a><span data-ttu-id="9793c-103">\_Структура запроса ввода-вывода бросить \_</span><span class="sxs-lookup"><span data-stu-id="9793c-103">SCARD\_IO\_REQUEST structure</span></span>

<span data-ttu-id="9793c-104">Структура **\_ \_ запроса ввода-вывода бросить** начинает структуру данных управления протоколом.</span><span class="sxs-lookup"><span data-stu-id="9793c-104">The **SCARD\_IO\_REQUEST** structure begins a protocol control information structure.</span></span> <span data-ttu-id="9793c-105">Все сведения, относящиеся к протоколу, затем следуют этой структуре сразу.</span><span class="sxs-lookup"><span data-stu-id="9793c-105">Any protocol-specific information then immediately follows this structure.</span></span> <span data-ttu-id="9793c-106">Вся длина структуры должна быть согласована с базовым размером аппаратной архитектуры.</span><span class="sxs-lookup"><span data-stu-id="9793c-106">The entire length of the structure must be aligned with the underlying hardware architecture word size.</span></span> <span data-ttu-id="9793c-107">Например, в Win32 длина любой информации PCI должна быть кратной четырем байтам, что соответствует 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="9793c-107">For example, in Win32 the length of any PCI information must be a multiple of four bytes so that it aligns on a 32-bit boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="9793c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9793c-108">Syntax</span></span>


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a><span data-ttu-id="9793c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="9793c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="9793c-110">**двпротокол**</span><span class="sxs-lookup"><span data-stu-id="9793c-110">**dwProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="9793c-111">Используемый протокол.</span><span class="sxs-lookup"><span data-stu-id="9793c-111">Protocol in use.</span></span>

</dd> <dt>

<span data-ttu-id="9793c-112">**кбпЦиленгс**</span><span class="sxs-lookup"><span data-stu-id="9793c-112">**cbPciLength**</span></span>
</dt> <dd>

<span data-ttu-id="9793c-113">Длина (в байтах) структуры **\_ \_ запроса ввода-вывода бросить** , а также следующие сведения, относящиеся к шине PCI.</span><span class="sxs-lookup"><span data-stu-id="9793c-113">Length, in bytes, of the **SCARD\_IO\_REQUEST** structure plus any following PCI-specific information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9793c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9793c-114">Requirements</span></span>



| <span data-ttu-id="9793c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9793c-115">Requirement</span></span> | <span data-ttu-id="9793c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9793c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9793c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9793c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9793c-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9793c-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9793c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9793c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9793c-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9793c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9793c-121">Header</span><span class="sxs-lookup"><span data-stu-id="9793c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9793c-122"><dt>Винсмкрд. h</dt></span><span class="sxs-lookup"><span data-stu-id="9793c-122"><dt>Winsmcrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9793c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9793c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9793c-124">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="9793c-124">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




