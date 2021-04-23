---
description: Задает или получает расположение поиска Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Свойство Settings. Активедиректорисеарчлокатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668764"
---
# <a name="settingsactivedirectorysearchlocation-property"></a><span data-ttu-id="1ea5b-103">Свойство Settings. Активедиректорисеарчлокатион</span><span class="sxs-lookup"><span data-stu-id="1ea5b-103">Settings.ActiveDirectorySearchLocation property</span></span>

<span data-ttu-id="1ea5b-104">\[Свойство **активедиректорисеарчлокатион** доступно для использования в операционных системах, указанных в разделе требования.\]</span><span class="sxs-lookup"><span data-stu-id="1ea5b-104">\[The **ActiveDirectorySearchLocation** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="1ea5b-105">Свойство **активедиректорисеарчлокатион** задает или получает расположение поиска Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ea5b-105">The **ActiveDirectorySearchLocation** property sets or retrieves the Active Directory search location.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea5b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ea5b-106">Syntax</span></span>


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="1ea5b-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1ea5b-107">Property value</span></span>

<span data-ttu-id="1ea5b-108">Значение перечисления [**CAPICOM \_ Active \_ Directory \_ \_**](capicom-active-directory-search-location.md) , указывающее место поиска.</span><span class="sxs-lookup"><span data-stu-id="1ea5b-108">A value of the [**CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION**](capicom-active-directory-search-location.md) enumeration that specifies the search location.</span></span> <span data-ttu-id="1ea5b-109">По умолчанию используется значение CAPICOM \_ Search \_ ANY.</span><span class="sxs-lookup"><span data-stu-id="1ea5b-109">The default value is CAPICOM\_SEARCH\_ANY.</span></span> <span data-ttu-id="1ea5b-110">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="1ea5b-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="1ea5b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1ea5b-111">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="1ea5b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1ea5b-112">Meaning</span></span>                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <span data-ttu-id="1ea5b-113"><dt>**CAPICOM \_ Поиск \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea5b-113"><dt>**CAPICOM\_SEARCH\_ANY**</dt></span></span> </dl>                                   | <span data-ttu-id="1ea5b-114">Поиск по всем доступным расположениям.</span><span class="sxs-lookup"><span data-stu-id="1ea5b-114">Search all available locations.</span></span><br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <span data-ttu-id="1ea5b-115"><dt>**\_Поиск в \_ домене CAPICOM по умолчанию \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea5b-115"><dt>**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="1ea5b-116">Поиск только по домену по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ea5b-116">Search only the default domain.</span></span><br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <span data-ttu-id="1ea5b-117"><dt>**CAPICOM \_ Поиск в \_ глобальном \_ каталоге**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea5b-117"><dt>**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</dt></span></span> </dl> | <span data-ttu-id="1ea5b-118">Поиск только в глобальном каталоге.</span><span class="sxs-lookup"><span data-stu-id="1ea5b-118">Search only the global catalog.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ea5b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1ea5b-119">Requirements</span></span>



| <span data-ttu-id="1ea5b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1ea5b-120">Requirement</span></span> | <span data-ttu-id="1ea5b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1ea5b-121">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea5b-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1ea5b-122">Redistributable</span></span><br/> | <span data-ttu-id="1ea5b-123">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ea5b-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1ea5b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1ea5b-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="1ea5b-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ea5b-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ea5b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ea5b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea5b-127">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="1ea5b-127">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




