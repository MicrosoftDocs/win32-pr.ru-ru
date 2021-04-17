---
title: Имсрдпдриве Редиректионстате, свойство
description: Указывает состояние перенаправления диска.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректионстате
- Службы удаленных рабочих столов свойства Редиректионстате, интерфейс Имсрдпдриве
- Службы удаленных рабочих столов интерфейса Имсрдпдриве, свойство Редиректионстате
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415860"
---
# <a name="imsrdpdriveredirectionstate-property"></a><span data-ttu-id="aa746-106">Свойство Имсрдпдриве:: Редиректионстате</span><span class="sxs-lookup"><span data-stu-id="aa746-106">IMsRdpDrive::RedirectionState property</span></span>

<span data-ttu-id="aa746-107">Указывает состояние перенаправления диска.</span><span class="sxs-lookup"><span data-stu-id="aa746-107">Indicates the redirection state of the drive.</span></span>

<span data-ttu-id="aa746-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="aa746-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa746-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa746-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="aa746-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="aa746-110">Property value</span></span>

<span data-ttu-id="aa746-111">Присвойте этому параметру значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="aa746-111">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="aa746-112">для отключения перенаправления или **варианта \_ true**.</span><span class="sxs-lookup"><span data-stu-id="aa746-112">to disable redirection or **VARIANT\_TRUE**.</span></span> <span data-ttu-id="aa746-113">для включения перенаправления.</span><span class="sxs-lookup"><span data-stu-id="aa746-113">to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aa746-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="aa746-114">Error codes</span></span>

<span data-ttu-id="aa746-115">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="aa746-115">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="aa746-116">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="aa746-116">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa746-117">Требования</span><span class="sxs-lookup"><span data-stu-id="aa746-117">Requirements</span></span>



| <span data-ttu-id="aa746-118">Требование</span><span class="sxs-lookup"><span data-stu-id="aa746-118">Requirement</span></span> | <span data-ttu-id="aa746-119">Значение</span><span class="sxs-lookup"><span data-stu-id="aa746-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa746-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa746-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa746-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa746-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aa746-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa746-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa746-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa746-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aa746-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="aa746-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa746-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa746-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa746-126">DLL</span><span class="sxs-lookup"><span data-stu-id="aa746-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa746-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa746-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa746-128">IID</span><span class="sxs-lookup"><span data-stu-id="aa746-128">IID</span></span><br/>                      | <span data-ttu-id="aa746-129">IID \_ имсрдпдриве определен как d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="aa746-129">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="aa746-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa746-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa746-131">**имсрдпдриве**</span><span class="sxs-lookup"><span data-stu-id="aa746-131">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





