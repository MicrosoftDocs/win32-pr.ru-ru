---
title: Интерфейс Инапсохконструктор (Наппротокол. h)
description: Используются SHA для создания Сохрекуестс и SHV для создания Сохреспонсес.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- Инапсохконструктор интерфейса NAP
- Инапсохконструктор интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988256"
---
# <a name="inapsohconstructor-interface"></a><span data-ttu-id="63b71-105">Интерфейс Инапсохконструктор</span><span class="sxs-lookup"><span data-stu-id="63b71-105">INapSoHConstructor interface</span></span>

> [!Note]  
> <span data-ttu-id="63b71-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="63b71-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="63b71-107">**Инапсохконструктор** предоставляет методы, используемые SHA для создания [**сохрекуестс**](/windows/win32/api/naptypes/ns-naptypes-soh) и SHV для создания **сохреспонсес**.</span><span class="sxs-lookup"><span data-stu-id="63b71-107">The **INapSoHConstructor** provides methods that are used by SHAs to construct [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to construct **SoHResponses**.</span></span>

## <a name="members"></a><span data-ttu-id="63b71-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="63b71-108">Members</span></span>

<span data-ttu-id="63b71-109">Интерфейс **инапсохконструктор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="63b71-109">The **INapSoHConstructor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="63b71-110">**Инапсохконструктор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="63b71-110">**INapSoHConstructor** also has these types of members:</span></span>

-   [<span data-ttu-id="63b71-111">Методы</span><span class="sxs-lookup"><span data-stu-id="63b71-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="63b71-112">Методы</span><span class="sxs-lookup"><span data-stu-id="63b71-112">Methods</span></span>

<span data-ttu-id="63b71-113">Интерфейс **инапсохконструктор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="63b71-113">The **INapSoHConstructor** interface has these methods.</span></span>



| <span data-ttu-id="63b71-114">Метод</span><span class="sxs-lookup"><span data-stu-id="63b71-114">Method</span></span>                                                                                   | <span data-ttu-id="63b71-115">Описание</span><span class="sxs-lookup"><span data-stu-id="63b71-115">Description</span></span>                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [<span data-ttu-id="63b71-116">**Инапсохконструктор:: Аппендаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="63b71-116">**INapSoHConstructor::AppendAttribute**</span></span>](inapsohconstructor-appendattribute-method.md) | <span data-ttu-id="63b71-117">Добавляет TLV в конец буфера SoH.</span><span class="sxs-lookup"><span data-stu-id="63b71-117">Adds a TLV to the end of the SoH buffer.</span></span><br/> |
| [<span data-ttu-id="63b71-118">**Инапсохконструктор:: Жетсох**</span><span class="sxs-lookup"><span data-stu-id="63b71-118">**INapSoHConstructor::GetSoH**</span></span>](inapsohconstructor-getsoh-method.md)                   | <span data-ttu-id="63b71-119">Извлекает сконструированный пакет SoH.</span><span class="sxs-lookup"><span data-stu-id="63b71-119">Retrieves the constructed SoH packet.</span></span><br/>    |
| [<span data-ttu-id="63b71-120">**Инапсохконструктор:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="63b71-120">**INapSoHConstructor::Initialize**</span></span>](inapsohconstructor-initialize-method.md)           | <span data-ttu-id="63b71-121">Инициализирует пакет SoH.</span><span class="sxs-lookup"><span data-stu-id="63b71-121">Initializes the SoH packet.</span></span><br/>              |
| [<span data-ttu-id="63b71-122">**Инапсохконструктор:: Validate**</span><span class="sxs-lookup"><span data-stu-id="63b71-122">**INapSoHConstructor::Validate**</span></span>](inapsohconstructor-validate-method.md)               | <span data-ttu-id="63b71-123">Проверяет допустимость пакета SoH.</span><span class="sxs-lookup"><span data-stu-id="63b71-123">Checks the validity of the SoH packet.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="63b71-124">Требования</span><span class="sxs-lookup"><span data-stu-id="63b71-124">Requirements</span></span>



| <span data-ttu-id="63b71-125">Требование</span><span class="sxs-lookup"><span data-stu-id="63b71-125">Requirement</span></span> | <span data-ttu-id="63b71-126">Значение</span><span class="sxs-lookup"><span data-stu-id="63b71-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b71-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63b71-127">Minimum supported client</span></span><br/> | <span data-ttu-id="63b71-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63b71-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="63b71-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63b71-129">Minimum supported server</span></span><br/> | <span data-ttu-id="63b71-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63b71-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="63b71-131">Header</span><span class="sxs-lookup"><span data-stu-id="63b71-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b71-132"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b71-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="63b71-133">IDL</span><span class="sxs-lookup"><span data-stu-id="63b71-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63b71-134"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63b71-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="63b71-135">DLL</span><span class="sxs-lookup"><span data-stu-id="63b71-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63b71-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63b71-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="63b71-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63b71-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b71-138">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="63b71-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="63b71-139">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="63b71-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

