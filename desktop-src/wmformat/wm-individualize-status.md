---
title: Структура WM_INDIVIDUALIZE_STATUS (Дрмекстерналс. h)
description: '\_ \_ Структура состояния WM индивидуализируйте записывает состояние процесса индивидуализации.'
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- Формат WM_INDIVIDUALIZE_STATUS структуры Windows Media
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701065"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a><span data-ttu-id="a8dec-104">Структура WM_INDIVIDUALIZE_STATUS (Дрмекстерналс. h)</span><span class="sxs-lookup"><span data-stu-id="a8dec-104">WM_INDIVIDUALIZE_STATUS structure (Drmexternals.h)</span></span>

<span data-ttu-id="a8dec-105">Структура **\_ \_ состояния WM индивидуализируйте** записывает состояние процесса [*индивидуализации*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a8dec-105">The **WM\_INDIVIDUALIZE\_STATUS** structure records the status of the [*individualization*](wmformat-glossary.md) process.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8dec-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8dec-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="a8dec-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a8dec-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8dec-108">**ч**</span><span class="sxs-lookup"><span data-stu-id="a8dec-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="a8dec-109">Код возврата **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8dec-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="a8dec-110">**ениндистатус**</span><span class="sxs-lookup"><span data-stu-id="a8dec-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="a8dec-111">Значение из типа перечисления " [**\_ \_ состояние индивидуализации" DRM**](drm-individualization-status.md) .</span><span class="sxs-lookup"><span data-stu-id="a8dec-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drm-individualization-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="a8dec-112">**псзиндиреспурл**</span><span class="sxs-lookup"><span data-stu-id="a8dec-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="a8dec-113">Указатель на строку с завершающим нулем, содержащую URL-адрес ответа для индивидуальной строки.</span><span class="sxs-lookup"><span data-stu-id="a8dec-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="a8dec-114">**двхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="a8dec-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="a8dec-115">**Параметр DWORD** , указывающий количество выполненных циклов HTTP-обращений к службе индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="a8dec-115">**DWORD** that indicates the number of HTTP round trips to the individualization service that have been completed..</span></span>

</dd> <dt>

<span data-ttu-id="a8dec-116">**енхттпстатус**</span><span class="sxs-lookup"><span data-stu-id="a8dec-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="a8dec-117">Значение из типа [**перечисления \_ \_ состояния HTTP DRM**](drm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="a8dec-117">Value from the [**DRM\_HTTP\_STATUS**](drm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="a8dec-118">**двхттпреадпрогресс**</span><span class="sxs-lookup"><span data-stu-id="a8dec-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="a8dec-119">Значение **типа DWORD** , содержащее число байтов, скачанных до настоящего момента.</span><span class="sxs-lookup"><span data-stu-id="a8dec-119">**DWORD** containing the number of bytes downloaded until now..</span></span>

</dd> <dt>

<span data-ttu-id="a8dec-120">**двхттпреадтотал**</span><span class="sxs-lookup"><span data-stu-id="a8dec-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="a8dec-121">Значение **типа DWORD** , содержащее общее число байтов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="a8dec-121">**DWORD** containing the total number of bytes to be downloaded.</span></span> <span data-ttu-id="a8dec-122">Используйте это значение и **двхттпреадпрогресс** , чтобы отобразить пользовательский интерфейс, указывающий, сколько завершенных Скачиваний и сколько осталось выполнить.</span><span class="sxs-lookup"><span data-stu-id="a8dec-122">Use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8dec-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8dec-123">Remarks</span></span>

<span data-ttu-id="a8dec-124">Эта структура заполняется компонентами времени выполнения DRM и отправляется в приложения в параметре *pValue* метода [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , если событие равно ВМТ \_ индивидуализируйте.</span><span class="sxs-lookup"><span data-stu-id="a8dec-124">This structure is filled in by the DRM run-time components and is sent to applications in the *pValue* parameter of the applications [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method when the event equals WMT\_INDIVIDUALIZE.</span></span> <span data-ttu-id="a8dec-125">Приложение получает это событие несколько раз во время процесса загрузки.</span><span class="sxs-lookup"><span data-stu-id="a8dec-125">The application receives this event multiple times during the download process.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8dec-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a8dec-126">Requirements</span></span>



| <span data-ttu-id="a8dec-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a8dec-127">Requirement</span></span> | <span data-ttu-id="a8dec-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a8dec-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8dec-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8dec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a8dec-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a8dec-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a8dec-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8dec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a8dec-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a8dec-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a8dec-133">Версия</span><span class="sxs-lookup"><span data-stu-id="a8dec-133">Version</span></span><br/>                  | <span data-ttu-id="a8dec-134">Пакет SDK для Windows Media Format 7 или более поздние версии пакета SDK</span><span class="sxs-lookup"><span data-stu-id="a8dec-134">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="a8dec-135">Header</span><span class="sxs-lookup"><span data-stu-id="a8dec-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8dec-136"><dt>Дрмекстерналс. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8dec-136"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8dec-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8dec-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8dec-138">**\_состояние HTTP \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a8dec-138">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="a8dec-139">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="a8dec-139">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





