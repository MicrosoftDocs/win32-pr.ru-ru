---
description: Содержит вектор инициализации (IV) для шифрования блочного шифра в 128-битном режиме AES (AES-направление).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: Структура D3DAES_CTR_IV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342542"
---
# <a name="d3daes_ctr_iv-structure"></a><span data-ttu-id="4a554-103">Структура D3DAESного \_ \_ вектора</span><span class="sxs-lookup"><span data-stu-id="4a554-103">D3DAES\_CTR\_IV structure</span></span>

<span data-ttu-id="4a554-104">Содержит вектор инициализации (IV) для шифрования блочного шифра в 128-битном режиме AES (AES-направление).</span><span class="sxs-lookup"><span data-stu-id="4a554-104">Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a554-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a554-105">Syntax</span></span>


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a><span data-ttu-id="4a554-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4a554-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a554-107">**IV**</span><span class="sxs-lookup"><span data-stu-id="4a554-107">**IV**</span></span>
</dt> <dd>

<span data-ttu-id="4a554-108">Вектор инициализации в формате с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="4a554-108">The IV, in big-endian format.</span></span>

</dd> <dt>

<span data-ttu-id="4a554-109">**Количество**</span><span class="sxs-lookup"><span data-stu-id="4a554-109">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="4a554-110">Число блоков в формате с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="4a554-110">The block count, in big-endian format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a554-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a554-111">Remarks</span></span>

<span data-ttu-id="4a554-112">Структура **D3DAES \_ и \_ вектор** IV для [**DXVA2 \_ AES \_ \_**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="4a554-112">The **D3DAES\_CTR\_IV** structure and the [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) structure are equivalent.</span></span>

<span data-ttu-id="4a554-113">Дополнительные сведения см. в разделе [**DXVA2 AES с ключом \_ \_ \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span><span class="sxs-lookup"><span data-stu-id="4a554-113">For details, see [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a554-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4a554-114">Requirements</span></span>



| <span data-ttu-id="4a554-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4a554-115">Requirement</span></span> | <span data-ttu-id="4a554-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4a554-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a554-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a554-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a554-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4a554-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4a554-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a554-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a554-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a554-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4a554-121">Header</span><span class="sxs-lookup"><span data-stu-id="4a554-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a554-122"><dt>D3d9types. h (включение D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a554-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a554-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a554-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a554-124">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="4a554-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




