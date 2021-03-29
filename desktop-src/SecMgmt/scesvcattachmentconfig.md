---
description: Функция Сцесвкаттачментконфиг вызывается модулем настройки безопасности при настройке системы.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Функция обратного вызова Сцесвкаттачментконфиг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809304"
---
# <a name="scesvcattachmentconfig-callback-function"></a><span data-ttu-id="9ba23-103">Функция обратного вызова Сцесвкаттачментконфиг</span><span class="sxs-lookup"><span data-stu-id="9ba23-103">SceSvcAttachmentConfig callback function</span></span>

<span data-ttu-id="9ba23-104">Функция **сцесвкаттачментконфиг** вызывается модулем настройки безопасности при настройке системы.</span><span class="sxs-lookup"><span data-stu-id="9ba23-104">The **SceSvcAttachmentConfig** function is called by the Security Configuration Engine when the system is configured.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ba23-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9ba23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ba23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba23-107">*псцекбинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9ba23-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba23-108">Указатель на структуру [**\_ \_ сведений о обратном вызове сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) , которая содержит обработчик базы данных и функции обратного вызова для запроса, установки и бесплатной информации.</span><span class="sxs-lookup"><span data-stu-id="9ba23-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure that contains the database handle and the callback functions to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba23-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ba23-109">Return value</span></span>

<span data-ttu-id="9ba23-110">Если эта функция завершается успешно, возвращается СЦЕСТАТУС \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9ba23-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="9ba23-111">В противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="9ba23-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="9ba23-112">Дополнительные сведения о кодах ошибок конфигурации безопасности см. в разделе [возвращаемые значения вложений](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9ba23-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba23-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ba23-113">Remarks</span></span>

<span data-ttu-id="9ba23-114">При реализации этой функции используйте функцию обратного вызова, на которую указывает член **пфкуеринфо** структуры [**\_ обратного вызова \_ Сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (псцекбинфо->пфкуеринфо), чтобы получить сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9ba23-114">When implementing this function, use the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve configuration information.</span></span> <span data-ttu-id="9ba23-115">Затем настройте службу, используя возвращенные сведения.</span><span class="sxs-lookup"><span data-stu-id="9ba23-115">Then configure the service using the returned information.</span></span>

<span data-ttu-id="9ba23-116">Эта функция должна выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9ba23-116">This function must do the following:</span></span>

-   <span data-ttu-id="9ba23-117">Запросите сведения о конфигурации из набора средств настройки безопасности, используя функцию обратного вызова, на которую указывает член **пфкуеринфо** структуры [**\_ обратного \_ вызова Сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (псцекбинфо->пфкуеринфо).</span><span class="sxs-lookup"><span data-stu-id="9ba23-117">Query configuration information from the Security Configuration tool set using the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo).</span></span>
-   <span data-ttu-id="9ba23-118">Настройте службу, используя сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9ba23-118">Configure the service using the configuration information.</span></span>

<span data-ttu-id="9ba23-119">Дополнительные сведения см. в разделе [Реализация сцесвкаттачментконфиг](implementing-scesvcattachmentconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba23-119">For more information, see [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba23-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9ba23-120">Requirements</span></span>



| <span data-ttu-id="9ba23-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9ba23-121">Requirement</span></span> | <span data-ttu-id="9ba23-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba23-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9ba23-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ba23-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba23-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ba23-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9ba23-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ba23-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba23-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ba23-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ba23-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ba23-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba23-128">**\_сведения о обратном вызове сцесвк \_**</span><span class="sxs-lookup"><span data-stu-id="9ba23-128">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="9ba23-129">**сцесвкаттачментанализе**</span><span class="sxs-lookup"><span data-stu-id="9ba23-129">**SceSvcAttachmentAnalyze**</span></span>](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




