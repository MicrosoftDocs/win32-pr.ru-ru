---
title: Константы WINBIO_IDENTITY_TYPE (Винбио \_ types. h)
description: Укажите формат сведений об удостоверении, содержащихся в \_ структуре удостоверений винбио.
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988428"
---
# <a name="winbio_identity_type-constants"></a><span data-ttu-id="efc93-103">\_ \_ Константы типа идентификатора винбио</span><span class="sxs-lookup"><span data-stu-id="efc93-103">WINBIO\_IDENTITY\_TYPE Constants</span></span>

<span data-ttu-id="efc93-104">Для указания формата сведений об удостоверении, содержащихся в структуре [**\_ удостоверений винбио**](winbio-identity.md) , можно использовать следующие константы **\_ \_ типа идентификатора винбио** .</span><span class="sxs-lookup"><span data-stu-id="efc93-104">The following **WINBIO\_IDENTITY\_TYPE** constants can be used to specify the format of the identity information contained in the [**WINBIO\_IDENTITY**](winbio-identity.md) structure.</span></span>



| <span data-ttu-id="efc93-105">Константа</span><span class="sxs-lookup"><span data-stu-id="efc93-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="efc93-106">Описание</span><span class="sxs-lookup"><span data-stu-id="efc93-106">Description</span></span>                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="efc93-107"><dt>**\_тип идентификатора \_ винбио \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="efc93-107"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="efc93-108">Шаблон не имеет связанного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="efc93-108">The template has no associated ID.</span></span> <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="efc93-109"><dt>**\_ \_ шаблон типа идентификатора \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="efc93-109"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="efc93-110">Структура соответствует всем удостоверениям шаблона.</span><span class="sxs-lookup"><span data-stu-id="efc93-110">The structure matches all template identities.</span></span><br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="efc93-111"><dt>**\_ \_ GUID типа идентификатора \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="efc93-111"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="efc93-112">Идентификатор GUID идентифицирует шаблон.</span><span class="sxs-lookup"><span data-stu-id="efc93-112">A GUID identifies the template.</span></span><br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="efc93-113"><dt>**ИД \_ \_ безопасности типа \_ идентификатора винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="efc93-113"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="efc93-114">Идентификатор безопасности учетной записи идентифицирует шаблон.</span><span class="sxs-lookup"><span data-stu-id="efc93-114">An account SID identifies the template.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="efc93-115">Требования</span><span class="sxs-lookup"><span data-stu-id="efc93-115">Requirements</span></span>



| <span data-ttu-id="efc93-116">Требование</span><span class="sxs-lookup"><span data-stu-id="efc93-116">Requirement</span></span> | <span data-ttu-id="efc93-117">Значение</span><span class="sxs-lookup"><span data-stu-id="efc93-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efc93-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efc93-118">Minimum supported client</span></span><br/> | <span data-ttu-id="efc93-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="efc93-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="efc93-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efc93-120">Minimum supported server</span></span><br/> | <span data-ttu-id="efc93-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="efc93-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="efc93-122">Header</span><span class="sxs-lookup"><span data-stu-id="efc93-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="efc93-123"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efc93-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc93-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efc93-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc93-125">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="efc93-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="efc93-126">**\_удостоверение винбио**</span><span class="sxs-lookup"><span data-stu-id="efc93-126">**WINBIO\_IDENTITY**</span></span>](winbio-identity.md)
</dt> </dl>

 

 





