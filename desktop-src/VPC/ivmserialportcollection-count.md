---
title: Свойство Ивмсериалпортколлектион Count (Впккоминтерфацес. h)
description: Возвращает число последовательных портов в этой коллекции.
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмсериалпортколлектион
- Ивмсериалпортколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf0503f00fd1df7d27a8eeafedd3efe42619b98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892186"
---
# <a name="ivmserialportcollectioncount-property"></a><span data-ttu-id="4a4f0-106">Свойство Ивмсериалпортколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="4a4f0-106">IVMSerialPortCollection::Count property</span></span>

<span data-ttu-id="4a4f0-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4a4f0-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4a4f0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4a4f0-109">Возвращает число последовательных портов в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-109">Retrieves the number of serial ports in this collection.</span></span>

<span data-ttu-id="4a4f0-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4f0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a4f0-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="4a4f0-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4a4f0-112">Property value</span></span>

<span data-ttu-id="4a4f0-113">Число последовательных портов.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-113">The number of serial ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4a4f0-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4a4f0-114">Error codes</span></span>



| <span data-ttu-id="4a4f0-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="4a4f0-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="4a4f0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4a4f0-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="4a4f0-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4a4f0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="4a4f0-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="4a4f0-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="4a4f0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="4a4f0-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="4a4f0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4a4f0-121">Requirements</span></span>



| <span data-ttu-id="4a4f0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4a4f0-122">Requirement</span></span> | <span data-ttu-id="4a4f0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4a4f0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4f0-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a4f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4f0-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4a4f0-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a4f0-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a4f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4f0-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4a4f0-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4a4f0-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4a4f0-128">End of client support</span></span><br/>    | <span data-ttu-id="4a4f0-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4a4f0-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4a4f0-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="4a4f0-130">Product</span></span><br/>                  | <span data-ttu-id="4a4f0-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4a4f0-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4a4f0-132">Header</span><span class="sxs-lookup"><span data-stu-id="4a4f0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a4f0-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a4f0-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4a4f0-134">IID</span><span class="sxs-lookup"><span data-stu-id="4a4f0-134">IID</span></span><br/>                      | <span data-ttu-id="4a4f0-135">IID \_ ивмсериалпортколлектион определен как dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="4a4f0-135">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="4a4f0-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a4f0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4f0-137">**ивмсериалпортколлектион**</span><span class="sxs-lookup"><span data-stu-id="4a4f0-137">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

