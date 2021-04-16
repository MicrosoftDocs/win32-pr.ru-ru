---
description: Задает или получает имя элемента CAPICOM атрибута. Это свойство по умолчанию.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Attribute.Name, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665191"
---
# <a name="attributename-property"></a><span data-ttu-id="e890a-104">Attribute.Name, свойство</span><span class="sxs-lookup"><span data-stu-id="e890a-104">Attribute.Name property</span></span>

<span data-ttu-id="e890a-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e890a-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="e890a-106">Вместо этого используйте [**класс криптографикаттрибутеобжект**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="e890a-106">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="e890a-107">Свойство **Name** задает или получает имя элемента CAPICOM атрибута.</span><span class="sxs-lookup"><span data-stu-id="e890a-107">The **Name** property sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="e890a-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e890a-108">This is the default property.</span></span>

<span data-ttu-id="e890a-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e890a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e890a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e890a-110">Syntax</span></span>


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a><span data-ttu-id="e890a-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e890a-111">Property value</span></span>

<span data-ttu-id="e890a-112">Значение перечисления [**\_ атрибутов CAPICOM**](capicom-attribute.md) , которое указывает CAPICOM-имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="e890a-112">A value of the [**CAPICOM\_ATTRIBUTE**](capicom-attribute.md) enumeration that specifies the CAPICOM name of the attribute.</span></span> <span data-ttu-id="e890a-113">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="e890a-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="e890a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e890a-114">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="e890a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e890a-115">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <span data-ttu-id="e890a-116"><dt>**\_время подписи CAPICOM проверенного \_ атрибута \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e890a-116"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</dt></span></span> </dl>                         | <span data-ttu-id="e890a-117">Атрибут содержит время создания подписи.</span><span class="sxs-lookup"><span data-stu-id="e890a-117">The attribute contains the time that the signature was created.</span></span><br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <span data-ttu-id="e890a-118"><dt>**\_ \_ \_ имя документа атрибута CAPICOM, прошедшего проверку подлинности \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e890a-118"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</dt></span></span> </dl>                      | <span data-ttu-id="e890a-119">Атрибут содержит имя подписанного документа.</span><span class="sxs-lookup"><span data-stu-id="e890a-119">The attribute contains the name of the signed document.</span></span><br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <span data-ttu-id="e890a-120"><dt>**\_ \_ \_ описание документа атрибута CAPICOM, прошедшего проверку подлинности \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e890a-120"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</dt></span></span> </dl> | <span data-ttu-id="e890a-121">Атрибут содержит описание подписанного документа.</span><span class="sxs-lookup"><span data-stu-id="e890a-121">The attribute contains a description of the signed document.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="e890a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e890a-122">Remarks</span></span>

<span data-ttu-id="e890a-123">Когда значение этого свойства сбрасывается прямо или косвенно, полное состояние объекта сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="e890a-123">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="e890a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e890a-124">Requirements</span></span>



| <span data-ttu-id="e890a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e890a-125">Requirement</span></span> | <span data-ttu-id="e890a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e890a-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e890a-127">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e890a-127">End of client support</span></span><br/> | <span data-ttu-id="e890a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e890a-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e890a-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e890a-129">End of server support</span></span><br/> | <span data-ttu-id="e890a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e890a-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e890a-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e890a-131">Redistributable</span></span><br/>       | <span data-ttu-id="e890a-132">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e890a-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e890a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e890a-133">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e890a-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e890a-134"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e890a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e890a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e890a-136">**attribute**</span><span class="sxs-lookup"><span data-stu-id="e890a-136">**Attribute**</span></span>](attribute.md)
</dt> </dl>

 

 
