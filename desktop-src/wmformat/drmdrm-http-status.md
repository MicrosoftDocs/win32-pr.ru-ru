---
title: Перечисление DRM_HTTP_STATUS (Вмдрмсдк. h)
description: '\_ \_ Тип перечисления состояния HTTP DRM определяет диапазон состояний HTTP для запроса DRM.'
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- Формат Windows Media DRM_HTTP_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708494"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="7499e-105">Перечисление DRM_HTTP_STATUS (Вмдрмсдк. h)</span><span class="sxs-lookup"><span data-stu-id="7499e-105">DRM_HTTP_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="7499e-106">Тип **перечисления \_ \_ состояния HTTP DRM** определяет диапазон состояний HTTP для запроса DRM.</span><span class="sxs-lookup"><span data-stu-id="7499e-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of HTTP states for a DRM request.</span></span>

## <a name="syntax"></a><span data-ttu-id="7499e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7499e-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="7499e-108">Константы</span><span class="sxs-lookup"><span data-stu-id="7499e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7499e-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_НОТИНИТИАТЕД HTTP**</span><span class="sxs-lookup"><span data-stu-id="7499e-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="7499e-110">Операции HTTP не инициированы.</span><span class="sxs-lookup"><span data-stu-id="7499e-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="7499e-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_подключение HTTP**</span><span class="sxs-lookup"><span data-stu-id="7499e-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="7499e-112">Устанавливается соединение.</span><span class="sxs-lookup"><span data-stu-id="7499e-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="7499e-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP- \_ запрос**</span><span class="sxs-lookup"><span data-stu-id="7499e-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="7499e-114">Выполняется запрос данных.</span><span class="sxs-lookup"><span data-stu-id="7499e-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="7499e-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_Получение HTTP**</span><span class="sxs-lookup"><span data-stu-id="7499e-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="7499e-116">Данные получаются.</span><span class="sxs-lookup"><span data-stu-id="7499e-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="7499e-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="7499e-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="7499e-118">Операции HTTP завершены.</span><span class="sxs-lookup"><span data-stu-id="7499e-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7499e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7499e-119">Remarks</span></span>

<span data-ttu-id="7499e-120">Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](drmwm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="7499e-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7499e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7499e-121">Requirements</span></span>



| <span data-ttu-id="7499e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7499e-122">Requirement</span></span> | <span data-ttu-id="7499e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7499e-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7499e-124">Header</span><span class="sxs-lookup"><span data-stu-id="7499e-124">Header</span></span><br/> | <dl> <span data-ttu-id="7499e-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="7499e-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7499e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7499e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7499e-127">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="7499e-127">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





