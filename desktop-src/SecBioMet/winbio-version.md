---
title: Структура WINBIO_VERSION (Винбио \_ types. h)
description: Содержит номер версии программного обеспечения для компонента биометрической службы поставщика.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- API структуры WINBIO_VERSION биометрическая платформа Windows
- PWINBIO_VERSION API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493017"
---
# <a name="winbio_version-structure"></a><span data-ttu-id="d7ce9-105">\_Структура версии винбио</span><span class="sxs-lookup"><span data-stu-id="d7ce9-105">WINBIO\_VERSION structure</span></span>

<span data-ttu-id="d7ce9-106">Структура **\_ версии винбио** содержит номер версии программного обеспечения для компонента биометрической службы поставщика.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-106">The **WINBIO\_VERSION** structure contains the software version number of a biometric service provider component.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ce9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7ce9-107">Syntax</span></span>


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a><span data-ttu-id="d7ce9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d7ce9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7ce9-109">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="d7ce9-109">**MajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d7ce9-110">Значение **типа DWORD** , содержащее основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-110">A **DWORD** that contains the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="d7ce9-111">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="d7ce9-111">**MinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d7ce9-112">Значение **типа DWORD** , содержащее дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-112">A **DWORD** that contains the minor version number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7ce9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d7ce9-113">Requirements</span></span>



| <span data-ttu-id="d7ce9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d7ce9-114">Requirement</span></span> | <span data-ttu-id="d7ce9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d7ce9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ce9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7ce9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ce9-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d7ce9-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="d7ce9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7ce9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ce9-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7ce9-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d7ce9-120">Header</span><span class="sxs-lookup"><span data-stu-id="d7ce9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ce9-121"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7ce9-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ce9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7ce9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ce9-123">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="d7ce9-123">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="d7ce9-124">**\_схема винбио BSP \_**</span><span class="sxs-lookup"><span data-stu-id="d7ce9-124">**WINBIO\_BSP\_SCHEMA**</span></span>](winbio-bsp-schema.md)
</dt> <dt>

[<span data-ttu-id="d7ce9-125">**\_схема единицы \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="d7ce9-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





