---
description: '\_ \_ Перечислимый тип флага CAPICOM определяет, будут ли игнорироваться ошибки экспорта закрытого ключа.'
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Перечисление CAPICOM_EXPORT_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665523"
---
# <a name="capicom_export_flag-enumeration"></a><span data-ttu-id="2de9e-103">\_ \_ Перечисление флагов CAPICOM Export</span><span class="sxs-lookup"><span data-stu-id="2de9e-103">CAPICOM\_EXPORT\_FLAG enumeration</span></span>

<span data-ttu-id="2de9e-104">Перечислимый тип **\_ \_ флага CAPICOM** определяет, будут ли игнорироваться ошибки экспорта закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="2de9e-104">The **CAPICOM\_EXPORT\_FLAG** enumeration type defines whether any private key export errors are ignored.</span></span>

## <a name="members"></a><span data-ttu-id="2de9e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="2de9e-105">Members</span></span>



| <span data-ttu-id="2de9e-106">Член</span><span class="sxs-lookup"><span data-stu-id="2de9e-106">Member</span></span>                                                            | <span data-ttu-id="2de9e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2de9e-107">Description</span></span>                                               | <span data-ttu-id="2de9e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2de9e-108">Value</span></span> |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| <span data-ttu-id="2de9e-109">**\_ \_ по умолчанию для экспорта CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="2de9e-109">**CAPICOM\_EXPORT\_DEFAULT**</span></span>                                      | <span data-ttu-id="2de9e-110">Любые ошибки экспорта закрытого ключа не пропускаются.</span><span class="sxs-lookup"><span data-stu-id="2de9e-110">Any private key export errors are not ignored.</span></span><br/> | <span data-ttu-id="2de9e-111">0</span><span class="sxs-lookup"><span data-stu-id="2de9e-111">0</span></span>     |
| <span data-ttu-id="2de9e-112">**CAPICOM \_ Export \_ игнорировать \_ ошибку закрытого \_ ключа \_ без \_ экспорта \_**</span><span class="sxs-lookup"><span data-stu-id="2de9e-112">**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</span></span> | <span data-ttu-id="2de9e-113">Все ошибки экспорта закрытого ключа игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2de9e-113">Any private key export errors are ignored.</span></span><br/>     | <span data-ttu-id="2de9e-114">1</span><span class="sxs-lookup"><span data-stu-id="2de9e-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="2de9e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2de9e-115">Remarks</span></span>

<span data-ttu-id="2de9e-116">\_ \_ Тип перечисления флагов CAPICOM Export используется следующим методом:</span><span class="sxs-lookup"><span data-stu-id="2de9e-116">The CAPICOM\_EXPORT\_FLAG enumeration type is used by the following method:</span></span>

-   [<span data-ttu-id="2de9e-117">**Certificates. Save**</span><span class="sxs-lookup"><span data-stu-id="2de9e-117">**Certificates.Save**</span></span>](certificates-save.md)

## <a name="requirements"></a><span data-ttu-id="2de9e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2de9e-118">Requirements</span></span>



| <span data-ttu-id="2de9e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2de9e-119">Requirement</span></span> | <span data-ttu-id="2de9e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2de9e-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2de9e-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2de9e-121">Redistributable</span></span><br/> | <span data-ttu-id="2de9e-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="2de9e-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="2de9e-123">Header</span><span class="sxs-lookup"><span data-stu-id="2de9e-123">Header</span></span><br/>          | <dl> <span data-ttu-id="2de9e-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="2de9e-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




