---
title: Структура WMDRM_LICENSE_FILTER (Вмдрмсдк. h)
description: '\_ \_ Структура фильтра лицензий WMDRM определяет параметры фильтрации для использования при создании перечисления лицензий.'
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- Формат WMDRM_LICENSE_FILTER структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694862"
---
# <a name="wmdrm_license_filter-structure"></a><span data-ttu-id="6f398-105">\_ \_ Структура фильтра лицензий WMDRM</span><span class="sxs-lookup"><span data-stu-id="6f398-105">WMDRM\_LICENSE\_FILTER structure</span></span>

<span data-ttu-id="6f398-106">Структура **\_ \_ фильтра лицензий WMDRM** определяет параметры фильтрации для использования при создании перечисления лицензий.</span><span class="sxs-lookup"><span data-stu-id="6f398-106">The **WMDRM\_LICENSE\_FILTER** structure defines filtering parameters for use when creating a license enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f398-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f398-107">Syntax</span></span>


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a><span data-ttu-id="6f398-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6f398-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f398-109">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="6f398-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="6f398-110">Указывает минимальный номер версии для возвращенных лицензий.</span><span class="sxs-lookup"><span data-stu-id="6f398-110">Specifies a minimum version number for the returned licenses.</span></span>

</dd> <dt>

<span data-ttu-id="6f398-111">**бстркид**</span><span class="sxs-lookup"><span data-stu-id="6f398-111">**bstrKID**</span></span>
</dt> <dd>

<span data-ttu-id="6f398-112">Указывает идентификатор ключа для фильтрации лицензий.</span><span class="sxs-lookup"><span data-stu-id="6f398-112">Specifies a key ID to filter licenses for.</span></span> <span data-ttu-id="6f398-113">В перечисление будут включаться только лицензии с указанным ИДЕНТИФИКАТОРом ключа.</span><span class="sxs-lookup"><span data-stu-id="6f398-113">Only licenses with the specified key ID will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="6f398-114">**бстрригхтс**</span><span class="sxs-lookup"><span data-stu-id="6f398-114">**bstrRights**</span></span>
</dt> <dd>

<span data-ttu-id="6f398-115">Задает набор прав для фильтрации лицензий.</span><span class="sxs-lookup"><span data-stu-id="6f398-115">Specifies a set of rights to filter licenses for.</span></span> <span data-ttu-id="6f398-116">В перечисление будут включаться только лицензии, предоставляющие все указанные права.</span><span class="sxs-lookup"><span data-stu-id="6f398-116">Only licenses that provide all of the specified rights will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="6f398-117">**бстралловедсаурцеидс**</span><span class="sxs-lookup"><span data-stu-id="6f398-117">**bstrAllowedSourceIDs**</span></span>
</dt> <dd>

<span data-ttu-id="6f398-118">Указывает источники защищенного содержимого для включения в Поиск лицензий.</span><span class="sxs-lookup"><span data-stu-id="6f398-118">Specifies the sources of protected content to include in the license search.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f398-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f398-119">Remarks</span></span>

<span data-ttu-id="6f398-120">Эта структура используется методом [**ивмдрмлиценсеманажемент:: креателиценсинумератион**](iwmdrmlicensemanagement-createlicenseenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="6f398-120">This structure is used by the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f398-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6f398-121">Requirements</span></span>



| <span data-ttu-id="6f398-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6f398-122">Requirement</span></span> | <span data-ttu-id="6f398-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6f398-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f398-124">Header</span><span class="sxs-lookup"><span data-stu-id="6f398-124">Header</span></span><br/> | <dl> <span data-ttu-id="6f398-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f398-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f398-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f398-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f398-127">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="6f398-127">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





