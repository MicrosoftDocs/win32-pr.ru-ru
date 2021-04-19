---
description: Предоставляет системе сведения о документе после завершения операции Сохранить как.
title: Функция Длпнотифипостсавеасдокумент (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495862"
---
# <a name="dlpnotifypostsaveasdocument-function"></a><span data-ttu-id="2b401-103">Функция Длпнотифипостсавеасдокумент</span><span class="sxs-lookup"><span data-stu-id="2b401-103">DlpNotifyPostSaveAsDocument function</span></span>

<span data-ttu-id="2b401-104">Предоставляет системе сведения о документе после завершения операции Сохранить как.</span><span class="sxs-lookup"><span data-stu-id="2b401-104">Provides the system with information about a document after the save as operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b401-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b401-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="2b401-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b401-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b401-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b401-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b401-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о сохраненном документе.</span><span class="sxs-lookup"><span data-stu-id="2b401-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="2b401-109">*Назначение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b401-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b401-110">Объект **лпквстр** , содержащий целевой путь к сохраненному документу.</span><span class="sxs-lookup"><span data-stu-id="2b401-110">A **LPCWSTR** containing the destination path the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="2b401-111">*Опстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b401-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b401-112">Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии операции "Сохранить как".</span><span class="sxs-lookup"><span data-stu-id="2b401-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the save as operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="2b401-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b401-113">Return value</span></span>

<span data-ttu-id="2b401-114">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="2b401-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b401-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="2b401-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="2b401-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2b401-116">Requirements</span></span>



| <span data-ttu-id="2b401-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2b401-117">Requirement</span></span>          |    <span data-ttu-id="2b401-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2b401-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b401-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b401-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b401-120">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="2b401-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="2b401-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2b401-121">DLL</span></span><br/>                      | <span data-ttu-id="2b401-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="2b401-122">EndpointDlp.dll</span></span> |