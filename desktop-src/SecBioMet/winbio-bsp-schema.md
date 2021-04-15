---
title: Структура WINBIO_BSP_SCHEMA (Винбио \_ types. h)
description: Описание возможностей поставщика биометрической службы.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- API структуры WINBIO_BSP_SCHEMA биометрическая платформа Windows
- PWINBIO_BSP_SCHEMA API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490767"
---
# <a name="winbio_bsp_schema-structure"></a><span data-ttu-id="97f43-105">\_ \_ Структура схемы BSP винбио</span><span class="sxs-lookup"><span data-stu-id="97f43-105">WINBIO\_BSP\_SCHEMA structure</span></span>

<span data-ttu-id="97f43-106">В **структуре \_ \_ схемы BSP винбио** описываются возможности поставщика биометрической службы.</span><span class="sxs-lookup"><span data-stu-id="97f43-106">The **WINBIO\_BSP\_SCHEMA** structure describes the capabilities of a biometric service provider.</span></span> <span data-ttu-id="97f43-107">Эта структура используется функцией [**винбиоенумсервицепровидерс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) .</span><span class="sxs-lookup"><span data-stu-id="97f43-107">This structure is used by the [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f43-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97f43-108">Syntax</span></span>


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="97f43-109">Члены</span><span class="sxs-lookup"><span data-stu-id="97f43-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="97f43-110">**биометрикфактор**</span><span class="sxs-lookup"><span data-stu-id="97f43-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="97f43-111">Тип биометрического измерения, используемого этим устройством.</span><span class="sxs-lookup"><span data-stu-id="97f43-111">The type of biometric measurement used by this device.</span></span> <span data-ttu-id="97f43-112">В настоящее время это должен быть **винбио \_ типа " \_ отпечаток**".</span><span class="sxs-lookup"><span data-stu-id="97f43-112">Currently this must be **WINBIO\_TYPE\_FINGERPRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="97f43-113">**бспид**</span><span class="sxs-lookup"><span data-stu-id="97f43-113">**BspId**</span></span>
</dt> <dd>

<span data-ttu-id="97f43-114">Значение, уникально идентифицирующее этот компонент биометрической службы.</span><span class="sxs-lookup"><span data-stu-id="97f43-114">A value that uniquely identifies this biometric service provider component.</span></span>

</dd> <dt>

<span data-ttu-id="97f43-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="97f43-115">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="97f43-116">Строка **в Юникоде**, заканчивающаяся нулем, которая содержит описание поставщика биометрической службы.</span><span class="sxs-lookup"><span data-stu-id="97f43-116">A **NULL**-terminated Unicode string that contains a description of the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="97f43-117">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="97f43-117">**Vendor**</span></span>
</dt> <dd>

<span data-ttu-id="97f43-118">Строка **в Юникоде**, заканчивающаяся нулем и содержащая имя поставщика биометрической службы.</span><span class="sxs-lookup"><span data-stu-id="97f43-118">A **NULL**-terminated Unicode string that contains the name of the vendor supplying the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="97f43-119">**Version**</span><span class="sxs-lookup"><span data-stu-id="97f43-119">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="97f43-120">Структура [**\_ версии винбио**](winbio-version.md) , содержащая версию программного обеспечения компонента биометрической службы поставщика.</span><span class="sxs-lookup"><span data-stu-id="97f43-120">A [**WINBIO\_VERSION**](winbio-version.md) structure the contains the software version of the biometric service provider component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97f43-121">Требования</span><span class="sxs-lookup"><span data-stu-id="97f43-121">Requirements</span></span>



| <span data-ttu-id="97f43-122">Требование</span><span class="sxs-lookup"><span data-stu-id="97f43-122">Requirement</span></span> | <span data-ttu-id="97f43-123">Значение</span><span class="sxs-lookup"><span data-stu-id="97f43-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97f43-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97f43-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97f43-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="97f43-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="97f43-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97f43-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97f43-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="97f43-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="97f43-128">Header</span><span class="sxs-lookup"><span data-stu-id="97f43-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="97f43-129"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97f43-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97f43-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97f43-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f43-131">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="97f43-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="97f43-132">**винбиоенумсервицепровидерс**</span><span class="sxs-lookup"><span data-stu-id="97f43-132">**WinBioEnumServiceProviders**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





