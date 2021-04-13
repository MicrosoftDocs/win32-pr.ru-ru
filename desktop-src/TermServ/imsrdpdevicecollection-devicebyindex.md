---
title: Имсрдпдевицеколлектион Девицебиндекс, свойство
description: Извлекает устройство по указанному индексу.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицебиндекс
- Службы удаленных рабочих столов свойства Девицебиндекс, интерфейс Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, свойство Девицебиндекс
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12d763d4c147efa26e904a1903149504ee557ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493173"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a><span data-ttu-id="0e6ac-106">Имсрдпдевицеколлектион: свойство Евицебиндекс:D</span><span class="sxs-lookup"><span data-stu-id="0e6ac-106">IMsRdpDeviceCollection::DeviceByIndex property</span></span>

<span data-ttu-id="0e6ac-107">Извлекает устройство по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-107">Retrieves the device at the specified index.</span></span>

<span data-ttu-id="0e6ac-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e6ac-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e6ac-109">Syntax</span></span>


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="0e6ac-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0e6ac-110">Property value</span></span>

<span data-ttu-id="0e6ac-111">Указатель интерфейса [**имсрдпдевице**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="0e6ac-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e6ac-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0e6ac-112">Error codes</span></span>

<span data-ttu-id="0e6ac-113">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="0e6ac-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="0e6ac-114">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="0e6ac-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e6ac-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0e6ac-115">Requirements</span></span>



| <span data-ttu-id="0e6ac-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0e6ac-116">Requirement</span></span> | <span data-ttu-id="0e6ac-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0e6ac-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6ac-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e6ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0e6ac-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e6ac-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="0e6ac-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e6ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0e6ac-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e6ac-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="0e6ac-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0e6ac-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e6ac-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e6ac-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0e6ac-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0e6ac-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e6ac-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e6ac-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0e6ac-126">IID</span><span class="sxs-lookup"><span data-stu-id="0e6ac-126">IID</span></span><br/>                      | <span data-ttu-id="0e6ac-127">IID \_ имсрдпдевицеколлектион определен как 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="0e6ac-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e6ac-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e6ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6ac-129">**имсрдпдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="0e6ac-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





