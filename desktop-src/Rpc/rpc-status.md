---
title: RPC_STATUS (Рпкдце. h)
description: Тип данных состояние RPC \_ представляет тип кода состояния, зависящий от платформы.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071590"
---
# <a name="rpc_status"></a><span data-ttu-id="eb035-105">\_Состояние RPC</span><span class="sxs-lookup"><span data-stu-id="eb035-105">RPC\_STATUS</span></span>

<span data-ttu-id="eb035-106">Тип данных **\_ Состояние RPC** представляет тип кода состояния, зависящий от платформы.</span><span class="sxs-lookup"><span data-stu-id="eb035-106">The data type **RPC\_STATUS** represents a platform-specific status code type.</span></span>


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a><span data-ttu-id="eb035-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb035-107">Remarks</span></span>

<span data-ttu-id="eb035-108">Тип **\_ состояния RPC** возвращается большинством функций RPC и является частью определения типа функции [**RPC \_ Object \_ инк \_ fn**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .</span><span class="sxs-lookup"><span data-stu-id="eb035-108">The **RPC\_STATUS** type is returned by most RPC functions and is part of the [**RPC\_OBJECT\_INQ\_FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) function type definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb035-109">Требования</span><span class="sxs-lookup"><span data-stu-id="eb035-109">Requirements</span></span>



| <span data-ttu-id="eb035-110">Требование</span><span class="sxs-lookup"><span data-stu-id="eb035-110">Requirement</span></span> | <span data-ttu-id="eb035-111">Значение</span><span class="sxs-lookup"><span data-stu-id="eb035-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb035-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb035-112">Minimum supported client</span></span><br/> | <span data-ttu-id="eb035-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eb035-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eb035-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb035-114">Minimum supported server</span></span><br/> | <span data-ttu-id="eb035-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eb035-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="eb035-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="eb035-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb035-117"><dt>Рпкдце. h (включение RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb035-117"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb035-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb035-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb035-119">**RPC \_ Object \_ инк \_ fn**</span><span class="sxs-lookup"><span data-stu-id="eb035-119">**RPC\_OBJECT\_INQ\_FN**</span></span>](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





