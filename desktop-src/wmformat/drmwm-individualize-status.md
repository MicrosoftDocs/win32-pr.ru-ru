---
title: Структура WM_INDIVIDUALIZE_STATUS (Вмдрмсдк. h)
description: '\_ \_ Структура состояния WM индивидуализируйте содержит сведения о ожидающем процессе индивидуализации.'
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- Формат WM_INDIVIDUALIZE_STATUS структуры Windows Media
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704449"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a><span data-ttu-id="584bc-104">Структура WM_INDIVIDUALIZE_STATUS (Вмдрмсдк. h)</span><span class="sxs-lookup"><span data-stu-id="584bc-104">WM_INDIVIDUALIZE_STATUS structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="584bc-105">Структура **\_ \_ состояния WM индивидуализируйте** содержит сведения о ожидающем процессе индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="584bc-105">The **WM\_INDIVIDUALIZE\_STATUS** structure holds information about a pending individualization process.</span></span>

## <a name="syntax"></a><span data-ttu-id="584bc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="584bc-106">Syntax</span></span>


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a><span data-ttu-id="584bc-107">Члены</span><span class="sxs-lookup"><span data-stu-id="584bc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="584bc-108">**ч**</span><span class="sxs-lookup"><span data-stu-id="584bc-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="584bc-109">Код возврата **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="584bc-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="584bc-110">**ениндистатус**</span><span class="sxs-lookup"><span data-stu-id="584bc-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="584bc-111">Значение из типа перечисления " [**\_ \_ состояние индивидуальной обработки DRM**](drmdrm-individualization-status.md) ", которое указывает текущее состояние процесса индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="584bc-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drmdrm-individualization-status.md) enumeration type that indicates the current status of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="584bc-112">**псзиндиреспурл**</span><span class="sxs-lookup"><span data-stu-id="584bc-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="584bc-113">Указатель на строку с завершающим нулем, содержащую URL-адрес ответа для индивидуальной строки.</span><span class="sxs-lookup"><span data-stu-id="584bc-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="584bc-114">**двхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="584bc-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="584bc-115">Количество полных путей HTTP к службе индивидуализации, которые были завершены.</span><span class="sxs-lookup"><span data-stu-id="584bc-115">The number of HTTP round trips to the individualization service that have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="584bc-116">**енхттпстатус**</span><span class="sxs-lookup"><span data-stu-id="584bc-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="584bc-117">Значение из типа [**перечисления \_ \_ состояния HTTP DRM**](drmdrm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="584bc-117">Value from the [**DRM\_HTTP\_STATUS**](drmdrm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="584bc-118">**двхттпреадпрогресс**</span><span class="sxs-lookup"><span data-stu-id="584bc-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="584bc-119">Число скачанных байтов.</span><span class="sxs-lookup"><span data-stu-id="584bc-119">The number of bytes downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="584bc-120">**двхттпреадтотал**</span><span class="sxs-lookup"><span data-stu-id="584bc-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="584bc-121">Общее число байтов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="584bc-121">The total number of bytes to be downloaded.</span></span> <span data-ttu-id="584bc-122">Вы можете использовать это значение и **двхттпреадпрогресс** , чтобы отобразить пользовательский интерфейс, указывающий, сколько завершенных Скачиваний и сколько осталось выполнить.</span><span class="sxs-lookup"><span data-stu-id="584bc-122">You can use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="584bc-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="584bc-123">Remarks</span></span>

<span data-ttu-id="584bc-124">Эта структура получается при вызове метода [**ивмдрминдивидуализатионстатус::-Status**](iwmdrmindividualizationstatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="584bc-124">This structure is received when you call the [**IWMDRMIndividualizationStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md) method.</span></span> <span data-ttu-id="584bc-125">Он содержит состояние ожидающего процесса индивидуализации во время вызова.</span><span class="sxs-lookup"><span data-stu-id="584bc-125">It contains the status of the pending individualization process at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="584bc-126">Требования</span><span class="sxs-lookup"><span data-stu-id="584bc-126">Requirements</span></span>



| <span data-ttu-id="584bc-127">Требование</span><span class="sxs-lookup"><span data-stu-id="584bc-127">Requirement</span></span> | <span data-ttu-id="584bc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="584bc-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="584bc-129">Header</span><span class="sxs-lookup"><span data-stu-id="584bc-129">Header</span></span><br/> | <dl> <span data-ttu-id="584bc-130"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="584bc-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="584bc-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="584bc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584bc-132">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="584bc-132">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





