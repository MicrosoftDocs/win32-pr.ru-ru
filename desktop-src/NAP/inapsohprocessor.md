---
title: Интерфейс Инапсохпроцессор (Наппротокол. h)
description: Используются SHA для обработки содержимого Сохреспонсес и SHV для обработки содержимого Сохрекуестс.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- Инапсохпроцессор интерфейса NAP
- Инапсохпроцессор интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071148"
---
# <a name="inapsohprocessor-interface"></a><span data-ttu-id="ee6d0-105">Интерфейс Инапсохпроцессор</span><span class="sxs-lookup"><span data-stu-id="ee6d0-105">INapSoHProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="ee6d0-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="ee6d0-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ee6d0-107">**Инапсохпроцессор** предоставляет методы, используемые SHA для обработки содержимого [**сохреспонсес**](/windows/win32/api/naptypes/ns-naptypes-soh) и SHV для обработки содержимого **сохрекуестс**.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-107">The **INapSoHProcessor** provides methods that are used by SHAs to process the contents of [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to process the contents of **SoHRequests**.</span></span>

## <a name="members"></a><span data-ttu-id="ee6d0-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="ee6d0-108">Members</span></span>

<span data-ttu-id="ee6d0-109">Интерфейс **инапсохпроцессор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ee6d0-109">The **INapSoHProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ee6d0-110">**Инапсохпроцессор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ee6d0-110">**INapSoHProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="ee6d0-111">Методы</span><span class="sxs-lookup"><span data-stu-id="ee6d0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ee6d0-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ee6d0-112">Methods</span></span>

<span data-ttu-id="ee6d0-113">Интерфейс **инапсохпроцессор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-113">The **INapSoHProcessor** interface has these methods.</span></span>



| <span data-ttu-id="ee6d0-114">Метод</span><span class="sxs-lookup"><span data-stu-id="ee6d0-114">Method</span></span>                                                                                           | <span data-ttu-id="ee6d0-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ee6d0-115">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee6d0-116">**Инапсохпроцессор:: Финднекстаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="ee6d0-116">**INapSoHProcessor::FindNextAttribute**</span></span>](inapsohprocessor-findnextattribute-method.md)         | <span data-ttu-id="ee6d0-117">Находит индекс расположения следующего атрибута пакета SoH.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-117">Finds the location index of the next SoH packet attribute.</span></span><br/>                 |
| [<span data-ttu-id="ee6d0-118">**Инапсохпроцессор:: OutAttribute**</span><span class="sxs-lookup"><span data-stu-id="ee6d0-118">**INapSoHProcessor::GetAttribute**</span></span>](inapsohprocessor-getattribute-method.md)                   | <span data-ttu-id="ee6d0-119">Извлекает тип и значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-119">Retrieves the attribute type and value.</span></span><br/>                                    |
| [<span data-ttu-id="ee6d0-120">**Инапсохпроцессор:: Жетнумберофаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="ee6d0-120">**INapSoHProcessor::GetNumberOfAttributes**</span></span>](inapsohprocessor-getnumberofattributes-method.md) | <span data-ttu-id="ee6d0-121">Извлекает количество атрибутов, содержащихся в SoH.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-121">Retrieves the number of attributes contained in the SoH.</span></span><br/>                   |
| [<span data-ttu-id="ee6d0-122">**Инапсохпроцессор:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="ee6d0-122">**INapSoHProcessor::Initialize**</span></span>](inapsohprocessor-initialize-method.md)                       | <span data-ttu-id="ee6d0-123">Инициализирует пакет протокола SoH и систему защиты доступа к сети для обработки содержимого.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-123">Initializes the SoH protocol packet and NAP System for content processing.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ee6d0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ee6d0-124">Requirements</span></span>



| <span data-ttu-id="ee6d0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ee6d0-125">Requirement</span></span> | <span data-ttu-id="ee6d0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ee6d0-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee6d0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee6d0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ee6d0-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee6d0-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee6d0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee6d0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ee6d0-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee6d0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ee6d0-131">Header</span><span class="sxs-lookup"><span data-stu-id="ee6d0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee6d0-132"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee6d0-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee6d0-133">IDL</span><span class="sxs-lookup"><span data-stu-id="ee6d0-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee6d0-134"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee6d0-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="ee6d0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ee6d0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee6d0-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee6d0-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ee6d0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee6d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee6d0-138">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="ee6d0-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ee6d0-139">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="ee6d0-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

