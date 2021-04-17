---
title: Имсрдпдривеколлектион Дривекаунт, свойство
description: Возвращает число объектов в коллекции. | Имсрдпдривеколлектион Дривекаунт, свойство
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дривекаунт
- Службы удаленных рабочих столов свойства Дривекаунт, интерфейс Имсрдпдривеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдривеколлектион, свойство Дривекаунт
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af724344cd7d88676483c13d1a6a8cfeb8548294
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684962"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a><span data-ttu-id="38ffe-107">Имсрдпдривеколлектион: свойство Ривекаунт:D</span><span class="sxs-lookup"><span data-stu-id="38ffe-107">IMsRdpDriveCollection::DriveCount property</span></span>

<span data-ttu-id="38ffe-108">Возвращает число объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="38ffe-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="38ffe-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="38ffe-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ffe-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38ffe-110">Syntax</span></span>


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a><span data-ttu-id="38ffe-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="38ffe-111">Property value</span></span>

<span data-ttu-id="38ffe-112">Число объектов.</span><span class="sxs-lookup"><span data-stu-id="38ffe-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="38ffe-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="38ffe-113">Error codes</span></span>

<span data-ttu-id="38ffe-114">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="38ffe-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="38ffe-115">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="38ffe-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ffe-116">Требования</span><span class="sxs-lookup"><span data-stu-id="38ffe-116">Requirements</span></span>



| <span data-ttu-id="38ffe-117">Требование</span><span class="sxs-lookup"><span data-stu-id="38ffe-117">Requirement</span></span> | <span data-ttu-id="38ffe-118">Значение</span><span class="sxs-lookup"><span data-stu-id="38ffe-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ffe-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38ffe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="38ffe-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38ffe-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="38ffe-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38ffe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="38ffe-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38ffe-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="38ffe-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="38ffe-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="38ffe-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38ffe-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="38ffe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="38ffe-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38ffe-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38ffe-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="38ffe-127">IID</span><span class="sxs-lookup"><span data-stu-id="38ffe-127">IID</span></span><br/>                      | <span data-ttu-id="38ffe-128">IID \_ имсрдпдривеколлектион определен как 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="38ffe-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38ffe-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38ffe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ffe-130">**имсрдпдривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="38ffe-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





