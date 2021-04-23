---
title: Имсрдпдриве имя свойства
description: Возвращает имя диска.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Имя свойства службы удаленных рабочих столов
- Свойство Name службы удаленных рабочих столов, интерфейс Имсрдпдриве
- Службы удаленных рабочих столов интерфейса Имсрдпдриве, свойство Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491631"
---
# <a name="imsrdpdrivename-property"></a><span data-ttu-id="d73fb-106">Свойство Имсрдпдриве:: Name</span><span class="sxs-lookup"><span data-stu-id="d73fb-106">IMsRdpDrive::Name property</span></span>

<span data-ttu-id="d73fb-107">Возвращает имя диска.</span><span class="sxs-lookup"><span data-stu-id="d73fb-107">Retrieves the name of the drive.</span></span>

<span data-ttu-id="d73fb-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d73fb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d73fb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d73fb-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a><span data-ttu-id="d73fb-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d73fb-110">Property value</span></span>

<span data-ttu-id="d73fb-111">Имя диска.</span><span class="sxs-lookup"><span data-stu-id="d73fb-111">The drive name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d73fb-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d73fb-112">Error codes</span></span>

<span data-ttu-id="d73fb-113">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="d73fb-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="d73fb-114">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="d73fb-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d73fb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d73fb-115">Requirements</span></span>



| <span data-ttu-id="d73fb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d73fb-116">Requirement</span></span> | <span data-ttu-id="d73fb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d73fb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d73fb-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d73fb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d73fb-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d73fb-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d73fb-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d73fb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d73fb-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d73fb-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d73fb-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d73fb-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="d73fb-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d73fb-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d73fb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d73fb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d73fb-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d73fb-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d73fb-126">IID</span><span class="sxs-lookup"><span data-stu-id="d73fb-126">IID</span></span><br/>                      | <span data-ttu-id="d73fb-127">IID \_ имсрдпдриве определен как d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="d73fb-127">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d73fb-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d73fb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73fb-129">**имсрдпдриве**</span><span class="sxs-lookup"><span data-stu-id="d73fb-129">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





