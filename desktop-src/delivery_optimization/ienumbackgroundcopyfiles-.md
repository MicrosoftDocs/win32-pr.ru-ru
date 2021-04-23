---
title: Интерфейс Иенумбаккграундкопифилес (Deliveryoptimization. h)
description: Используйте интерфейс Иенумбаккграундкопифилес для перечисления файлов, содержащихся в задании. Чтобы получить указатель интерфейса Иенумбаккграундкопифилес, вызовите метод использованием метода ibackgroundcopyjob Енумфилес.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Интерфейс Иенумбаккграундкопифилес
- Интерфейс Иенумбаккграундкопифилес, описание
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710493"
---
# <a name="ienumbackgroundcopyfiles-interface"></a><span data-ttu-id="3c460-106">Интерфейс Иенумбаккграундкопифилес</span><span class="sxs-lookup"><span data-stu-id="3c460-106">IEnumBackgroundCopyFiles interface</span></span>

<span data-ttu-id="3c460-107">Используйте интерфейс **иенумбаккграундкопифилес** для перечисления файлов, содержащихся в задании.</span><span class="sxs-lookup"><span data-stu-id="3c460-107">Use the **IEnumBackgroundCopyFiles** interface to enumerate the files that a job contains.</span></span> <span data-ttu-id="3c460-108">Чтобы получить указатель интерфейса **иенумбаккграундкопифилес** , вызовите метод [**использованием метода ibackgroundcopyjob:: енумфилес**](ibackgroundcopyjob-enumfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="3c460-108">To get an **IEnumBackgroundCopyFiles** interface pointer, call the [**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="3c460-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="3c460-109">Members</span></span>

<span data-ttu-id="3c460-110">Интерфейс **иенумбаккграундкопифилес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3c460-110">The **IEnumBackgroundCopyFiles** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3c460-111">**Иенумбаккграундкопифилес** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3c460-111">**IEnumBackgroundCopyFiles** also has these types of members:</span></span>

-   [<span data-ttu-id="3c460-112">Методы</span><span class="sxs-lookup"><span data-stu-id="3c460-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3c460-113">Методы</span><span class="sxs-lookup"><span data-stu-id="3c460-113">Methods</span></span>

<span data-ttu-id="3c460-114">Интерфейс **иенумбаккграундкопифилес** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3c460-114">The **IEnumBackgroundCopyFiles** interface has these methods.</span></span>



| <span data-ttu-id="3c460-115">Метод</span><span class="sxs-lookup"><span data-stu-id="3c460-115">Method</span></span>                                                | <span data-ttu-id="3c460-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3c460-116">Description</span></span>                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="3c460-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="3c460-117">**GetCount**</span></span>](ienumbackgroundcopyfiles-getcount.md) | <span data-ttu-id="3c460-118">Извлекает количество элементов в перечислении.</span><span class="sxs-lookup"><span data-stu-id="3c460-118">Retrieves the number of items in the enumeration.</span></span><br/>                  |
| [<span data-ttu-id="3c460-119">**Далее**</span><span class="sxs-lookup"><span data-stu-id="3c460-119">**Next**</span></span>](ienumbackgroundcopyfiles-next.md)         | <span data-ttu-id="3c460-120">Возвращает заданное число элементов последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="3c460-120">Retrieves a specified number of items in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="3c460-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="3c460-121">**Reset**</span></span>](ienumbackgroundcopyfiles-reset.md)       | <span data-ttu-id="3c460-122">Сбрасывает последовательность перечисления в начало.</span><span class="sxs-lookup"><span data-stu-id="3c460-122">Resets the enumeration sequence to the beginning.</span></span><br/>                  |
| [<span data-ttu-id="3c460-123">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="3c460-123">**Skip**</span></span>](ienumbackgroundcopyfiles-skip.md)         | <span data-ttu-id="3c460-124">Пропускает заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="3c460-124">Skips a specified number of items in the enumeration sequence.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="3c460-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3c460-125">Requirements</span></span>



| <span data-ttu-id="3c460-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3c460-126">Requirement</span></span> | <span data-ttu-id="3c460-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3c460-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c460-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c460-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3c460-129">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="3c460-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3c460-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c460-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3c460-131">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="3c460-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3c460-132">Header</span><span class="sxs-lookup"><span data-stu-id="3c460-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c460-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c460-133"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c460-134">IDL</span><span class="sxs-lookup"><span data-stu-id="3c460-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c460-135"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c460-135"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3c460-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c460-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c460-137"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c460-137"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3c460-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3c460-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c460-139"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c460-139"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3c460-140">IID</span><span class="sxs-lookup"><span data-stu-id="3c460-140">IID</span></span><br/>                      | <span data-ttu-id="3c460-141">IID_IEnumBackgroundCopyFiles определен как CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="3c460-141">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3c460-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c460-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c460-143">**Использованием метода ibackgroundcopyjob:: Енумфилес**</span><span class="sxs-lookup"><span data-stu-id="3c460-143">**IBackgroundCopyJob::EnumFiles**</span></span>](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

