---
description: Указывает расположение для поиска Active Directory хранилище сертификатов.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Перечисление CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665354"
---
# <a name="capicom_active_directory_search_location-enumeration"></a><span data-ttu-id="a01bc-103">\_ \_ \_ \_ Перечисление расположения поиска CAPICOM Active Directory</span><span class="sxs-lookup"><span data-stu-id="a01bc-103">CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION enumeration</span></span>

<span data-ttu-id="a01bc-104">Тип перечисления **CAPICOM \_ Active \_ Directory \_ Search \_** указывает расположение для поиска Active Directory [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a01bc-104">The **CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION** enumeration type indicates the location to be searched for an Active Directory [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="a01bc-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="a01bc-105">Members</span></span>



| <span data-ttu-id="a01bc-106">Член</span><span class="sxs-lookup"><span data-stu-id="a01bc-106">Member</span></span>                               | <span data-ttu-id="a01bc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a01bc-107">Description</span></span>                                  | <span data-ttu-id="a01bc-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a01bc-108">Value</span></span> |
|--------------------------------------|----------------------------------------------|-------|
| <span data-ttu-id="a01bc-109">**CAPICOM \_ Поиск \_**</span><span class="sxs-lookup"><span data-stu-id="a01bc-109">**CAPICOM\_SEARCH\_ANY**</span></span>             | <span data-ttu-id="a01bc-110">Выполняет поиск во всех доступных расположениях.</span><span class="sxs-lookup"><span data-stu-id="a01bc-110">Searches all available locations.</span></span><br/> | <span data-ttu-id="a01bc-111">0</span><span class="sxs-lookup"><span data-stu-id="a01bc-111">0</span></span>     |
| <span data-ttu-id="a01bc-112">**CAPICOM \_ Поиск в \_ глобальном \_ каталоге**</span><span class="sxs-lookup"><span data-stu-id="a01bc-112">**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</span></span> | <span data-ttu-id="a01bc-113">Выполняет поиск только в глобальном каталоге.</span><span class="sxs-lookup"><span data-stu-id="a01bc-113">Searches only the global catalog.</span></span><br/> | <span data-ttu-id="a01bc-114">1</span><span class="sxs-lookup"><span data-stu-id="a01bc-114">1</span></span>     |
| <span data-ttu-id="a01bc-115">**\_Поиск в \_ домене CAPICOM по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="a01bc-115">**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</span></span> | <span data-ttu-id="a01bc-116">Выполняет поиск только по домену по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a01bc-116">Searches only the default domain.</span></span><br/> | <span data-ttu-id="a01bc-117">2</span><span class="sxs-lookup"><span data-stu-id="a01bc-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="a01bc-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a01bc-118">Remarks</span></span>

<span data-ttu-id="a01bc-119">Этот тип перечисления используется следующим свойством:</span><span class="sxs-lookup"><span data-stu-id="a01bc-119">This enumeration type is used by the following property:</span></span>

-   [<span data-ttu-id="a01bc-120">**Settings. Активедиректорисеарчлокатион**</span><span class="sxs-lookup"><span data-stu-id="a01bc-120">**Settings.ActiveDirectorySearchLocation**</span></span>](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a><span data-ttu-id="a01bc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a01bc-121">Requirements</span></span>



| <span data-ttu-id="a01bc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a01bc-122">Requirement</span></span> | <span data-ttu-id="a01bc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a01bc-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a01bc-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a01bc-124">Redistributable</span></span><br/> | <span data-ttu-id="a01bc-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a01bc-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="a01bc-126">Header</span><span class="sxs-lookup"><span data-stu-id="a01bc-126">Header</span></span><br/>          | <dl> <span data-ttu-id="a01bc-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a01bc-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 
