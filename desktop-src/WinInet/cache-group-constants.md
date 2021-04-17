---
title: Константы группы кэша (WinInet. h)
description: В следующем списке содержатся константы, используемые функциями группы кэша.
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710523"
---
# <a name="cache-group-constants"></a><span data-ttu-id="102a7-103">Константы группы кэша</span><span class="sxs-lookup"><span data-stu-id="102a7-103">Cache Group Constants</span></span>

<span data-ttu-id="102a7-104">В следующем списке содержатся константы, используемые функциями группы кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-104">The following list contains the constants used by the cache group functions.</span></span>

<dl> <dt>

<span data-ttu-id="102a7-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**\_атрибут качеграуп \_ Basic**</span><span class="sxs-lookup"><span data-stu-id="102a7-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP\_ATTRIBUTE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="102a7-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="102a7-107">Извлекает атрибуты флага, типа и дисковой квоты группы кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-107">Retrieves the flags, type, and disk quota attributes of the cache group.</span></span> <span data-ttu-id="102a7-108">Это используется функцией [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="102a7-108">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_флаг атрибута \_ качеграуп**</span><span class="sxs-lookup"><span data-stu-id="102a7-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP\_ATTRIBUTE\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="102a7-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="102a7-111">Задает или получает флаги, связанные с группой кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-111">Sets or retrieves the flags associated with the cache group.</span></span> <span data-ttu-id="102a7-112">Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="102a7-112">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**КАЧЕГРАУП \_ атрибут \_ Get \_**</span><span class="sxs-lookup"><span data-stu-id="102a7-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP\_ATTRIBUTE\_GET\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-114">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="102a7-114">0xffffffff</span></span>
</dt> <dt>



<span data-ttu-id="102a7-115">Извлекает все атрибуты группы кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-115">Retrieves all the attributes of the cache group.</span></span> <span data-ttu-id="102a7-116">Это используется функцией [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="102a7-116">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**КАЧЕГРАУП, \_ атрибут \_ GROUPNAME**</span><span class="sxs-lookup"><span data-stu-id="102a7-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP\_ATTRIBUTE\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-118">0x000000010</span><span class="sxs-lookup"><span data-stu-id="102a7-118">0x000000010</span></span>
</dt> <dt>



<span data-ttu-id="102a7-119">Задает или получает имя группы кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-119">Sets or retrieves the group name of the cache group.</span></span> <span data-ttu-id="102a7-120">Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="102a7-120">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_ \_ Квота атрибута качеграуп**</span><span class="sxs-lookup"><span data-stu-id="102a7-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP\_ATTRIBUTE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="102a7-122">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="102a7-123">Задает или получает дисковую квоту, связанную с группой кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-123">Sets or retrieves the disk quota associated with the cache group.</span></span> <span data-ttu-id="102a7-124">Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="102a7-124">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_хранилище АТРИБУТОВ \_ качеграуп**</span><span class="sxs-lookup"><span data-stu-id="102a7-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP\_ATTRIBUTE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="102a7-126">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="102a7-127">Задает или получает хранилище владельца группы, связанное с группой кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-127">Sets or retrieves the group owner storage associated with the cache group.</span></span> <span data-ttu-id="102a7-128">Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="102a7-128">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_тип атрибута \_ качеграуп**</span><span class="sxs-lookup"><span data-stu-id="102a7-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP\_ATTRIBUTE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="102a7-130">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="102a7-131">Задает или получает тип группы кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-131">Sets or retrieves the cache group type.</span></span> <span data-ttu-id="102a7-132">Он используется функциями [**жетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) и [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="102a7-132">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**КАЧЕГРАУП \_ \_ ФЛУШУРЛ, \_ Удаление флага**</span><span class="sxs-lookup"><span data-stu-id="102a7-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP\_FLAG\_FLUSHURL\_ONDELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="102a7-134">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="102a7-135">Указывает, что все записи кэша, связанные с группой кэша, должны быть удалены, если только запись не принадлежит другой группе кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-135">Indicates that all the cache entries associated with the cache group should be deleted, unless the entry belongs to another cache group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**\_гидонли флаг \_ качеграуп**</span><span class="sxs-lookup"><span data-stu-id="102a7-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP\_FLAG\_GIDONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="102a7-137">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="102a7-138">Указывает, что функция должна создавать только уникальный идентификатор GROUPID для группы кэша и не создавать фактическую группу.</span><span class="sxs-lookup"><span data-stu-id="102a7-138">Indicates that the function should only create a unique GROUPID for the cache group and not create the actual group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**Флаг КАЧЕГРАУП не был \_ \_ очищен**</span><span class="sxs-lookup"><span data-stu-id="102a7-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP\_FLAG\_NONPURGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-140">0x00000001</span><span class="sxs-lookup"><span data-stu-id="102a7-140">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="102a7-141">Указывает, что группа кэша не может быть очищена.</span><span class="sxs-lookup"><span data-stu-id="102a7-141">Indicates that the cache group cannot be purged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**\_Маска качеграуп ReadWrite \_**</span><span class="sxs-lookup"><span data-stu-id="102a7-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP\_READWRITE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-143">0x0000003c</span><span class="sxs-lookup"><span data-stu-id="102a7-143">0x0000003c</span></span>
</dt> <dt>



<span data-ttu-id="102a7-144">Задает тип, квоту диска, имя группы и атрибуты хранилища владельца группы кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-144">Sets the type, disk quota, group name, and owner storage attributes of the cache group.</span></span> <span data-ttu-id="102a7-145">Это используется функцией [**сетурлкачеграупаттрибуте**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="102a7-145">This is used by the [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**КАЧЕГРАУП \_ Поиск \_ всех**</span><span class="sxs-lookup"><span data-stu-id="102a7-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP\_SEARCH\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="102a7-147">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="102a7-148">Указывает, что необходимо перечислить все группы кэша в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="102a7-148">Indicates that all of the cache groups in the user's system should be enumerated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**КАЧЕГРАУП \_ поиска \_ бюрл**</span><span class="sxs-lookup"><span data-stu-id="102a7-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP\_SEARCH\_BYURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="102a7-150">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="102a7-151">В настоящий момент не реализовано.</span><span class="sxs-lookup"><span data-stu-id="102a7-151">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**\_Недопустимый тип качеграуп \_**</span><span class="sxs-lookup"><span data-stu-id="102a7-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP\_TYPE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="102a7-153">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="102a7-154">Указывает, что тип группы кэша недопустим.</span><span class="sxs-lookup"><span data-stu-id="102a7-154">Indicates that the cache group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_ \_ Размер хранилища владельца \_ группы**</span><span class="sxs-lookup"><span data-stu-id="102a7-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**GROUP\_OWNER\_STORAGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-156">0x00000004</span><span class="sxs-lookup"><span data-stu-id="102a7-156">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="102a7-157">Длина массива хранения владельца группы.</span><span class="sxs-lookup"><span data-stu-id="102a7-157">Length of the group owner storage array.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="102a7-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**ИМЯ_ГРУППЫ \_ Максимальная \_ Длина**</span><span class="sxs-lookup"><span data-stu-id="102a7-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME\_MAX\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102a7-159">0x00000078</span><span class="sxs-lookup"><span data-stu-id="102a7-159">0x00000078</span></span>
</dt> <dt>



<span data-ttu-id="102a7-160">Максимальное число символов, разрешенное для имени группы кэша.</span><span class="sxs-lookup"><span data-stu-id="102a7-160">Maximum number of characters allowed for a cache group name.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="102a7-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="102a7-161">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="102a7-162">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="102a7-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="102a7-163">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="102a7-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="102a7-164">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="102a7-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="102a7-165">Требования</span><span class="sxs-lookup"><span data-stu-id="102a7-165">Requirements</span></span>



| <span data-ttu-id="102a7-166">Требование</span><span class="sxs-lookup"><span data-stu-id="102a7-166">Requirement</span></span> | <span data-ttu-id="102a7-167">Значение</span><span class="sxs-lookup"><span data-stu-id="102a7-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="102a7-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="102a7-168">Minimum supported client</span></span><br/> | <span data-ttu-id="102a7-169">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="102a7-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="102a7-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="102a7-170">Minimum supported server</span></span><br/> | <span data-ttu-id="102a7-171">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="102a7-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="102a7-172">Заголовок</span><span class="sxs-lookup"><span data-stu-id="102a7-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="102a7-173"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="102a7-173"><dt>Wininet.h</dt></span></span> </dl> |



 

