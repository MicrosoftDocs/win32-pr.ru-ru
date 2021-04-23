---
title: Структура WINBIO_BIR_DATA (Винбио \_ types. h)
description: Задает размер в байтах и смещение блока биометрических данных.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- API структуры WINBIO_BIR_DATA биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415472"
---
# <a name="winbio_bir_data-structure"></a><span data-ttu-id="4aca2-104">\_ \_ Структура данных винбио Бир</span><span class="sxs-lookup"><span data-stu-id="4aca2-104">WINBIO\_BIR\_DATA structure</span></span>

<span data-ttu-id="4aca2-105">Структура **\_ \_ данных винбио Бир** определяет размер в байтах и смещение блока биометрических данных.</span><span class="sxs-lookup"><span data-stu-id="4aca2-105">The **WINBIO\_BIR\_DATA** structure specifies the size, in bytes, and the offset of a block of biometric information.</span></span> <span data-ttu-id="4aca2-106">Эта структура используется структурой [**винбио \_ Бир**](winbio-bir.md) , чтобы указать, где находятся различные части записи биометрической информации.</span><span class="sxs-lookup"><span data-stu-id="4aca2-106">This structure is used by the [**WINBIO\_BIR**](winbio-bir.md) structure to specify where the various parts of a biometric information record are located.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aca2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4aca2-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a><span data-ttu-id="4aca2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4aca2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4aca2-109">**Размер**</span><span class="sxs-lookup"><span data-stu-id="4aca2-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="4aca2-110">Размер биометрической информации в байтах.</span><span class="sxs-lookup"><span data-stu-id="4aca2-110">Size, in bytes, of the biometric information.</span></span>

</dd> <dt>

<span data-ttu-id="4aca2-111">**Offset**</span><span class="sxs-lookup"><span data-stu-id="4aca2-111">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="4aca2-112">Смещение (в байтах от начала структуры [**винбио \_ Бир**](winbio-bir.md) ) биометрической информации.</span><span class="sxs-lookup"><span data-stu-id="4aca2-112">Offset, in bytes from the beginning of the [**WINBIO\_BIR**](winbio-bir.md) structure, of the biometric information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4aca2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4aca2-113">Remarks</span></span>

<span data-ttu-id="4aca2-114">Использование смещений вместо указателей позволяет легко сериализовать Бир и для менее сложного перевода между 32 и 64-разрядными средами или между пользователем и режимом ядра.</span><span class="sxs-lookup"><span data-stu-id="4aca2-114">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aca2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4aca2-115">Requirements</span></span>



| <span data-ttu-id="4aca2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4aca2-116">Requirement</span></span> | <span data-ttu-id="4aca2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4aca2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aca2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4aca2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4aca2-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4aca2-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4aca2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4aca2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4aca2-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4aca2-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4aca2-122">Header</span><span class="sxs-lookup"><span data-stu-id="4aca2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aca2-123"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4aca2-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aca2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4aca2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aca2-125">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="4aca2-125">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="4aca2-126">**ВИНБИО \_ Бир**</span><span class="sxs-lookup"><span data-stu-id="4aca2-126">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="4aca2-127">**\_заголовок винбио Бир \_**</span><span class="sxs-lookup"><span data-stu-id="4aca2-127">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





