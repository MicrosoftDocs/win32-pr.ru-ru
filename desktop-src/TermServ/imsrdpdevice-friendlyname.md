---
title: Имсрдпдевице FriendlyName, свойство
description: Извлекает отображаемое имя для устройства.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- Свойство FriendlyName службы удаленных рабочих столов
- Свойство FriendlyName службы удаленных рабочих столов, интерфейс Имсрдпдевице
- Службы удаленных рабочих столов интерфейса Имсрдпдевице, свойство FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf7963cf49945b886d72a622b517438e24d148f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801558"
---
# <a name="imsrdpdevicefriendlyname-property"></a><span data-ttu-id="fbd1a-106">Свойство Имсрдпдевице:: FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fbd1a-106">IMsRdpDevice::FriendlyName property</span></span>

<span data-ttu-id="fbd1a-107">Извлекает отображаемое имя для устройства.</span><span class="sxs-lookup"><span data-stu-id="fbd1a-107">Retrieves the display name for the device.</span></span>

<span data-ttu-id="fbd1a-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fbd1a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd1a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbd1a-109">Syntax</span></span>


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a><span data-ttu-id="fbd1a-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fbd1a-110">Property value</span></span>

<span data-ttu-id="fbd1a-111">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="fbd1a-111">The display name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fbd1a-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fbd1a-112">Error codes</span></span>

<span data-ttu-id="fbd1a-113">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="fbd1a-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="fbd1a-114">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="fbd1a-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd1a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fbd1a-115">Requirements</span></span>



| <span data-ttu-id="fbd1a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fbd1a-116">Requirement</span></span> | <span data-ttu-id="fbd1a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fbd1a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd1a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbd1a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fbd1a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbd1a-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fbd1a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbd1a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fbd1a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbd1a-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fbd1a-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fbd1a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="fbd1a-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbd1a-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbd1a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fbd1a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbd1a-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbd1a-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbd1a-126">IID</span><span class="sxs-lookup"><span data-stu-id="fbd1a-126">IID</span></span><br/>                      | <span data-ttu-id="fbd1a-127">IID \_ имсрдпдевице определен как 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="fbd1a-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="fbd1a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbd1a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd1a-129">**имсрдпдевице**</span><span class="sxs-lookup"><span data-stu-id="fbd1a-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





