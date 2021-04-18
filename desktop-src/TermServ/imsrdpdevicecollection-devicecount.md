---
title: Имсрдпдевицеколлектион Девицекаунт, свойство
description: Возвращает число объектов в коллекции. | Имсрдпдевицеколлектион Девицекаунт, свойство
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицекаунт
- Службы удаленных рабочих столов свойства Девицекаунт, интерфейс Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, свойство Девицекаунт
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a389cd89699eb383b9f235858f0cf4a052606a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684899"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a><span data-ttu-id="4d423-107">Имсрдпдевицеколлектион: свойство Евицекаунт:D</span><span class="sxs-lookup"><span data-stu-id="4d423-107">IMsRdpDeviceCollection::DeviceCount property</span></span>

<span data-ttu-id="4d423-108">Возвращает число объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4d423-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="4d423-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4d423-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d423-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d423-110">Syntax</span></span>


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a><span data-ttu-id="4d423-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4d423-111">Property value</span></span>

<span data-ttu-id="4d423-112">Число объектов.</span><span class="sxs-lookup"><span data-stu-id="4d423-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d423-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4d423-113">Error codes</span></span>

<span data-ttu-id="4d423-114">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="4d423-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="4d423-115">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="4d423-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d423-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4d423-116">Requirements</span></span>



| <span data-ttu-id="4d423-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4d423-117">Requirement</span></span> | <span data-ttu-id="4d423-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4d423-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d423-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d423-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d423-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d423-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="4d423-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d423-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d423-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d423-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="4d423-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4d423-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d423-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d423-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="4d423-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4d423-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d423-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d423-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="4d423-127">IID</span><span class="sxs-lookup"><span data-stu-id="4d423-127">IID</span></span><br/>                      | <span data-ttu-id="4d423-128">IID \_ имсрдпдевицеколлектион определен как 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="4d423-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d423-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d423-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d423-130">**имсрдпдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="4d423-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





