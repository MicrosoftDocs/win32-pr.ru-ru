---
title: Имсрдпдевице Редиректионстате, свойство
description: Указывает состояние перенаправления устройства.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректионстате
- Службы удаленных рабочих столов свойства Редиректионстате, интерфейс Имсрдпдевице
- Службы удаленных рабочих столов интерфейса Имсрдпдевице, свойство Редиректионстате
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490344"
---
# <a name="imsrdpdeviceredirectionstate-property"></a><span data-ttu-id="fb61f-106">Свойство Имсрдпдевице:: Редиректионстате</span><span class="sxs-lookup"><span data-stu-id="fb61f-106">IMsRdpDevice::RedirectionState property</span></span>

<span data-ttu-id="fb61f-107">Указывает состояние перенаправления устройства.</span><span class="sxs-lookup"><span data-stu-id="fb61f-107">Indicates the redirection state of the device.</span></span>

<span data-ttu-id="fb61f-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="fb61f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb61f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb61f-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="fb61f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fb61f-110">Property value</span></span>

<span data-ttu-id="fb61f-111">Присвойте этому параметру значение **Variant \_ false** , чтобы отключить перенаправление или **вариант \_ true** , чтобы включить перенаправление.</span><span class="sxs-lookup"><span data-stu-id="fb61f-111">Set this parameter to **VARIANT\_FALSE** to disable redirection or **VARIANT\_TRUE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb61f-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fb61f-112">Error codes</span></span>

<span data-ttu-id="fb61f-113">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="fb61f-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="fb61f-114">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="fb61f-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb61f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fb61f-115">Requirements</span></span>



| <span data-ttu-id="fb61f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fb61f-116">Requirement</span></span> | <span data-ttu-id="fb61f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fb61f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb61f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb61f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fb61f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb61f-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fb61f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb61f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fb61f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb61f-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fb61f-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fb61f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb61f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb61f-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb61f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fb61f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb61f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb61f-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb61f-126">IID</span><span class="sxs-lookup"><span data-stu-id="fb61f-126">IID</span></span><br/>                      | <span data-ttu-id="fb61f-127">IID \_ имсрдпдевице определен как 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="fb61f-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="fb61f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb61f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb61f-129">**имсрдпдевице**</span><span class="sxs-lookup"><span data-stu-id="fb61f-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





