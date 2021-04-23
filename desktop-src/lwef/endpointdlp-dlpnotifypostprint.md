---
description: Предоставляет системе сведения о документе после завершения операции печати.
title: Функция Длпнотифипостпринт (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495865"
---
# <a name="dlpnotifypostprint-function"></a><span data-ttu-id="4c045-103">Функция Длпнотифипостпринт</span><span class="sxs-lookup"><span data-stu-id="4c045-103">DlpNotifyPostPrint function</span></span>

<span data-ttu-id="4c045-104">Предоставляет системе сведения о документе после завершения операции печати.</span><span class="sxs-lookup"><span data-stu-id="4c045-104">Provides the system with information about a document after a print operation has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c045-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c045-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a><span data-ttu-id="4c045-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c045-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c045-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c045-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, связанном с операцией печати.</span><span class="sxs-lookup"><span data-stu-id="4c045-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4c045-109">*Принтинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c045-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c045-110">Указатель на структуру [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) , содержащую сведения об операции печати.</span><span class="sxs-lookup"><span data-stu-id="4c045-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4c045-111">*Опстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c045-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c045-112">Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии операции печати.</span><span class="sxs-lookup"><span data-stu-id="4c045-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="4c045-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c045-113">Return value</span></span>

<span data-ttu-id="4c045-114">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="4c045-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c045-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="4c045-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="4c045-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4c045-116">Requirements</span></span>



| <span data-ttu-id="4c045-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4c045-117">Requirement</span></span>          |    <span data-ttu-id="4c045-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4c045-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c045-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c045-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c045-120">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="4c045-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="4c045-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4c045-121">DLL</span></span><br/>                      | <span data-ttu-id="4c045-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="4c045-122">EndpointDlp.dll</span></span> |