---
title: Структура MPRESOURCE_INFO (Мпклиент. h)
description: Структура сведений о ресурсах.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO структуры устаревшие функции среды Windows
- Функции PMPRESOURCE_INFO указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988923"
---
# <a name="mpresource_info-structure"></a><span data-ttu-id="7ce47-105">\_Структура сведений о мпресаурце</span><span class="sxs-lookup"><span data-stu-id="7ce47-105">MPRESOURCE\_INFO structure</span></span>

<span data-ttu-id="7ce47-106">Структура сведений о ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7ce47-106">Resource information structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce47-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ce47-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a><span data-ttu-id="7ce47-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7ce47-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ce47-109">**Схема**</span><span class="sxs-lookup"><span data-stu-id="7ce47-109">**Scheme**</span></span>
</dt> <dd>

<span data-ttu-id="7ce47-110">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ce47-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7ce47-111">Идентификатор схемы ресурсов, например "File" или "Dir".</span><span class="sxs-lookup"><span data-stu-id="7ce47-111">Resource scheme identifier such as "file" or "dir".</span></span>

</dd> <dt>

<span data-ttu-id="7ce47-112">**Путь**</span><span class="sxs-lookup"><span data-stu-id="7ce47-112">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="7ce47-113">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ce47-113">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7ce47-114">Абсолютный путь к ресурсу на основе **схемы**.</span><span class="sxs-lookup"><span data-stu-id="7ce47-114">Absolute path of resource, based on **Scheme**.</span></span>

</dd> <dt>

<span data-ttu-id="7ce47-115">**Класс**</span><span class="sxs-lookup"><span data-stu-id="7ce47-115">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="7ce47-116">Тип: **\_ класс мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="7ce47-116">Type: **MPRESOURCE\_CLASS**</span></span>

</dd> <dd>

<span data-ttu-id="7ce47-117">Это поле задается, когда ресурс идентифицируется как часть угрозы.</span><span class="sxs-lookup"><span data-stu-id="7ce47-117">This field is set when the resource is identified as part of the threat.</span></span> <span data-ttu-id="7ce47-118">Он указывает класс ресурсов, в основном и нескрытое.</span><span class="sxs-lookup"><span data-stu-id="7ce47-118">It specifies the resource class, mainly concrete vs. latent.</span></span> <span data-ttu-id="7ce47-119">Это может быть сочетание следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="7ce47-119">It can be a combination of these possible values:</span></span>



| <span data-ttu-id="7ce47-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce47-120">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="7ce47-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce47-121">Meaning</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <span data-ttu-id="7ce47-122"><dt>**Пакет управления \_ \_Неизвестный \_ символ 0X0000 класса ресурсов**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7ce47-122"><dt>**MP\_RESOURCE\_CLASS\_UNKNOWN**</dt> <dt>0x0000</dt></span></span> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <span data-ttu-id="7ce47-123"><dt>**Пакет управления \_ \_Класс ресурсов \_ бетон**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="7ce47-123"><dt>**MP\_RESOURCE\_CLASS\_CONCRETE**</dt> <dt>0x0001</dt></span></span> </dl>           | <span data-ttu-id="7ce47-124">Взаимоисключающий с **\_ \_ классом \_ ресурсов MP "скрытые**".</span><span class="sxs-lookup"><span data-stu-id="7ce47-124">Mutually exclusive with **MP\_RESOURCE\_CLASS\_LATENT**.</span></span><br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <span data-ttu-id="7ce47-125"><dt>**Пакет управления \_ Класс ресурсов — \_ \_ скрытые**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="7ce47-125"><dt>**MP\_RESOURCE\_CLASS\_LATENT**</dt> <dt>0x0002</dt></span></span> </dl>                 | <span data-ttu-id="7ce47-126">Взаимоисключающий с **\_ \_ \_ конкретным классом ресурсов MP**.</span><span class="sxs-lookup"><span data-stu-id="7ce47-126">Mutually exclusive with **MP\_RESOURCE\_CLASS\_CONCRETE**.</span></span><br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <span data-ttu-id="7ce47-127"><dt>**Пакет управления \_ \_ \_ Пример \_ файла 0x0004 класса ресурсов**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7ce47-127"><dt>**MP\_RESOURCE\_CLASS\_SAMPLE\_FILE**</dt> <dt>0x0004</dt></span></span> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <span data-ttu-id="7ce47-128"><dt>**Пакет управления \_ \_Класс ресурсов \_ Shared**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="7ce47-128"><dt>**MP\_RESOURCE\_CLASS\_SHARED**</dt> <dt>0x0100</dt></span></span> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ce47-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7ce47-129">Requirements</span></span>



| <span data-ttu-id="7ce47-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7ce47-130">Requirement</span></span> | <span data-ttu-id="7ce47-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce47-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce47-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ce47-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce47-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7ce47-133">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7ce47-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ce47-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce47-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7ce47-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ce47-136">Header</span><span class="sxs-lookup"><span data-stu-id="7ce47-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ce47-137"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ce47-137"><dt>MpClient.h</dt></span></span> </dl> |



 

 





