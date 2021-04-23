---
description: Предоставляет системе сведения о документе после завершения операции вставки из буфера обмена.
title: Функция Длпнотифипостпастефромклипбоард (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 69a5afbc41350092ebd4d433d2f4d7259ece82cf
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495866"
---
# <a name="dlpnotifypostpastefromclipboard-function"></a><span data-ttu-id="853d9-103">Функция Длпнотифипостпастефромклипбоард</span><span class="sxs-lookup"><span data-stu-id="853d9-103">DlpNotifyPostPasteFromClipboard function</span></span>

<span data-ttu-id="853d9-104">Предоставляет системе сведения о документе после завершения операции вставки из буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="853d9-104">Provides the system with information about a document after a paste from clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="853d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="853d9-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="853d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="853d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="853d9-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="853d9-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="853d9-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, в который было скопировано содержимое.</span><span class="sxs-lookup"><span data-stu-id="853d9-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="853d9-109">*Опстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="853d9-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="853d9-110">Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии операции вставки из буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="853d9-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the paste from clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="853d9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="853d9-111">Return value</span></span>

<span data-ttu-id="853d9-112">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="853d9-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="853d9-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="853d9-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="853d9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="853d9-114">Requirements</span></span>



| <span data-ttu-id="853d9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="853d9-115">Requirement</span></span>          |    <span data-ttu-id="853d9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="853d9-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="853d9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="853d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="853d9-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="853d9-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="853d9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="853d9-119">DLL</span></span><br/>                      | <span data-ttu-id="853d9-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="853d9-120">EndpointDlp.dll</span></span> |