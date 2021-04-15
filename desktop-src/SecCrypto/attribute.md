---
description: Представляет отдельный атрибут, прошедший проверку подлинности.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669301"
---
# <a name="attribute-object"></a><span data-ttu-id="4e9ba-103">Attribute, объект</span><span class="sxs-lookup"><span data-stu-id="4e9ba-103">Attribute object</span></span>

<span data-ttu-id="4e9ba-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="4e9ba-105">Вместо этого используйте [**класс криптографикаттрибутеобжект**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="4e9ba-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="4e9ba-106">Объект **атрибута** представляет один атрибут, прошедший проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-106">The **Attribute** object represents a single authenticated attribute.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4e9ba-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="4e9ba-107">When to use</span></span>

<span data-ttu-id="4e9ba-108">Объект **атрибута** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="4e9ba-108">The **Attribute** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4e9ba-109">Задайте или извлеките имя элемента CAPICOM атрибута.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-109">Set or retrieve the CAPICOM name of the attribute.</span></span>
-   <span data-ttu-id="4e9ba-110">Задайте или получите значение атрибута, например время подписи, имя подписанного документа или описание документа, подписанного.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-110">Set or retrieve the value of the attribute, such as signing time, the name of the document signed, or a description of the document signed.</span></span>

## <a name="members"></a><span data-ttu-id="4e9ba-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="4e9ba-111">Members</span></span>

<span data-ttu-id="4e9ba-112">Объект **атрибута** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4e9ba-112">The **Attribute** object has these types of members:</span></span>

-   [<span data-ttu-id="4e9ba-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e9ba-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e9ba-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e9ba-114">Properties</span></span>

<span data-ttu-id="4e9ba-115">Объект **атрибута** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-115">The **Attribute** object has these properties.</span></span>



| <span data-ttu-id="4e9ba-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="4e9ba-116">Property</span></span>                                    | <span data-ttu-id="4e9ba-117">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="4e9ba-117">Access type</span></span>           | <span data-ttu-id="4e9ba-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4e9ba-118">Description</span></span>                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e9ba-119">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4e9ba-119">**Name**</span></span>](attribute-name.md)<br/>   | <span data-ttu-id="4e9ba-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4e9ba-120">Read/write</span></span><br/> | <span data-ttu-id="4e9ba-121">Задает или получает имя элемента CAPICOM атрибута.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-121">Sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="4e9ba-122">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-122">This is the default property.</span></span><br/> |
| [<span data-ttu-id="4e9ba-123">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4e9ba-123">**Value**</span></span>](attribute-value.md)<br/> | <span data-ttu-id="4e9ba-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4e9ba-124">Read/write</span></span><br/> | <span data-ttu-id="4e9ba-125">Задает или получает значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-125">Sets or retrieves the value of the attribute.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="4e9ba-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e9ba-126">Remarks</span></span>

<span data-ttu-id="4e9ba-127">Объект **атрибута** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-127">The **Attribute** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="4e9ba-128">ProgID для объекта **атрибута** — CAPICOM. Атрибут. 1.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-128">The ProgID for the **Attribute** object is CAPICOM.Attribute.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9ba-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4e9ba-129">Requirements</span></span>



| <span data-ttu-id="4e9ba-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4e9ba-130">Requirement</span></span> | <span data-ttu-id="4e9ba-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4e9ba-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9ba-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4e9ba-132">End of client support</span></span><br/> | <span data-ttu-id="4e9ba-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e9ba-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4e9ba-134">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4e9ba-134">End of server support</span></span><br/> | <span data-ttu-id="4e9ba-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e9ba-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4e9ba-136">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4e9ba-136">Redistributable</span></span><br/>       | <span data-ttu-id="4e9ba-137">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="4e9ba-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4e9ba-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4e9ba-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4e9ba-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e9ba-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e9ba-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e9ba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9ba-141">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="4e9ba-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
