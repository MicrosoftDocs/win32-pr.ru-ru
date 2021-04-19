---
description: Предоставляет системе сведения о документе после завершения операции копирования в буфер обмена.
title: Функция Длпнотифипосткопитоклипбоард (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b4b1a375d68819fc36f82a530a7fe7a8abe881c0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495899"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a><span data-ttu-id="92569-103">Функция Длпнотифипосткопитоклипбоард</span><span class="sxs-lookup"><span data-stu-id="92569-103">DlpNotifyPostCopyToClipboard function</span></span>

<span data-ttu-id="92569-104">Предоставляет системе сведения о документе после завершения операции копирования в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="92569-104">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="92569-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92569-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="92569-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92569-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92569-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92569-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92569-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, из которого было скопировано содержимое.</span><span class="sxs-lookup"><span data-stu-id="92569-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="92569-109">*Опстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92569-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92569-110">Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии операции копирования в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="92569-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the copy to clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="92569-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92569-111">Return value</span></span>

<span data-ttu-id="92569-112">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="92569-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="92569-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="92569-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="92569-114">Требования</span><span class="sxs-lookup"><span data-stu-id="92569-114">Requirements</span></span>



| <span data-ttu-id="92569-115">Требование</span><span class="sxs-lookup"><span data-stu-id="92569-115">Requirement</span></span>          |    <span data-ttu-id="92569-116">Значение</span><span class="sxs-lookup"><span data-stu-id="92569-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92569-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92569-117">Minimum supported client</span></span><br/> | <span data-ttu-id="92569-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="92569-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="92569-119">DLL</span><span class="sxs-lookup"><span data-stu-id="92569-119">DLL</span></span><br/>                      | <span data-ttu-id="92569-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="92569-120">EndpointDlp.dll</span></span> |