---
title: Свойство Item Ивмтаскколлектион (Впккоминтерфацес. h)
description: Извлекает объект Task, соответствующий указанному индексу.
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмтаскколлектион
- Интерфейс Ивмтаскколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f445280834383ee594fbb53a3390c91b1928f4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534772"
---
# <a name="ivmtaskcollectionitem-property"></a><span data-ttu-id="437ef-106">Свойство Ивмтаскколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="437ef-106">IVMTaskCollection::Item property</span></span>

<span data-ttu-id="437ef-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="437ef-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="437ef-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="437ef-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="437ef-109">Извлекает объект Task, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="437ef-109">Retrieves the task object that corresponds to the specified index.</span></span>

<span data-ttu-id="437ef-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="437ef-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="437ef-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="437ef-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a><span data-ttu-id="437ef-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="437ef-112">Property value</span></span>

<span data-ttu-id="437ef-113">Объект [**ивмтаск**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="437ef-113">The [**IVMTask**](ivmtask.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="437ef-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="437ef-114">Error codes</span></span>



| <span data-ttu-id="437ef-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="437ef-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="437ef-116">Значение</span><span class="sxs-lookup"><span data-stu-id="437ef-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="437ef-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="437ef-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="437ef-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="437ef-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="437ef-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="437ef-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="437ef-120">Параметр *задачи* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="437ef-120">The *task* parameter is **NULL**.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="437ef-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="437ef-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="437ef-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="437ef-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="437ef-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="437ef-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="437ef-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="437ef-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="437ef-125">Требования</span><span class="sxs-lookup"><span data-stu-id="437ef-125">Requirements</span></span>



| <span data-ttu-id="437ef-126">Требование</span><span class="sxs-lookup"><span data-stu-id="437ef-126">Requirement</span></span> | <span data-ttu-id="437ef-127">Значение</span><span class="sxs-lookup"><span data-stu-id="437ef-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="437ef-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="437ef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="437ef-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="437ef-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="437ef-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="437ef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="437ef-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="437ef-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="437ef-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="437ef-132">End of client support</span></span><br/>    | <span data-ttu-id="437ef-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="437ef-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="437ef-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="437ef-134">Product</span></span><br/>                  | <span data-ttu-id="437ef-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="437ef-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="437ef-136">Header</span><span class="sxs-lookup"><span data-stu-id="437ef-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="437ef-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="437ef-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="437ef-138">IID</span><span class="sxs-lookup"><span data-stu-id="437ef-138">IID</span></span><br/>                      | <span data-ttu-id="437ef-139">IID \_ ивмтаскколлектион определен как 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="437ef-139">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="437ef-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="437ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="437ef-141">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="437ef-141">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="437ef-142">**ивмтаскколлектион**</span><span class="sxs-lookup"><span data-stu-id="437ef-142">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

