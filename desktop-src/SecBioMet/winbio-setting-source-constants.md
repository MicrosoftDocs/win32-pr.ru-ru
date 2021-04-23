---
title: Константы WINBIO_SETTING_SOURCE (Винбио \_ types. h)
description: Определите, включена ли в данный момент биометрическая платформа Windows.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989343"
---
# <a name="winbio_setting_source-constants"></a><span data-ttu-id="c60ad-103">\_ \_ Константы источника параметра винбио</span><span class="sxs-lookup"><span data-stu-id="c60ad-103">WINBIO\_SETTING\_SOURCE Constants</span></span>

<span data-ttu-id="c60ad-104">Функция [**винбиожетенабледсеттинг**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) использует следующие константы для определения того, включена ли в данный момент биометрическая платформа Windows.</span><span class="sxs-lookup"><span data-stu-id="c60ad-104">The following constants are used by the [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) function to determine whether the Windows Biometric Framework is currently enabled.</span></span> <span data-ttu-id="c60ad-105">Константы указывают, где был создан параметр.</span><span class="sxs-lookup"><span data-stu-id="c60ad-105">The constants specify where the setting originated.</span></span>



| <span data-ttu-id="c60ad-106">Константа</span><span class="sxs-lookup"><span data-stu-id="c60ad-106">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="c60ad-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c60ad-107">Description</span></span>                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <span data-ttu-id="c60ad-108"><dt>**\_ \_ Недопустимый источник параметра винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ad-108"><dt>**WINBIO\_SETTING\_SOURCE\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="c60ad-109">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="c60ad-109">The setting is not valid.</span></span><br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <span data-ttu-id="c60ad-110"><dt>**\_Источник параметра \_ винбио \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ad-110"><dt>**WINBIO\_SETTING\_SOURCE\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="c60ad-111">Этот параметр создан из встроенной политики.</span><span class="sxs-lookup"><span data-stu-id="c60ad-111">The setting originated from built-in policy.</span></span><br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <span data-ttu-id="c60ad-112"><dt>**\_ \_ Политика источника параметра \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ad-112"><dt>**WINBIO\_SETTING\_SOURCE\_POLICY**</dt></span></span> </dl>    | <span data-ttu-id="c60ad-113">Этот параметр создан в реестре локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="c60ad-113">The setting originated in the local computer registry.</span></span><br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <span data-ttu-id="c60ad-114"><dt>**\_ \_ Локальная настройка источника винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ad-114"><dt>**WINBIO\_SETTING\_SOURCE\_LOCAL**</dt></span></span> </dl>       | <span data-ttu-id="c60ad-115">Этот параметр был создан групповая политика</span><span class="sxs-lookup"><span data-stu-id="c60ad-115">The setting was created by Group Policy</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="c60ad-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c60ad-116">Requirements</span></span>



| <span data-ttu-id="c60ad-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c60ad-117">Requirement</span></span> | <span data-ttu-id="c60ad-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c60ad-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c60ad-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c60ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c60ad-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c60ad-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c60ad-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c60ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c60ad-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c60ad-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c60ad-123">Header</span><span class="sxs-lookup"><span data-stu-id="c60ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c60ad-124"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c60ad-124"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c60ad-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c60ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60ad-126">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="c60ad-126">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





