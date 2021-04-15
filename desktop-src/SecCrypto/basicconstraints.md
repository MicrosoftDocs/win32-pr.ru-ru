---
description: Представляет расширение базовых ограничений сертификата.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Объект Басикконстраинтс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669081"
---
# <a name="basicconstraints-object"></a><span data-ttu-id="21a02-103">Объект Басикконстраинтс</span><span class="sxs-lookup"><span data-stu-id="21a02-103">BasicConstraints object</span></span>

<span data-ttu-id="21a02-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21a02-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="21a02-105">Вместо этого используйте [**класс X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="21a02-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="21a02-106">Объект **басикконстраинтс** представляет расширение базовых ограничений сертификата.</span><span class="sxs-lookup"><span data-stu-id="21a02-106">The **BasicConstraints** object represents the basic constraints extension of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="21a02-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="21a02-107">When to use</span></span>

<span data-ttu-id="21a02-108">Объект **басикконстраинтс** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="21a02-108">The **BasicConstraints** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="21a02-109">Определение наличия расширения базовых ограничений.</span><span class="sxs-lookup"><span data-stu-id="21a02-109">Determine whether the basic constraints extension is present.</span></span>
-   <span data-ttu-id="21a02-110">Определите, помечено ли расширение базовых ограничений как критическое.</span><span class="sxs-lookup"><span data-stu-id="21a02-110">Determine whether the basic constraints extension is marked critical.</span></span>
-   <span data-ttu-id="21a02-111">Определите, ограничен ли сертификат центрами сертификации.</span><span class="sxs-lookup"><span data-stu-id="21a02-111">Determine whether the certificate is constrained to certificate authorities.</span></span>
-   <span data-ttu-id="21a02-112">Определите, имеется ли ограничение длины пути, и получите значение ограничения длины пути.</span><span class="sxs-lookup"><span data-stu-id="21a02-112">Determine whether the path length constraint is present and retrieve the path length constraint value.</span></span>

## <a name="members"></a><span data-ttu-id="21a02-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="21a02-113">Members</span></span>

<span data-ttu-id="21a02-114">Объект **басикконстраинтс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="21a02-114">The **BasicConstraints** object has these types of members:</span></span>

-   [<span data-ttu-id="21a02-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="21a02-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21a02-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="21a02-116">Properties</span></span>

<span data-ttu-id="21a02-117">Объект **басикконстраинтс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="21a02-117">The **BasicConstraints** object has these properties.</span></span>



| <span data-ttu-id="21a02-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="21a02-118">Property</span></span>                                                                                     | <span data-ttu-id="21a02-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="21a02-119">Access type</span></span>          | <span data-ttu-id="21a02-120">Описание</span><span class="sxs-lookup"><span data-stu-id="21a02-120">Description</span></span>                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21a02-121">**исцертификатеаусорити**</span><span class="sxs-lookup"><span data-stu-id="21a02-121">**IsCertificateAuthority**</span></span>](basicconstraints-iscertificateauthority.md)<br/>         | <span data-ttu-id="21a02-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="21a02-122">Read-only</span></span><br/> | <span data-ttu-id="21a02-123">Возвращает логическое значение, указывающее, предназначен ли сертификат для [*центра сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="21a02-123">Retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span><br/> |
| [<span data-ttu-id="21a02-124">**Критическое**</span><span class="sxs-lookup"><span data-stu-id="21a02-124">**IsCritical**</span></span>](basicconstraints-iscritical.md)<br/>                                 | <span data-ttu-id="21a02-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="21a02-125">Read-only</span></span><br/> | <span data-ttu-id="21a02-126">Получает логическое значение, указывающее, помечено ли расширение базового ограничения как критическое.</span><span class="sxs-lookup"><span data-stu-id="21a02-126">Retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="21a02-127">**испасленконстраинтпресент**</span><span class="sxs-lookup"><span data-stu-id="21a02-127">**IsPathLenConstraintPresent**</span></span>](basicconstraints-ispathlenconstraintpresent.md)<br/> | <span data-ttu-id="21a02-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="21a02-128">Read-only</span></span><br/> | <span data-ttu-id="21a02-129">Получает логическое значение, указывающее, имеется ли ограничение длины пути сертификата.</span><span class="sxs-lookup"><span data-stu-id="21a02-129">Retrieves a Boolean value that indicates whether the certificate's path length constraint is present.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="21a02-130">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="21a02-130">**IsPresent**</span></span>](basicconstraints-ispresent.md)<br/>                                   | <span data-ttu-id="21a02-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="21a02-131">Read-only</span></span><br/> | <span data-ttu-id="21a02-132">Получает логическое значение, указывающее, имеется ли расширение базовых ограничений.</span><span class="sxs-lookup"><span data-stu-id="21a02-132">Retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="21a02-133">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="21a02-133">This is the default property.</span></span><br/>                                                                              |
| [<span data-ttu-id="21a02-134">**пасленконстраинт**</span><span class="sxs-lookup"><span data-stu-id="21a02-134">**PathLenConstraint**</span></span>](basicconstraints-pathlenconstraint.md)<br/>                   | <span data-ttu-id="21a02-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="21a02-135">Read-only</span></span><br/> | <span data-ttu-id="21a02-136">Возвращает значение ограничения длины пути.</span><span class="sxs-lookup"><span data-stu-id="21a02-136">Retrieves the value of the path length constraint.</span></span><br/>                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="21a02-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21a02-137">Remarks</span></span>

<span data-ttu-id="21a02-138">Не удается создать объект **басикконстраинтс** .</span><span class="sxs-lookup"><span data-stu-id="21a02-138">The **BasicConstraints** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="21a02-139">Требования</span><span class="sxs-lookup"><span data-stu-id="21a02-139">Requirements</span></span>



| <span data-ttu-id="21a02-140">Требование</span><span class="sxs-lookup"><span data-stu-id="21a02-140">Requirement</span></span> | <span data-ttu-id="21a02-141">Значение</span><span class="sxs-lookup"><span data-stu-id="21a02-141">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21a02-142">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="21a02-142">End of client support</span></span><br/> | <span data-ttu-id="21a02-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21a02-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="21a02-144">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="21a02-144">End of server support</span></span><br/> | <span data-ttu-id="21a02-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21a02-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="21a02-146">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="21a02-146">Redistributable</span></span><br/>       | <span data-ttu-id="21a02-147">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="21a02-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="21a02-148">DLL</span><span class="sxs-lookup"><span data-stu-id="21a02-148">DLL</span></span><br/>                   | <dl> <span data-ttu-id="21a02-149"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21a02-149"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a02-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21a02-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a02-151">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="21a02-151">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
