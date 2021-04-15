---
description: Определяет режим запроса для защищенного хранилища при каждом отображении пользовательского интерфейса.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: Структура PST_PROMPTINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668509"
---
# <a name="pst_promptinfo-structure"></a><span data-ttu-id="87b4a-103">\_Структура PST промптинфо</span><span class="sxs-lookup"><span data-stu-id="87b4a-103">PST\_PROMPTINFO structure</span></span>

<span data-ttu-id="87b4a-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="87b4a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="87b4a-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="87b4a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="87b4a-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="87b4a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="87b4a-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="87b4a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="87b4a-108">Определяет режим запроса для защищенного хранилища при каждом отображении пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="87b4a-108">Defines the prompting behavior of the Protected Store whenever it displays a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b4a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87b4a-109">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a><span data-ttu-id="87b4a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="87b4a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="87b4a-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="87b4a-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="87b4a-112">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="87b4a-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="87b4a-113">**двпромптфлагс**</span><span class="sxs-lookup"><span data-stu-id="87b4a-113">**dwPromptFlags**</span></span>
</dt> <dd>

<span data-ttu-id="87b4a-114">Этот флаг отклонен.</span><span class="sxs-lookup"><span data-stu-id="87b4a-114">This flag is ignored.</span></span>



| <span data-ttu-id="87b4a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="87b4a-115">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="87b4a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="87b4a-116">Meaning</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <span data-ttu-id="87b4a-117">PST-файл <dt>**\_ PF \_ всегда \_ Показывать**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="87b4a-117"><dt>**PST\_PF\_ALWAYS\_SHOW**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="87b4a-118">Запрашивает у поставщика диалоговое окно приглашения пользователю, даже если оно не требуется для этого доступа.</span><span class="sxs-lookup"><span data-stu-id="87b4a-118">Requests that the provider show the prompt dialog to the user even if it is not required for this access.</span></span> <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <span data-ttu-id="87b4a-119">PST-файл <dt>**\_ PF \_ никогда не \_ Показывать**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="87b4a-119"><dt>**PST\_PF\_NEVER\_SHOW**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="87b4a-120">Не показывать диалоговое окно запроса пользователю.</span><span class="sxs-lookup"><span data-stu-id="87b4a-120">Do not show the prompt dialog to the user.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="87b4a-121">**хвндапп**</span><span class="sxs-lookup"><span data-stu-id="87b4a-121">**hwndApp**</span></span>
</dt> <dd>

<span data-ttu-id="87b4a-122">Маркер родительского окна для пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="87b4a-122">The handle to the parent window for the user interface.</span></span> <span data-ttu-id="87b4a-123">Элемент **хвндапп** определяет, где отображается пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="87b4a-123">The **hwndApp** member determines where the user interface appears.</span></span> <span data-ttu-id="87b4a-124">Если передается **значение NULL** , Рабочий стол считается родительским окном.</span><span class="sxs-lookup"><span data-stu-id="87b4a-124">If **NULL** is passed, the desktop is considered to be the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="87b4a-125">**сзпромпт**</span><span class="sxs-lookup"><span data-stu-id="87b4a-125">**szPrompt**</span></span>
</dt> <dd>

<span data-ttu-id="87b4a-126">Строка запроса.</span><span class="sxs-lookup"><span data-stu-id="87b4a-126">The prompt string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87b4a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="87b4a-127">Requirements</span></span>



| <span data-ttu-id="87b4a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="87b4a-128">Requirement</span></span> | <span data-ttu-id="87b4a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="87b4a-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="87b4a-130">Header</span><span class="sxs-lookup"><span data-stu-id="87b4a-130">Header</span></span><br/> | <dl> <span data-ttu-id="87b4a-131"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="87b4a-131"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87b4a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87b4a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b4a-133">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="87b4a-133">**DeleteItem**</span></span>](ipstore-deleteitem.md)
</dt> <dt>

[<span data-ttu-id="87b4a-134">**опенитем**</span><span class="sxs-lookup"><span data-stu-id="87b4a-134">**OpenItem**</span></span>](ipstore-openitem.md)
</dt> <dt>

[<span data-ttu-id="87b4a-135">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="87b4a-135">**ReadItem**</span></span>](ipstore-readitem.md)
</dt> <dt>

[<span data-ttu-id="87b4a-136">**вритеитем**</span><span class="sxs-lookup"><span data-stu-id="87b4a-136">**WriteItem**</span></span>](ipstore-writeitem.md)
</dt> </dl>

 

 
