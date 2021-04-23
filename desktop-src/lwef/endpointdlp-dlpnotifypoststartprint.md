---
description: Предоставляет системе сведения о документе после запуска операции печати.
title: Функция Длпнотифипостстартпринт (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495861"
---
# <a name="dlpnotifypoststartprint-function"></a><span data-ttu-id="4d7f0-103">Функция Длпнотифипостстартпринт</span><span class="sxs-lookup"><span data-stu-id="4d7f0-103">DlpNotifyPostStartPrint function</span></span>

<span data-ttu-id="4d7f0-104">Предоставляет системе сведения о документе после начала операции печати.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-104">Provides the system with information about a document after a print operation has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d7f0-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a><span data-ttu-id="4d7f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d7f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7f0-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d7f0-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7f0-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, связанном с операцией печати.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4d7f0-109">*Принтинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d7f0-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7f0-110">Указатель на структуру [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) , содержащую сведения об операции печати.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="4d7f0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d7f0-111">Return value</span></span>

<span data-ttu-id="4d7f0-112">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d7f0-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="4d7f0-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="4d7f0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4d7f0-114">Requirements</span></span>



| <span data-ttu-id="4d7f0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4d7f0-115">Requirement</span></span>          |    <span data-ttu-id="4d7f0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4d7f0-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7f0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d7f0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d7f0-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="4d7f0-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="4d7f0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4d7f0-119">DLL</span></span><br/>                      | <span data-ttu-id="4d7f0-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="4d7f0-120">EndpointDlp.dll</span></span> |