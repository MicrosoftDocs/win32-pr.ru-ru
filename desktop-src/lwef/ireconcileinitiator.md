---
title: Интерфейс ИреконЦилеинитиатор
description: Предоставляет методы, которые предоставляют средство согласования портфелей с средствами для уведомления инициатора о ходе выполнения, установки объекта завершения и запроса заданной версии документа. Инициатор отвечает за реализацию этого интерфейса.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Устаревшие функции среды Windows интерфейса ИреконЦилеинитиатор
- Интерфейс ИреконЦилеинитиатор устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802350"
---
# <a name="ireconcileinitiator-interface"></a><span data-ttu-id="4b028-106">Интерфейс ИреконЦилеинитиатор</span><span class="sxs-lookup"><span data-stu-id="4b028-106">IReconcileInitiator interface</span></span>

<span data-ttu-id="4b028-107">Предоставляет методы, которые предоставляют средство согласования портфелей с средствами для уведомления инициатора о ходе выполнения, установки объекта завершения и запроса заданной версии документа.</span><span class="sxs-lookup"><span data-stu-id="4b028-107">Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document.</span></span> <span data-ttu-id="4b028-108">Инициатор отвечает за реализацию этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4b028-108">The initiator is responsible for implementing this interface.</span></span>

## <a name="members"></a><span data-ttu-id="4b028-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="4b028-109">Members</span></span>

<span data-ttu-id="4b028-110">Интерфейс **иреконЦилеинитиатор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4b028-110">The **IReconcileInitiator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4b028-111">**ИреконЦилеинитиатор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b028-111">**IReconcileInitiator** also has these types of members:</span></span>

-   [<span data-ttu-id="4b028-112">Методы</span><span class="sxs-lookup"><span data-stu-id="4b028-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b028-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4b028-113">Methods</span></span>

<span data-ttu-id="4b028-114">Интерфейс **иреконЦилеинитиатор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4b028-114">The **IReconcileInitiator** interface has these methods.</span></span>



| <span data-ttu-id="4b028-115">Метод</span><span class="sxs-lookup"><span data-stu-id="4b028-115">Method</span></span>                                                                 | <span data-ttu-id="4b028-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4b028-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b028-117">**сетаборткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="4b028-117">**SetAbortCallback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | <span data-ttu-id="4b028-118">Задает объект, через который инициатор может асинхронно завершить выверку.</span><span class="sxs-lookup"><span data-stu-id="4b028-118">Sets the object through which the initiator can asynchronously terminate a reconciliation.</span></span> <span data-ttu-id="4b028-119">Синхронизатор портфеля обычно задает этот объект для выверки, которые имеют длину или требуют взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="4b028-119">A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="4b028-120">**сетпрогрессфидбакк**</span><span class="sxs-lookup"><span data-stu-id="4b028-120">**SetProgressFeedback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | <span data-ttu-id="4b028-121">Указывает объем хода выполнения, сделанный синхронизатором портфеля в отношении завершения сверки.</span><span class="sxs-lookup"><span data-stu-id="4b028-121">Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation.</span></span> <span data-ttu-id="4b028-122">Величина является дробной и вычислена как частное от параметров *улпрогресс* и *улпрогрессмакс* .</span><span class="sxs-lookup"><span data-stu-id="4b028-122">The amount is a fraction and is computed as the quotient of the *ulProgress* and *ulProgressMax* parameters.</span></span> <span data-ttu-id="4b028-123">Посредники должны периодически вызывать этот метод в процессе сверки.</span><span class="sxs-lookup"><span data-stu-id="4b028-123">Reconcilers should call this method periodically during their reconciliation process.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b028-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4b028-124">Requirements</span></span>



| <span data-ttu-id="4b028-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4b028-125">Requirement</span></span> | <span data-ttu-id="4b028-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4b028-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b028-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b028-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4b028-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b028-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="4b028-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b028-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4b028-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b028-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4b028-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4b028-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b028-132"><dt>Shell32.dll (версия 4,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4b028-132"><dt>Shell32.dll (version 4.0 or later)</dt></span></span> </dl> |



 

