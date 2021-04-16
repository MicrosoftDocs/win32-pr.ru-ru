---
title: Структура WINBIO_REGISTERED_FORMAT (Винбио \_ types. h)
description: Задает зарегистрированный формат данных в виде пары "владелец-формат".
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- API структуры WINBIO_REGISTERED_FORMAT биометрическая платформа Windows
- PWINBIO_REGISTERED_FORMAT API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534193"
---
# <a name="winbio_registered_format-structure"></a><span data-ttu-id="70b20-105">ВИНБИО \_ зарегистрированная \_ Структура формата</span><span class="sxs-lookup"><span data-stu-id="70b20-105">WINBIO\_REGISTERED\_FORMAT structure</span></span>

<span data-ttu-id="70b20-106">В **винбионой структуре \_ \_ формата** зарегистрированный формат данных указывается как пара "владелец-формат".</span><span class="sxs-lookup"><span data-stu-id="70b20-106">The **WINBIO\_REGISTERED\_FORMAT** structure specifies a registered data format as an owner/format pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b20-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70b20-107">Syntax</span></span>


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a><span data-ttu-id="70b20-108">Члены</span><span class="sxs-lookup"><span data-stu-id="70b20-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="70b20-109">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="70b20-109">**Owner**</span></span>
</dt> <dd>

<span data-ttu-id="70b20-110">ИБИА (Международная ассоциация биометрической отрасли) назначает значение владельца.</span><span class="sxs-lookup"><span data-stu-id="70b20-110">An IBIA (International Biometric Industry Association) assigned owner value.</span></span>

</dd> <dt>

<span data-ttu-id="70b20-111">**Тип**</span><span class="sxs-lookup"><span data-stu-id="70b20-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="70b20-112">Формат, которому назначен владелец.</span><span class="sxs-lookup"><span data-stu-id="70b20-112">An owner assigned format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70b20-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70b20-113">Remarks</span></span>

<span data-ttu-id="70b20-114">Так как Windows в настоящее время поддерживает только средства чтения отпечатков пальцев, в **винбио \_ зарегистрированной структуре \_ формата** должны использоваться следующие значения.</span><span class="sxs-lookup"><span data-stu-id="70b20-114">Because Windows currently supports only fingerprint readers, the following values should be used in the **WINBIO\_REGISTERED\_FORMAT** structure.</span></span>



| <span data-ttu-id="70b20-115">Константа</span><span class="sxs-lookup"><span data-stu-id="70b20-115">Constant</span></span>                                    | <span data-ttu-id="70b20-116">Значение</span><span class="sxs-lookup"><span data-stu-id="70b20-116">Meaning</span></span>                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b20-117">\_ \_ \_ Владелец формата винбио ANSI \_ 381</span><span class="sxs-lookup"><span data-stu-id="70b20-117">WINBIO\_ANSI\_381\_FORMAT\_OWNER</span></span><br/> | <span data-ttu-id="70b20-118">Международный комитет для технического комитета по стандартам информационных технологий (ИНЦИТС) M1 (Биометрия).</span><span class="sxs-lookup"><span data-stu-id="70b20-118">InterNational Committee for Information Technology Standards (INCITS) technical committee M1 (biometrics).</span></span><br/> |
| <span data-ttu-id="70b20-119">\_ \_ \_ Тип формата винбио ANSI \_ 381</span><span class="sxs-lookup"><span data-stu-id="70b20-119">WINBIO\_ANSI\_381\_FORMAT\_TYPE</span></span><br/>  | <span data-ttu-id="70b20-120">Формат обмена данными с изображением пальца ANSI ИНЦИТС 381.</span><span class="sxs-lookup"><span data-stu-id="70b20-120">ANSI INCITS 381 finger image based data interchange format.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="70b20-121">Требования</span><span class="sxs-lookup"><span data-stu-id="70b20-121">Requirements</span></span>



| <span data-ttu-id="70b20-122">Требование</span><span class="sxs-lookup"><span data-stu-id="70b20-122">Requirement</span></span> | <span data-ttu-id="70b20-123">Значение</span><span class="sxs-lookup"><span data-stu-id="70b20-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b20-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70b20-124">Minimum supported client</span></span><br/> | <span data-ttu-id="70b20-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="70b20-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="70b20-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70b20-126">Minimum supported server</span></span><br/> | <span data-ttu-id="70b20-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="70b20-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="70b20-128">Header</span><span class="sxs-lookup"><span data-stu-id="70b20-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="70b20-129"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70b20-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70b20-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70b20-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b20-131">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="70b20-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="70b20-132">**\_ \_ \_ Константы формата ANSI 381 винбио**</span><span class="sxs-lookup"><span data-stu-id="70b20-132">**WINBIO\_ANSI\_381\_FORMAT Constants**</span></span>](winbio-ansi-381-format-constants.md)
</dt> <dt>

[<span data-ttu-id="70b20-133">**\_Заголовок винбио БДБ \_ ANSI \_ 381 \_**</span><span class="sxs-lookup"><span data-stu-id="70b20-133">**WINBIO\_BDB\_ANSI\_381\_HEADER**</span></span>](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[<span data-ttu-id="70b20-134">**\_заголовок винбио Бир \_**</span><span class="sxs-lookup"><span data-stu-id="70b20-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





