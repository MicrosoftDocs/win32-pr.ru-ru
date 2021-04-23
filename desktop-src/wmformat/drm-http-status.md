---
title: Перечисление DRM_HTTP_STATUS (Дрмекстерналс. h)
description: '\_ \_ Тип перечисления состояния HTTP DRM определяет диапазон состояний для запроса DRM.'
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- Формат Windows Media DRM_HTTP_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672771"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a><span data-ttu-id="1f20e-105">Перечисление DRM_HTTP_STATUS (Дрмекстерналс. h)</span><span class="sxs-lookup"><span data-stu-id="1f20e-105">DRM_HTTP_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="1f20e-106">Тип **перечисления \_ \_ состояния HTTP DRM** определяет диапазон состояний для запроса [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="1f20e-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of states for a [*DRM*](wmformat-glossary.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f20e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f20e-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="1f20e-108">Константы</span><span class="sxs-lookup"><span data-stu-id="1f20e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1f20e-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_НОТИНИТИАТЕД HTTP**</span><span class="sxs-lookup"><span data-stu-id="1f20e-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="1f20e-110">Операции HTTP не инициированы.</span><span class="sxs-lookup"><span data-stu-id="1f20e-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="1f20e-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_подключение HTTP**</span><span class="sxs-lookup"><span data-stu-id="1f20e-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="1f20e-112">Устанавливается соединение.</span><span class="sxs-lookup"><span data-stu-id="1f20e-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="1f20e-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP- \_ запрос**</span><span class="sxs-lookup"><span data-stu-id="1f20e-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="1f20e-114">Выполняется запрос данных.</span><span class="sxs-lookup"><span data-stu-id="1f20e-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="1f20e-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_Получение HTTP**</span><span class="sxs-lookup"><span data-stu-id="1f20e-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="1f20e-116">Данные получаются.</span><span class="sxs-lookup"><span data-stu-id="1f20e-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="1f20e-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="1f20e-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="1f20e-118">Операции HTTP завершены.</span><span class="sxs-lookup"><span data-stu-id="1f20e-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f20e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f20e-119">Remarks</span></span>

<span data-ttu-id="1f20e-120">Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="1f20e-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f20e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1f20e-121">Requirements</span></span>



| <span data-ttu-id="1f20e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1f20e-122">Requirement</span></span> | <span data-ttu-id="1f20e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1f20e-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f20e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f20e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1f20e-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f20e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1f20e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f20e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1f20e-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f20e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1f20e-128">Версия</span><span class="sxs-lookup"><span data-stu-id="1f20e-128">Version</span></span><br/>                  | <span data-ttu-id="1f20e-129">Пакет SDK для Windows Media Format 7 или более поздние версии пакета SDK</span><span class="sxs-lookup"><span data-stu-id="1f20e-129">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="1f20e-130">Header</span><span class="sxs-lookup"><span data-stu-id="1f20e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f20e-131"><dt>Дрмекстерналс. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f20e-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f20e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f20e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f20e-133">**\_состояние ИНДИВИДУАЛИЗАЦИИ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="1f20e-133">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drm-individualization-status.md)
</dt> <dt>

[<span data-ttu-id="1f20e-134">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="1f20e-134">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





