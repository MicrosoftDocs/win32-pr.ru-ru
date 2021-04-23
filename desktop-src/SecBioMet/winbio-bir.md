---
title: Структура WINBIO_BIR (Винбио \_ types. h)
description: Представляет запись биометрической информации (Бир).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- API структуры WINBIO_BIR биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682120"
---
# <a name="winbio_bir-structure"></a><span data-ttu-id="56ffc-104">\_Структура Бир винбио</span><span class="sxs-lookup"><span data-stu-id="56ffc-104">WINBIO\_BIR structure</span></span>

<span data-ttu-id="56ffc-105">Структура **винбио \_ Бир** представляет запись биометрической информации (Бир).</span><span class="sxs-lookup"><span data-stu-id="56ffc-105">The **WINBIO\_BIR** structure represents a biometric information record (BIR).</span></span> <span data-ttu-id="56ffc-106">Информационная запись содержит блоки заголовка, данных и подписи.</span><span class="sxs-lookup"><span data-stu-id="56ffc-106">The information record contains header, data, and signature blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ffc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56ffc-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a><span data-ttu-id="56ffc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="56ffc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="56ffc-109">**хеадерблокк**</span><span class="sxs-lookup"><span data-stu-id="56ffc-109">**HeaderBlock**</span></span>
</dt> <dd>

<span data-ttu-id="56ffc-110">Структура [**\_ \_ данных винбио Бир**](winbio-bir-data.md) , которая содержит размер, в байтах и смещение заголовка Бир.</span><span class="sxs-lookup"><span data-stu-id="56ffc-110">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the BIR header.</span></span> <span data-ttu-id="56ffc-111">Заголовок содержит сведения, описывающие содержимое информационной записи.</span><span class="sxs-lookup"><span data-stu-id="56ffc-111">The header contains information that describes the contents of the information record.</span></span>

</dd> <dt>

<span data-ttu-id="56ffc-112">**стандарддатаблокк**</span><span class="sxs-lookup"><span data-stu-id="56ffc-112">**StandardDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="56ffc-113">Структура [**\_ \_ данных винбио Бир**](winbio-bir-data.md) , которая содержит размер, в байтах и смещение обработанных или необработанных биометрических данных, СОЗДАННЫХ биометрическая платформа Windowsом (ВБФ).</span><span class="sxs-lookup"><span data-stu-id="56ffc-113">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information created by the Windows Biometric Framework (WBF).</span></span>

</dd> <dt>

<span data-ttu-id="56ffc-114">**вендордатаблокк**</span><span class="sxs-lookup"><span data-stu-id="56ffc-114">**VendorDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="56ffc-115">Структура [**\_ \_ данных винбио Бир**](winbio-bir-data.md) , которая содержит размер, в байтах, а также смещение обработанных или необработанных биометрических данных, предоставленных датчиками и программным обеспечением поставщика.</span><span class="sxs-lookup"><span data-stu-id="56ffc-115">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information provided by vendor sensors and software.</span></span>

</dd> <dt>

<span data-ttu-id="56ffc-116">**сигнатуреблокк**</span><span class="sxs-lookup"><span data-stu-id="56ffc-116">**SignatureBlock**</span></span>
</dt> <dd>

<span data-ttu-id="56ffc-117">Необязательная структура [**\_ \_ данных винбио Бир**](winbio-bir-data.md) , которая содержит размер, в байтах и смещение кода проверки подлинности сообщений цифровой подписи (Mac), который может использоваться для проверки целостности Бир.</span><span class="sxs-lookup"><span data-stu-id="56ffc-117">An optional [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the digital signature message authentication code (MAC) that can be used to verify the integrity of the BIR.</span></span> <span data-ttu-id="56ffc-118">При наличии подписи или MAC должна охватываться заголовок и блоки данных.</span><span class="sxs-lookup"><span data-stu-id="56ffc-118">If present, the signature or MAC must cover the header and data blocks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56ffc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56ffc-119">Remarks</span></span>

<span data-ttu-id="56ffc-120">Использование смещений вместо указателей позволяет легко сериализовать Бир и для менее сложного перевода между 32 и 64-разрядными средами или между пользователем и режимом ядра.</span><span class="sxs-lookup"><span data-stu-id="56ffc-120">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

<span data-ttu-id="56ffc-121">Бир совместим с общей биометрической структурой формата Exchange (КБЕФФ), определенной директивой NIST 6529-A.</span><span class="sxs-lookup"><span data-stu-id="56ffc-121">The BIR is compatible with the Common Biometric Exchange Format Framework (CBEFF) defined by NIST 6529-A.</span></span>

<span data-ttu-id="56ffc-122">Если эта структура содержит значение *стандарддатаблокк* , то параметру *Type* заголовка, указанного в параметре *хеадерблокк* , должен быть задан **\_ \_ \_ \_ тип винбио ANSI 381**.</span><span class="sxs-lookup"><span data-stu-id="56ffc-122">If this structure contains a *StandardDataBlock* value, the *Type* parameter of the header specified by the *HeaderBlock* parameter must be set to **WINBIO\_ANSI\_381\_FORMAT\_TYPE**.</span></span> <span data-ttu-id="56ffc-123">Это единственный стандартный формат данных, поддерживаемый текущей версией биометрическая платформа Windows.</span><span class="sxs-lookup"><span data-stu-id="56ffc-123">This is the only standard data format supported by the current version of the Windows Biometric Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ffc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="56ffc-124">Requirements</span></span>



| <span data-ttu-id="56ffc-125">Требование</span><span class="sxs-lookup"><span data-stu-id="56ffc-125">Requirement</span></span> | <span data-ttu-id="56ffc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="56ffc-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ffc-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56ffc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="56ffc-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="56ffc-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="56ffc-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56ffc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="56ffc-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="56ffc-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="56ffc-131">Header</span><span class="sxs-lookup"><span data-stu-id="56ffc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ffc-132"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56ffc-132"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ffc-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56ffc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ffc-134">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="56ffc-134">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="56ffc-135">**ВИНБИО \_ Бир \_ данные**</span><span class="sxs-lookup"><span data-stu-id="56ffc-135">**WINBIO\_BIR\_DATA**</span></span>](winbio-bir-data.md)
</dt> <dt>

[<span data-ttu-id="56ffc-136">**\_заголовок винбио Бир \_**</span><span class="sxs-lookup"><span data-stu-id="56ffc-136">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





