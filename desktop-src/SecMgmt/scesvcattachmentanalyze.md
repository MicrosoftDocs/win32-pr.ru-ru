---
description: Функция Сцесвкаттачментанализе вызывается модулем настройки безопасности при анализе системы.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Функция обратного вызова Сцесвкаттачментанализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809305"
---
# <a name="scesvcattachmentanalyze-callback-function"></a><span data-ttu-id="2bdb7-103">Функция обратного вызова Сцесвкаттачментанализе</span><span class="sxs-lookup"><span data-stu-id="2bdb7-103">SceSvcAttachmentAnalyze callback function</span></span>

<span data-ttu-id="2bdb7-104">Функция **сцесвкаттачментанализе** вызывается модулем настройки безопасности при анализе системы.</span><span class="sxs-lookup"><span data-stu-id="2bdb7-104">The **SceSvcAttachmentAnalyze** function is called by the Security Configuration Engine when the system is analyzed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bdb7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bdb7-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2bdb7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bdb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bdb7-107">*псцекбинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2bdb7-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bdb7-108">Указатель на структуру [**\_ \_ сведений о обратном вызове сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) , которая содержит непрозрачный маркер базы данных и указатели на функции обратного вызова для запроса, установки и бесплатной информации.</span><span class="sxs-lookup"><span data-stu-id="2bdb7-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains an opaque database handle and callback function pointers to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bdb7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bdb7-109">Return value</span></span>

<span data-ttu-id="2bdb7-110">Если эта функция завершается успешно, возвращается СЦЕСТАТУС \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2bdb7-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="2bdb7-111">В противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2bdb7-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="2bdb7-112">Дополнительные сведения о кодах ошибок конфигурации безопасности см. в разделе [возвращаемые значения вложений](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2bdb7-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2bdb7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bdb7-113">Remarks</span></span>

<span data-ttu-id="2bdb7-114">Функция **сцесвкаттачментанализе** должна выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2bdb7-114">The **SceSvcAttachmentAnalyze** function must do the following:</span></span>

-   <span data-ttu-id="2bdb7-115">Непосредственно запрашивать сведения о конфигурации от службы.</span><span class="sxs-lookup"><span data-stu-id="2bdb7-115">Directly query configuration information from the service.</span></span>
-   <span data-ttu-id="2bdb7-116">Вызовите функцию обратного вызова, на которую указывает член **пфкуеринфо** структуры [**\_ \_ сведений о обратном вызове Сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (псцекбинфо->пфкуеринфо), чтобы получить сведения из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="2bdb7-116">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve information from the security database.</span></span>
-   <span data-ttu-id="2bdb7-117">Вычисление различий между данными на основе типа и синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="2bdb7-117">Compute the differences between the information based on type and syntax.</span></span>
-   <span data-ttu-id="2bdb7-118">Вызовите функцию обратного вызова, на  которую указывает член пфсетинфо [**структуры \_ обратного вызова \_ Сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (псцекбинфо->пфсетинфо), чтобы обновить базу данных безопасности с помощью полученных сведений о службе, которые отличаются.</span><span class="sxs-lookup"><span data-stu-id="2bdb7-118">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to update the security database with the retrieved service information that is different.</span></span>

<span data-ttu-id="2bdb7-119">Дополнительные сведения см. в разделе [Реализация сцесвкаттачментанализе](implementing-scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="2bdb7-119">For more information, see [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bdb7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2bdb7-120">Requirements</span></span>



| <span data-ttu-id="2bdb7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2bdb7-121">Requirement</span></span> | <span data-ttu-id="2bdb7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2bdb7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2bdb7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bdb7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2bdb7-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2bdb7-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2bdb7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bdb7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2bdb7-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2bdb7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bdb7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bdb7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdb7-128">Реализация Сцесвкаттачментанализе</span><span class="sxs-lookup"><span data-stu-id="2bdb7-128">Implementing SceSvcAttachmentAnalyze</span></span>](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[<span data-ttu-id="2bdb7-129">**\_сведения о обратном вызове сцесвк \_**</span><span class="sxs-lookup"><span data-stu-id="2bdb7-129">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="2bdb7-130">**сцесвкаттачментконфиг**</span><span class="sxs-lookup"><span data-stu-id="2bdb7-130">**SceSvcAttachmentConfig**</span></span>](scesvcattachmentconfig.md)
</dt> </dl>

 

 




