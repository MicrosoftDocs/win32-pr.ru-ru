---
title: Структура WMDRM_ENCRYPT_SCATTER_BLOCK (Вмдрмсдк. h)
description: '\_ \_ \_ Структура блочной точечной файловой структуры содержит блок данных для шифрования.'
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- Формат WMDRM_ENCRYPT_SCATTER_BLOCK структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721015"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a><span data-ttu-id="40996-105">\_ \_ \_ Структура блочного блока WMDRM Encrypt</span><span class="sxs-lookup"><span data-stu-id="40996-105">WMDRM\_ENCRYPT\_SCATTER\_BLOCK structure</span></span>

<span data-ttu-id="40996-106">Структура **\_ \_ \_ блочной точечной файловой** структуры содержит блок данных для шифрования.</span><span class="sxs-lookup"><span data-stu-id="40996-106">The **WMDRM\_ENCRYPT\_SCATTER\_BLOCK** structure contains a block of data to be encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="40996-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40996-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a><span data-ttu-id="40996-108">Члены</span><span class="sxs-lookup"><span data-stu-id="40996-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="40996-109">**двстреамид**</span><span class="sxs-lookup"><span data-stu-id="40996-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="40996-110">Идентификатор потока, которому принадлежит блок данных.</span><span class="sxs-lookup"><span data-stu-id="40996-110">Identifier of the stream to which the data block belongs.</span></span>

</dd> <dt>

<span data-ttu-id="40996-111">**кбблокк**</span><span class="sxs-lookup"><span data-stu-id="40996-111">**cbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="40996-112">Размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="40996-112">Size of block in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="40996-113">**пбблокк**</span><span class="sxs-lookup"><span data-stu-id="40996-113">**pbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="40996-114">Указатель на буфер, содержащий блок данных.</span><span class="sxs-lookup"><span data-stu-id="40996-114">Pointer to a buffer containing the data block.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40996-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40996-115">Remarks</span></span>

<span data-ttu-id="40996-116">Эта структура используется методом [**ивмдрменкриптскаттер:: енкриптскаттер**](iwmdrmencryptscatter-encryptscatter.md) для обнаружения блоков данных для шифрования.</span><span class="sxs-lookup"><span data-stu-id="40996-116">This structure is used by the [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) method to identify blocks of data to encrypt.</span></span>

## <a name="requirements"></a><span data-ttu-id="40996-117">Требования</span><span class="sxs-lookup"><span data-stu-id="40996-117">Requirements</span></span>



| <span data-ttu-id="40996-118">Требование</span><span class="sxs-lookup"><span data-stu-id="40996-118">Requirement</span></span> | <span data-ttu-id="40996-119">Значение</span><span class="sxs-lookup"><span data-stu-id="40996-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40996-120">Header</span><span class="sxs-lookup"><span data-stu-id="40996-120">Header</span></span><br/> | <dl> <span data-ttu-id="40996-121"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="40996-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40996-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40996-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40996-123">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="40996-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





