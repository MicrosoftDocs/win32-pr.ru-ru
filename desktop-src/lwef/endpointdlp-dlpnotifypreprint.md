---
description: Предоставляет системе сведения о документе до начала операции печати.
title: Функция Длпнотифипрепринт (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: eef5e3a19a6b93a49ba8b600be77385a99d3153a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495818"
---
# <a name="dlpnotifypreprint-function"></a><span data-ttu-id="2cb4d-103">Функция Длпнотифипрепринт</span><span class="sxs-lookup"><span data-stu-id="2cb4d-103">DlpNotifyPrePrint function</span></span>

<span data-ttu-id="2cb4d-104">Предоставляет системе сведения о документе до начала операции печати.</span><span class="sxs-lookup"><span data-stu-id="2cb4d-104">Provides the system with information about a document before a print operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cb4d-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a><span data-ttu-id="2cb4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cb4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cb4d-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2cb4d-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb4d-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о печатаемом документе.</span><span class="sxs-lookup"><span data-stu-id="2cb4d-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be printed.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="2cb4d-109">*Принтинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2cb4d-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb4d-110">Указатель на структуру [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) , содержащую сведения о операции печати.</span><span class="sxs-lookup"><span data-stu-id="2cb4d-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="2cb4d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cb4d-111">Return value</span></span>

<span data-ttu-id="2cb4d-112">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="2cb4d-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cb4d-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="2cb4d-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="2cb4d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2cb4d-114">Requirements</span></span>



| <span data-ttu-id="2cb4d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2cb4d-115">Requirement</span></span>          |    <span data-ttu-id="2cb4d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2cb4d-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb4d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cb4d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb4d-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="2cb4d-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="2cb4d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="2cb4d-119">DLL</span></span><br/>                      | <span data-ttu-id="2cb4d-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="2cb4d-120">EndpointDlp.dll</span></span> |