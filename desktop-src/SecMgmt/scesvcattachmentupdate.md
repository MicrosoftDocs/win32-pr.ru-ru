---
description: Функция Сцесвкаттачментупдате вызывается оснасткой настройки безопасности для передачи изменений конфигурации в базу данных безопасности.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Функция обратного вызова Сцесвкаттачментупдате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809299"
---
# <a name="scesvcattachmentupdate-callback-function"></a><span data-ttu-id="dd663-103">Функция обратного вызова Сцесвкаттачментупдате</span><span class="sxs-lookup"><span data-stu-id="dd663-103">SceSvcAttachmentUpdate callback function</span></span>

<span data-ttu-id="dd663-104">Функция **сцесвкаттачментупдате** вызывается оснасткой настройки безопасности для передачи изменений конфигурации в базу данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd663-104">The **SceSvcAttachmentUpdate** function is called by the Security Configuration snap-ins to pass configuration changes to the security database.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd663-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd663-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a><span data-ttu-id="dd663-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd663-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd663-107">*псцекбинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd663-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd663-108">Указатель на структуру [**\_ \_ сведений о обратном вызове сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) , которая содержит маркер обратного вызова и указатели на функции в SCE.</span><span class="sxs-lookup"><span data-stu-id="dd663-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains the callback handle and function pointers to SCE.</span></span>

</dd> <dt>

<span data-ttu-id="dd663-109">*ServiceInfo* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd663-109">*ServiceInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd663-110">Обновлены сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dd663-110">Updated configuration information.</span></span> <span data-ttu-id="dd663-111">Структура данных, используемая для этой информации, — это [**сцесвк \_ \_ сведения о конфигурации**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span><span class="sxs-lookup"><span data-stu-id="dd663-111">The data structure used for this information is [**SCESVC\_CONFIGURATION\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd663-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd663-112">Return value</span></span>

<span data-ttu-id="dd663-113">Если эта функция завершается успешно, возвращается СЦЕСТАТУС \_ Success.</span><span class="sxs-lookup"><span data-stu-id="dd663-113">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="dd663-114">В противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="dd663-114">Otherwise it returns an error code.</span></span> <span data-ttu-id="dd663-115">Дополнительные сведения о кодах ошибок конфигурации безопасности см. в разделе [возвращаемые значения вложений](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="dd663-115">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dd663-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd663-116">Remarks</span></span>

<span data-ttu-id="dd663-117">Функция **сцесвкаттачментупдате** должна выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="dd663-117">The **SceSvcAttachmentUpdate** function must do the following:</span></span>

-   <span data-ttu-id="dd663-118">Вызовите функцию обратного вызова, на которую указывает член **пфкуеринфо** структуры [**\_ \_ сведений о обратном вызове Сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (псцекбинфо->пфкуеринфо), чтобы получить текущие сведения о базовой конфигурации из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd663-118">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the current base configuration information from the security database.</span></span>
-   <span data-ttu-id="dd663-119">Вызовите функцию обратного вызова, на которую указывает элемент **пфкуеринфо** в структуре [**\_ \_ сведений о обратном вызове Сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (псцекбинфо->пфкуеринфо), чтобы получить последний набор различий (сведения об анализе) из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd663-119">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the last set of differences (analysis information) from the security database.</span></span>
-   <span data-ttu-id="dd663-120">Используйте указанные сведения о службе (см. *serviceInfo*), чтобы вычислить новую базовую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="dd663-120">Use the supplied service information (see *ServiceInfo*) to compute the new base configuration.</span></span>
-   <span data-ttu-id="dd663-121">Используйте указанные сведения о службе (см. *serviceInfo*) и анализ, чтобы вычислить новые сведения о разнице.</span><span class="sxs-lookup"><span data-stu-id="dd663-121">Use the supplied service information (see *ServiceInfo*) and the analysis to compute the new difference information.</span></span>
-   <span data-ttu-id="dd663-122">Вызовите функцию обратного вызова, на которую указывает член **пфсетинфо** структуры [**\_ \_ сведений о обратном вызове Сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (псцекбинфо->пфсетинфо), чтобы задать новую базовую конфигурацию в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd663-122">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo)to set the new base configuration in the security database.</span></span>
-   <span data-ttu-id="dd663-123">Вызовите функцию обратного вызова, на которую указывает элемент **пфсетинфо** в структуре [**\_ \_ сведений о обратном вызове Сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (псцекбинфо->пфсетинфо), чтобы задать новые данные анализа в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd663-123">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to set the new analysis information in the security database.</span></span>

<span data-ttu-id="dd663-124">Дополнительные сведения см. в разделе [Реализация сцесвкаттачментупдате](implementing-scesvcattachmentupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="dd663-124">For more information, see [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="dd663-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dd663-125">Requirements</span></span>



| <span data-ttu-id="dd663-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dd663-126">Requirement</span></span> | <span data-ttu-id="dd663-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dd663-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd663-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd663-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dd663-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dd663-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="dd663-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd663-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dd663-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd663-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd663-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd663-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd663-133">**\_сведения о обратном вызове сцесвк \_**</span><span class="sxs-lookup"><span data-stu-id="dd663-133">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="dd663-134">**\_ \_ сведения о конфигурации сцесвк**</span><span class="sxs-lookup"><span data-stu-id="dd663-134">**SCESVC\_CONFIGURATION\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




