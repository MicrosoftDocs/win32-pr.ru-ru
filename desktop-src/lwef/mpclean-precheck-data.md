---
title: Структура MPCLEAN_PRECHECK_DATA (Мпклиент. h)
description: Данные уведомления передаются в функцию очистки функции обратного вызова.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA структуры устаревшие функции среды Windows
- Функции PMPCLEAN_PRECHECK_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490008"
---
# <a name="mpclean_precheck_data-structure"></a><span data-ttu-id="90e97-105">\_Структура данных ПРЕДПРОВЕРКИ мпклеан \_</span><span class="sxs-lookup"><span data-stu-id="90e97-105">MPCLEAN\_PRECHECK\_DATA structure</span></span>

<span data-ttu-id="90e97-106">Данные уведомления передаются в функцию очистки функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="90e97-106">Notification data passed to clean precheck callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e97-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90e97-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a><span data-ttu-id="90e97-108">Члены</span><span class="sxs-lookup"><span data-stu-id="90e97-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="90e97-109">**блоккедресаурцеинфо**</span><span class="sxs-lookup"><span data-stu-id="90e97-109">**BlockedResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="90e97-110">Тип: **пмпресаурце \_ info** .</span><span class="sxs-lookup"><span data-stu-id="90e97-110">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="90e97-111">Сведения о ресурсе блокируемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="90e97-111">Resource information about the resource being blocked.</span></span> <span data-ttu-id="90e97-112">Например, если выполняется **Проверка мпнотифиности \_ \_ ресурса \_**.</span><span class="sxs-lookup"><span data-stu-id="90e97-112">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="90e97-113">См [**. \_ сведения о мпресаурце**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="90e97-113">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e97-114">**\_сведения о пмпресаурце**</span><span class="sxs-lookup"><span data-stu-id="90e97-114">**PMPRESOURCE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="90e97-115">Тип: **блоккингресаурцеинфо**</span><span class="sxs-lookup"><span data-stu-id="90e97-115">Type: **BlockingResourceInfo**</span></span>

</dd> <dd>

<span data-ttu-id="90e97-116">Сведения о ресурсе, который блокируется.</span><span class="sxs-lookup"><span data-stu-id="90e97-116">Resource information about the resource that is blocking.</span></span> <span data-ttu-id="90e97-117">Например, если выполняется **Проверка мпнотифиности \_ \_ ресурса \_**.</span><span class="sxs-lookup"><span data-stu-id="90e97-117">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="90e97-118">См [**. \_ сведения о мпресаурце**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="90e97-118">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90e97-119">Требования</span><span class="sxs-lookup"><span data-stu-id="90e97-119">Requirements</span></span>



| <span data-ttu-id="90e97-120">Требование</span><span class="sxs-lookup"><span data-stu-id="90e97-120">Requirement</span></span> | <span data-ttu-id="90e97-121">Значение</span><span class="sxs-lookup"><span data-stu-id="90e97-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90e97-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90e97-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90e97-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="90e97-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="90e97-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90e97-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90e97-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="90e97-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90e97-126">Header</span><span class="sxs-lookup"><span data-stu-id="90e97-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="90e97-127"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="90e97-127"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90e97-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90e97-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e97-129">**\_сведения о мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="90e97-129">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





