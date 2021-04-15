---
description: Указывает, что проверяется при проверке цифровой подписи.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: Перечисление CAPICOM_SIGNED_DATA_VERIFY_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669036"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a><span data-ttu-id="3d744-103">\_ \_ \_ \_ Перечисление флагов проверки данных CAPICOM со знаком</span><span class="sxs-lookup"><span data-stu-id="3d744-103">CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG enumeration</span></span>

<span data-ttu-id="3d744-104">Перечисление **\_ \_ \_ \_ флагов «CAPICOM подписанные данные** » указывает, что проверяется при проверке [*цифровой подписи*](../secgloss/d-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3d744-104">The **CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG** enumeration indicates what is checked when a [*digital signature*](../secgloss/d-gly.md) is verified.</span></span>

## <a name="members"></a><span data-ttu-id="3d744-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="3d744-105">Members</span></span>



| <span data-ttu-id="3d744-106">Член</span><span class="sxs-lookup"><span data-stu-id="3d744-106">Member</span></span>                                           | <span data-ttu-id="3d744-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3d744-107">Description</span></span>                                                                                                 | <span data-ttu-id="3d744-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3d744-108">Value</span></span> |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="3d744-109">**CAPICOM \_ проверить \_ \_ только подпись**</span><span class="sxs-lookup"><span data-stu-id="3d744-109">**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</span></span>             | <span data-ttu-id="3d744-110">Проверяется только подпись.</span><span class="sxs-lookup"><span data-stu-id="3d744-110">Only the signature is checked.</span></span><br/>                                                                   | <span data-ttu-id="3d744-111">0</span><span class="sxs-lookup"><span data-stu-id="3d744-111">0</span></span>     |
| <span data-ttu-id="3d744-112">**CAPICOM \_ Проверка \_ подписи \_ и \_ сертификата**</span><span class="sxs-lookup"><span data-stu-id="3d744-112">**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</span></span> | <span data-ttu-id="3d744-113">Проверяется подпись и допустимость сертификата, используемого для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="3d744-113">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> | <span data-ttu-id="3d744-114">1</span><span class="sxs-lookup"><span data-stu-id="3d744-114">1</span></span>     |



## <a name="requirements"></a><span data-ttu-id="3d744-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3d744-115">Requirements</span></span>



| <span data-ttu-id="3d744-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3d744-116">Requirement</span></span> | <span data-ttu-id="3d744-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3d744-117">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3d744-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="3d744-118">Redistributable</span></span><br/> | <span data-ttu-id="3d744-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="3d744-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="3d744-120">Header</span><span class="sxs-lookup"><span data-stu-id="3d744-120">Header</span></span><br/>          | <dl> <span data-ttu-id="3d744-121"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d744-121"><dt>Capicom.h</dt></span></span> </dl> |



 

 
