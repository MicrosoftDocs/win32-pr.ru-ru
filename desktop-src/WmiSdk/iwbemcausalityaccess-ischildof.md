---
description: Метод Исчилдоф определяет, является ли запрос дочерним по отношению к указанному запросу (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'Метод Ивбемкаусалитякцесс:: Исчилдоф (Вбеминт. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265598"
---
# <a name="iwbemcausalityaccessischildof-method"></a><span data-ttu-id="84ec5-103">Метод Ивбемкаусалитякцесс:: Исчилдоф</span><span class="sxs-lookup"><span data-stu-id="84ec5-103">IWbemCausalityAccess::IsChildOf method</span></span>

<span data-ttu-id="84ec5-104">Метод **исчилдоф** определяет, является ли запрос дочерним по отношению к указанному запросу (pId).</span><span class="sxs-lookup"><span data-stu-id="84ec5-104">The **IsChildOf** method determines if a request is a child of a specified request (pId).</span></span> <span data-ttu-id="84ec5-105">Родительский запрос может иметь несколько дочерних запросов.</span><span class="sxs-lookup"><span data-stu-id="84ec5-105">A parent request can have multiple child requests.</span></span> <span data-ttu-id="84ec5-106">Каждый запрос определяется глобальным уникальным идентификатором (GUID) и может иметь родительский запрос или может быть запросом Top.</span><span class="sxs-lookup"><span data-stu-id="84ec5-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="84ec5-107">GUID — это уникальное 128-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="84ec5-107">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="84ec5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84ec5-108">Syntax</span></span>


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a><span data-ttu-id="84ec5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="84ec5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84ec5-110">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84ec5-110">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84ec5-111">Значение идентификатора GUID, уникально идентифицирующего запрос.</span><span class="sxs-lookup"><span data-stu-id="84ec5-111">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="84ec5-112">Например, 5b2fc63a-8AF4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="84ec5-112">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84ec5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84ec5-113">Return value</span></span>

<span data-ttu-id="84ec5-114">Возвращает значение "успешно", если указанный запрос является дочерним по отношению к запросу, вызывающему метод **исчилдоф** .</span><span class="sxs-lookup"><span data-stu-id="84ec5-114">Returns successful if the specified request is a child of the request calling the **IsChildOf** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="84ec5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="84ec5-115">Requirements</span></span>



| <span data-ttu-id="84ec5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="84ec5-116">Requirement</span></span> | <span data-ttu-id="84ec5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="84ec5-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84ec5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84ec5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84ec5-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84ec5-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84ec5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84ec5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84ec5-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84ec5-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84ec5-122">Header</span><span class="sxs-lookup"><span data-stu-id="84ec5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="84ec5-123"><dt>Вбеминт. h</dt></span><span class="sxs-lookup"><span data-stu-id="84ec5-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="84ec5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="84ec5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84ec5-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84ec5-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84ec5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84ec5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84ec5-127">**ивбемкаусалитякцесс**</span><span class="sxs-lookup"><span data-stu-id="84ec5-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




