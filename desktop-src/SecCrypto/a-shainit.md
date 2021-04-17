---
description: Инициирует хэширование потока данных.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: Функция A_SHAInit (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685106"
---
# <a name="a_shainit-function"></a><span data-ttu-id="87129-103">\_Функция шаинит</span><span class="sxs-lookup"><span data-stu-id="87129-103">A\_SHAInit function</span></span>

<span data-ttu-id="87129-104">Инициирует хэширование потока данных.</span><span class="sxs-lookup"><span data-stu-id="87129-104">Initiates the hashing of a stream of data.</span></span>

## <a name="syntax"></a><span data-ttu-id="87129-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87129-105">Syntax</span></span>


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a><span data-ttu-id="87129-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87129-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87129-107">*Контекст* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="87129-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87129-108">Контекст SHA.</span><span class="sxs-lookup"><span data-stu-id="87129-108">The SHA context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87129-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87129-109">Return value</span></span>

<span data-ttu-id="87129-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="87129-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87129-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87129-111">Remarks</span></span>

<span data-ttu-id="87129-112">Эта функция очень похожа на Шаинит, но вызывается непосредственно из библиотеки, а не направляется через криптографическую инфраструктуру.</span><span class="sxs-lookup"><span data-stu-id="87129-112">This function is very similar to SHAInit, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="87129-113">Дополнительные сведения см. в разделе [поставщики Нткриптографик Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="87129-113">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="87129-114">Требования</span><span class="sxs-lookup"><span data-stu-id="87129-114">Requirements</span></span>



| <span data-ttu-id="87129-115">Требование</span><span class="sxs-lookup"><span data-stu-id="87129-115">Requirement</span></span> | <span data-ttu-id="87129-116">Значение</span><span class="sxs-lookup"><span data-stu-id="87129-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87129-117">Header</span><span class="sxs-lookup"><span data-stu-id="87129-117">Header</span></span><br/>  | <dl> <span data-ttu-id="87129-118"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="87129-118"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="87129-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87129-119">Library</span></span><br/> | <dl> <span data-ttu-id="87129-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87129-120"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="87129-121">DLL</span><span class="sxs-lookup"><span data-stu-id="87129-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="87129-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87129-122"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
