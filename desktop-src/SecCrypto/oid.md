---
description: Представляет идентификатор объекта (OID), используемый несколькими свойствами CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: OID, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669456"
---
# <a name="oid-object"></a><span data-ttu-id="5d610-103">OID, объект</span><span class="sxs-lookup"><span data-stu-id="5d610-103">OID object</span></span>

<span data-ttu-id="5d610-104">\[Объект **OID** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="5d610-104">\[The **OID** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d610-105">Вместо этого используйте [**класс Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5d610-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5d610-106">Объект **OID** представляет [*идентификатор объекта*](../secgloss/o-gly.md) (OID), используемый несколькими свойствами CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="5d610-106">The **OID** object represents an [*object identifier*](../secgloss/o-gly.md) (OID) that is used by several CAPICOM properties.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5d610-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="5d610-107">When to use</span></span>

<span data-ttu-id="5d610-108">Объект **OID** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="5d610-108">The **OID** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5d610-109">Задайте или извлеките имя элемента CAPICOM и отображаемое имя для OID.</span><span class="sxs-lookup"><span data-stu-id="5d610-109">Set or retrieve a CAPICOM name and display name for the OID.</span></span>
-   <span data-ttu-id="5d610-110">Задайте или извлеките числовое значение OID.</span><span class="sxs-lookup"><span data-stu-id="5d610-110">Set or retrieve the dotted number for the OID.</span></span>

## <a name="members"></a><span data-ttu-id="5d610-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="5d610-111">Members</span></span>

<span data-ttu-id="5d610-112">Объект **OID** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5d610-112">The **OID** object has these types of members:</span></span>

-   [<span data-ttu-id="5d610-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d610-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d610-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d610-114">Properties</span></span>

<span data-ttu-id="5d610-115">Объект **OID** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="5d610-115">The **OID** object has these properties.</span></span>



| <span data-ttu-id="5d610-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="5d610-116">Property</span></span>                                            | <span data-ttu-id="5d610-117">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="5d610-117">Access type</span></span>           | <span data-ttu-id="5d610-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5d610-118">Description</span></span>                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d610-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="5d610-119">**FriendlyName**</span></span>](oid-friendlyname.md)<br/> | <span data-ttu-id="5d610-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="5d610-120">Read/write</span></span><br/> | <span data-ttu-id="5d610-121">Задает или получает отображаемое имя для OID.</span><span class="sxs-lookup"><span data-stu-id="5d610-121">Sets or retrieves the display name for the OID.</span></span><br/>                                       |
| [<span data-ttu-id="5d610-122">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5d610-122">**Name**</span></span>](oid-name.md)<br/>                 | <span data-ttu-id="5d610-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="5d610-123">Read/write</span></span><br/> | <span data-ttu-id="5d610-124">Задает или получает имя объекта, определенное с помощью элемента CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="5d610-124">Sets or retrieves the CAPICOM-defined name for the OID.</span></span> <span data-ttu-id="5d610-125">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d610-125">This is the default property.</span></span><br/> |
| [<span data-ttu-id="5d610-126">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5d610-126">**Value**</span></span>](oid-value.md)<br/>               | <span data-ttu-id="5d610-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="5d610-127">Read/write</span></span><br/> | <span data-ttu-id="5d610-128">Задает или получает значение номера OID, разделенного OID.</span><span class="sxs-lookup"><span data-stu-id="5d610-128">Sets or retrieves the value of the OID dotted number of the OID.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="5d610-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d610-129">Remarks</span></span>

<span data-ttu-id="5d610-130">Объект **OID** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="5d610-130">The **OID** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="5d610-131">ProgID для объекта **OID** — CAPICOM. OID. 1.</span><span class="sxs-lookup"><span data-stu-id="5d610-131">The ProgID for the **OID** object is CAPICOM.OID.1.</span></span>

<span data-ttu-id="5d610-132">Следующие свойства элемента CAPICOM возвращают объект **OID** :</span><span class="sxs-lookup"><span data-stu-id="5d610-132">The following CAPICOM object properties return an **OID** object:</span></span>

-   [<span data-ttu-id="5d610-133">**Полициинформатион. OID**</span><span class="sxs-lookup"><span data-stu-id="5d610-133">**PolicyInformation.OID**</span></span>](policyinformation-oid.md)
-   [<span data-ttu-id="5d610-134">**Квалификатор. OID**</span><span class="sxs-lookup"><span data-stu-id="5d610-134">**Qualifier.OID**</span></span>](qualifier-oid.md)
-   [<span data-ttu-id="5d610-135">**Extension. OID**</span><span class="sxs-lookup"><span data-stu-id="5d610-135">**Extension.OID**</span></span>](extension-oid.md)
-   [<span data-ttu-id="5d610-136">**Template. OID**</span><span class="sxs-lookup"><span data-stu-id="5d610-136">**Template.OID**</span></span>](template-oid.md)

## <a name="requirements"></a><span data-ttu-id="5d610-137">Требования</span><span class="sxs-lookup"><span data-stu-id="5d610-137">Requirements</span></span>



| <span data-ttu-id="5d610-138">Требование</span><span class="sxs-lookup"><span data-stu-id="5d610-138">Requirement</span></span> | <span data-ttu-id="5d610-139">Значение</span><span class="sxs-lookup"><span data-stu-id="5d610-139">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d610-140">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="5d610-140">Redistributable</span></span><br/> | <span data-ttu-id="5d610-141">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d610-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5d610-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5d610-142">DLL</span></span><br/>             | <dl> <span data-ttu-id="5d610-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d610-143"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
