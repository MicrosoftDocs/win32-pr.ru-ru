---
title: Структура WMDRM_ENCRYPT_SCATTER_INFO (Вмдрмсдк. h)
description: '\_ \_ \_ Структура сведений о шифровании WMDRM содержит сведения, необходимые для настройки интерфейса ивмдрменкриптскаттер для использования.'
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- Формат WMDRM_ENCRYPT_SCATTER_INFO структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721021"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a><span data-ttu-id="e622f-105">\_ \_ \_ Структура сведений о шифровании WMDRM</span><span class="sxs-lookup"><span data-stu-id="e622f-105">WMDRM\_ENCRYPT\_SCATTER\_INFO structure</span></span>

<span data-ttu-id="e622f-106">Структура **\_ \_ \_ сведений о шифровании WMDRM** содержит сведения, необходимые для настройки интерфейса [**ивмдрменкриптскаттер**](iwmdrmencryptscatter.md) для использования.</span><span class="sxs-lookup"><span data-stu-id="e622f-106">The **WMDRM\_ENCRYPT\_SCATTER\_INFO** structure contains information needed to configure the [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="e622f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e622f-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a><span data-ttu-id="e622f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e622f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e622f-109">**двстреамид**</span><span class="sxs-lookup"><span data-stu-id="e622f-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="e622f-110">Идентификатор потока для шифрования.</span><span class="sxs-lookup"><span data-stu-id="e622f-110">Identifier of the stream to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="e622f-111">**двсамплепротектионверсион**</span><span class="sxs-lookup"><span data-stu-id="e622f-111">**dwSampleProtectionVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e622f-112">Пример версии защиты, используемой для кодирования данных из указанного потока.</span><span class="sxs-lookup"><span data-stu-id="e622f-112">Sample protection version to be used to encode data from the specified stream.</span></span>

</dd> <dt>

<span data-ttu-id="e622f-113">**кбпротектионинфо**</span><span class="sxs-lookup"><span data-stu-id="e622f-113">**cbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e622f-114">Размер буфера **пбпротектионинфо** в байтах.</span><span class="sxs-lookup"><span data-stu-id="e622f-114">Size of the **pbProtectionInfo** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e622f-115">**пбпротектионинфо**</span><span class="sxs-lookup"><span data-stu-id="e622f-115">**pbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e622f-116">Буфер, содержащий дополнительные сведения о защите.</span><span class="sxs-lookup"><span data-stu-id="e622f-116">Buffer containing additional protection information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e622f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e622f-117">Remarks</span></span>

<span data-ttu-id="e622f-118">Эта структура используется методом [**ивмдрменкриптскаттер:: инитенкриптскаттер**](iwmdrmencryptscatter-initencryptscatter.md) .</span><span class="sxs-lookup"><span data-stu-id="e622f-118">This structure is used by the [**IWMDRMEncryptScatter::InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e622f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e622f-119">Requirements</span></span>



| <span data-ttu-id="e622f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e622f-120">Requirement</span></span> | <span data-ttu-id="e622f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e622f-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e622f-122">Header</span><span class="sxs-lookup"><span data-stu-id="e622f-122">Header</span></span><br/> | <dl> <span data-ttu-id="e622f-123"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="e622f-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e622f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e622f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e622f-125">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="e622f-125">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





