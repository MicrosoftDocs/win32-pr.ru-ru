---
description: Определяет состояние диспетчера выходной защиты (ОПМ).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Перечисление MF_MEDIA_ENGINE_OPM_STATUS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674533"
---
# <a name="mf_media_engine_opm_status-enumeration"></a><span data-ttu-id="b86d5-103">\_ \_ \_ Перечисление состояния ОПМ для подсистемы передачи мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="b86d5-103">MF\_MEDIA\_ENGINE\_OPM\_STATUS enumeration</span></span>

<span data-ttu-id="b86d5-104">Определяет состояние [диспетчера выходной защиты](output-protection-manager.md) (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="b86d5-104">Defines the status of the [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

## <a name="syntax"></a><span data-ttu-id="b86d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b86d5-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a><span data-ttu-id="b86d5-106">Константы</span><span class="sxs-lookup"><span data-stu-id="b86d5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b86d5-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**\_ \_ ОПМ подсистема мультимедиа MF \_ \_ не \_ запрошена**</span><span class="sxs-lookup"><span data-stu-id="b86d5-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF\_MEDIA\_ENGINE\_OPM\_NOT\_REQUESTED**</span></span>
</dt> <dd>

<span data-ttu-id="b86d5-108">Состояние по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b86d5-108">Default status.</span></span> <span data-ttu-id="b86d5-109">Используется для возврата правильного состояния, когда содержимое не защищено.</span><span class="sxs-lookup"><span data-stu-id="b86d5-109">Used to return the correct status when the content is unprotected.</span></span>

</dd> <dt>

<span data-ttu-id="b86d5-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**\_ \_ опмная система мультимедиа MF \_ \_ установлена**</span><span class="sxs-lookup"><span data-stu-id="b86d5-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF\_MEDIA\_ENGINE\_OPM\_ESTABLISHED**</span></span>
</dt> <dd>

<span data-ttu-id="b86d5-111">ОПМ успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="b86d5-111">OPM successfully established.</span></span>

</dd> <dt>

<span data-ttu-id="b86d5-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_ \_ \_ \_ сбой \_ виртуальной машины ОПМ в MF Media Engine**</span><span class="sxs-lookup"><span data-stu-id="b86d5-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="b86d5-113">Сбой ОПМ из-за запуска в виртуальной машине (ВМ).</span><span class="sxs-lookup"><span data-stu-id="b86d5-113">OPM failed because running in a virtual machined (VM).</span></span>

</dd> <dt>

<span data-ttu-id="b86d5-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**\_BDA Media \_ Engine \_ ОПМ \_ Failed \_**</span><span class="sxs-lookup"><span data-stu-id="b86d5-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_BDA**</span></span>
</dt> <dd>

<span data-ttu-id="b86d5-115">Сбой ОПМ из-за отсутствия графического драйвера, и система использует базовый видеоадаптер (BDA).</span><span class="sxs-lookup"><span data-stu-id="b86d5-115">OPM failed because there is no graphics driver and the system is using Basic Display Adapter (BDA).</span></span>

</dd> <dt>

<span data-ttu-id="b86d5-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**\_ \_ \_ \_ \_ неподписанный драйвер ОПМ для подсистемы передачи мультимедиа MF \_**</span><span class="sxs-lookup"><span data-stu-id="b86d5-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_UNSIGNED\_DRIVER**</span></span>
</dt> <dd>

<span data-ttu-id="b86d5-117">Сбой ОПМ из-за того, что графический драйвер не подписан PE, вернемся к ИСКРИВЛЕНию.</span><span class="sxs-lookup"><span data-stu-id="b86d5-117">OPM failed because the graphics driver is not PE signed, falling back to WARP.</span></span>

</dd> <dt>

<span data-ttu-id="b86d5-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**\_ \_ сбой ОПМ для механизма передачи мультимедиа \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="b86d5-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="b86d5-119">Не удалось выполнить ОПМ по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="b86d5-119">OPM failed for other reasons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b86d5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b86d5-120">Requirements</span></span>



| <span data-ttu-id="b86d5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b86d5-121">Requirement</span></span> | <span data-ttu-id="b86d5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b86d5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b86d5-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b86d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b86d5-124">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b86d5-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b86d5-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b86d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b86d5-126">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b86d5-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b86d5-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b86d5-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b86d5-128"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b86d5-128"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b86d5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b86d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86d5-130">Перечисления Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b86d5-130">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




