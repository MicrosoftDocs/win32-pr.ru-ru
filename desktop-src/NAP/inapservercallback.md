---
title: Интерфейс Инапсерверкаллбакк (Напсистемхеалсвалидатор. h)
description: SHV используют для сигнализации завершения асинхронного запроса.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- Инапсерверкаллбакк интерфейса NAP
- Инапсерверкаллбакк интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489159"
---
# <a name="inapservercallback-interface"></a><span data-ttu-id="a2fcf-105">Интерфейс Инапсерверкаллбакк</span><span class="sxs-lookup"><span data-stu-id="a2fcf-105">INapServerCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="a2fcf-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="a2fcf-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a2fcf-107">**Инапсерверкаллбакк** предоставляет метод, который SHV использует для сигнализации завершения асинхронного запроса.</span><span class="sxs-lookup"><span data-stu-id="a2fcf-107">The **INapServerCallback** provides a method that SHVs use to signal asynchronous request completion.</span></span>

## <a name="members"></a><span data-ttu-id="a2fcf-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="a2fcf-108">Members</span></span>

<span data-ttu-id="a2fcf-109">Интерфейс **инапсерверкаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a2fcf-109">The **INapServerCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a2fcf-110">**Инапсерверкаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a2fcf-110">**INapServerCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="a2fcf-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a2fcf-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a2fcf-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a2fcf-112">Methods</span></span>

<span data-ttu-id="a2fcf-113">Интерфейс **инапсерверкаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a2fcf-113">The **INapServerCallback** interface has these methods.</span></span>



| <span data-ttu-id="a2fcf-114">Метод</span><span class="sxs-lookup"><span data-stu-id="a2fcf-114">Method</span></span>                                                                         | <span data-ttu-id="a2fcf-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a2fcf-115">Description</span></span>                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="a2fcf-116">**Инапсерверкаллбакк:: OnComplete**</span><span class="sxs-lookup"><span data-stu-id="a2fcf-116">**INapServerCallback::OnComplete**</span></span>](inapservercallback-oncomplete-method.md) | <span data-ttu-id="a2fcf-117">Используется SHV для сигнализации о завершении асинхронного запроса.</span><span class="sxs-lookup"><span data-stu-id="a2fcf-117">Used by SHVs to signal asynchronous request completion.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a2fcf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a2fcf-118">Requirements</span></span>



| <span data-ttu-id="a2fcf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a2fcf-119">Requirement</span></span> | <span data-ttu-id="a2fcf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a2fcf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fcf-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2fcf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fcf-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a2fcf-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="a2fcf-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2fcf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fcf-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2fcf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2fcf-125">Header</span><span class="sxs-lookup"><span data-stu-id="a2fcf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2fcf-126"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2fcf-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2fcf-127">IDL</span><span class="sxs-lookup"><span data-stu-id="a2fcf-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2fcf-128"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2fcf-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="a2fcf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a2fcf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2fcf-130"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2fcf-130"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="a2fcf-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2fcf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fcf-132">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="a2fcf-132">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a2fcf-133">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="a2fcf-133">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

