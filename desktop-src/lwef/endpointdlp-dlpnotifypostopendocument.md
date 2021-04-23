---
description: Предоставляет системе сведения о документе после завершения операции открытия.
title: Функция Длпнотифипостопендокумент (ендпоинтдлп. h)
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
ms.openlocfilehash: 10121e69ddbdc41516e56ec07e87a2f6dd8148cd
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495893"
---
# <a name="dlpnotifypostopendocument-function"></a><span data-ttu-id="dd8d6-103">Функция Длпнотифипостопендокумент</span><span class="sxs-lookup"><span data-stu-id="dd8d6-103">DlpNotifyPostOpenDocument function</span></span>

<span data-ttu-id="dd8d6-104">Предоставляет системе сведения о документе после завершения операции открытия документа.</span><span class="sxs-lookup"><span data-stu-id="dd8d6-104">Provides the system with information about a document after an open document operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd8d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd8d6-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="dd8d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd8d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd8d6-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd8d6-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd8d6-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о открытом документе.</span><span class="sxs-lookup"><span data-stu-id="dd8d6-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="dd8d6-109">*Опстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd8d6-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd8d6-110">Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии операции открытия документа.</span><span class="sxs-lookup"><span data-stu-id="dd8d6-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="dd8d6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd8d6-111">Return value</span></span>

<span data-ttu-id="dd8d6-112">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="dd8d6-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd8d6-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="dd8d6-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="dd8d6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="dd8d6-114">Requirements</span></span>



| <span data-ttu-id="dd8d6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="dd8d6-115">Requirement</span></span>          |    <span data-ttu-id="dd8d6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8d6-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd8d6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd8d6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dd8d6-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="dd8d6-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="dd8d6-119">DLL</span><span class="sxs-lookup"><span data-stu-id="dd8d6-119">DLL</span></span><br/>                      | <span data-ttu-id="dd8d6-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="dd8d6-120">EndpointDlp.dll</span></span> |