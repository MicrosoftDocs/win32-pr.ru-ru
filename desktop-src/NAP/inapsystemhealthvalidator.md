---
title: Интерфейс Инапсистемхеалсвалидатор (Напсистемхеалсвалидатор. h)
description: Должен быть реализован разработчиками SHV, чтобы обеспечить взаимодействие системы защиты доступа к сети с SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- Инапсистемхеалсвалидатор интерфейса NAP
- Инапсистемхеалсвалидатор интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801828"
---
# <a name="inapsystemhealthvalidator-interface"></a><span data-ttu-id="8c0c8-105">Интерфейс Инапсистемхеалсвалидатор</span><span class="sxs-lookup"><span data-stu-id="8c0c8-105">INapSystemHealthValidator interface</span></span>

> [!Note]  
> <span data-ttu-id="8c0c8-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="8c0c8-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8c0c8-107">**Инапсистемхеалсвалидатор** предоставляет методы, которые должны быть реализованы РАЗРАБОТЧИКами SHV, чтобы обеспечить взаимодействие системы защиты доступа к сети с SHV.</span><span class="sxs-lookup"><span data-stu-id="8c0c8-107">The **INapSystemHealthValidator** provides methods that must be implemented by SHV developers to enable the NAP system to communicate with an SHV.</span></span>

## <a name="members"></a><span data-ttu-id="8c0c8-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="8c0c8-108">Members</span></span>

<span data-ttu-id="8c0c8-109">Интерфейс **инапсистемхеалсвалидатор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8c0c8-109">The **INapSystemHealthValidator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8c0c8-110">**Инапсистемхеалсвалидатор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8c0c8-110">**INapSystemHealthValidator** also has these types of members:</span></span>

-   [<span data-ttu-id="8c0c8-111">Методы</span><span class="sxs-lookup"><span data-stu-id="8c0c8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8c0c8-112">Методы</span><span class="sxs-lookup"><span data-stu-id="8c0c8-112">Methods</span></span>

<span data-ttu-id="8c0c8-113">Интерфейс **инапсистемхеалсвалидатор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8c0c8-113">The **INapSystemHealthValidator** interface has these methods.</span></span>



| <span data-ttu-id="8c0c8-114">Метод</span><span class="sxs-lookup"><span data-stu-id="8c0c8-114">Method</span></span>                                                                                   | <span data-ttu-id="8c0c8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="8c0c8-115">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c0c8-116">**Инапсистемхеалсвалидатор:: Validate**</span><span class="sxs-lookup"><span data-stu-id="8c0c8-116">**INapSystemHealthValidator::Validate**</span></span>](inapsystemhealthvalidator-validate-method.md) | <span data-ttu-id="8c0c8-117">Система защиты доступа к сети вызывает этот определенный приложением метод для проверки [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , полученного от клиента.</span><span class="sxs-lookup"><span data-stu-id="8c0c8-117">The NAP system calls this application defined method to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="8c0c8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8c0c8-118">Requirements</span></span>



| <span data-ttu-id="8c0c8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8c0c8-119">Requirement</span></span> | <span data-ttu-id="8c0c8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8c0c8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0c8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c0c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0c8-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8c0c8-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="8c0c8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c0c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0c8-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c0c8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c0c8-125">Header</span><span class="sxs-lookup"><span data-stu-id="8c0c8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c0c8-126"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c8-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c0c8-127">IDL</span><span class="sxs-lookup"><span data-stu-id="8c0c8-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8c0c8-128"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c8-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0c8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c0c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0c8-130">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="8c0c8-130">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8c0c8-131">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="8c0c8-131">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

