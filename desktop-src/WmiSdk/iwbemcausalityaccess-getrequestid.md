---
description: Метод Жетрекуестид возвращает значение глобального уникального идентификатора (GUID) для запроса. GUID — это уникальное 128-разрядное число.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'Метод Ивбемкаусалитякцесс:: Жетрекуестид (Вбеминт. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683890"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a><span data-ttu-id="d1cfc-104">Метод Ивбемкаусалитякцесс:: Жетрекуестид</span><span class="sxs-lookup"><span data-stu-id="d1cfc-104">IWbemCausalityAccess::GetRequestId method</span></span>

<span data-ttu-id="d1cfc-105">Метод **жетрекуестид** возвращает значение глобального уникального идентификатора (GUID) для запроса.</span><span class="sxs-lookup"><span data-stu-id="d1cfc-105">The **GetRequestId** method returns a Globally Unique Identifier (GUID) value for a request.</span></span> <span data-ttu-id="d1cfc-106">GUID — это уникальное 128-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="d1cfc-106">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1cfc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1cfc-107">Syntax</span></span>


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="d1cfc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1cfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1cfc-109">*идентификатор процесса* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d1cfc-109">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1cfc-110">Значение идентификатора GUID, уникально идентифицирующего запрос.</span><span class="sxs-lookup"><span data-stu-id="d1cfc-110">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="d1cfc-111">Например, 5b2fc63a-8AF4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="d1cfc-111">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1cfc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1cfc-112">Return value</span></span>

<span data-ttu-id="d1cfc-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d1cfc-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1cfc-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1cfc-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cfc-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d1cfc-115">Requirements</span></span>



| <span data-ttu-id="d1cfc-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d1cfc-116">Requirement</span></span> | <span data-ttu-id="d1cfc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d1cfc-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cfc-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1cfc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d1cfc-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1cfc-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1cfc-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1cfc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d1cfc-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1cfc-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1cfc-122">Header</span><span class="sxs-lookup"><span data-stu-id="d1cfc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1cfc-123"><dt>Вбеминт. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1cfc-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="d1cfc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d1cfc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1cfc-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1cfc-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cfc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1cfc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cfc-127">**ивбемкаусалитякцесс**</span><span class="sxs-lookup"><span data-stu-id="d1cfc-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




