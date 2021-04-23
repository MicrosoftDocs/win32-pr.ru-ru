---
description: Предоставляет системе сведения о документе до инициирования операции копирования в буфер обмена.
title: Функция Длпнотифипрекопитоклипбоард (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b8e835e58d19570b9459d91ad131bbc0f38f378a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495857"
---
# <a name="dlpnotifyprecopytoclipboard-function"></a><span data-ttu-id="ee021-103">Функция Длпнотифипрекопитоклипбоард</span><span class="sxs-lookup"><span data-stu-id="ee021-103">DlpNotifyPreCopyToClipboard function</span></span>

<span data-ttu-id="ee021-104">Предоставляет системе сведения о документе до инициирования операции копирования в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="ee021-104">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee021-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee021-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="ee021-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee021-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee021-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee021-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee021-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, из которого копируется содержимое.</span><span class="sxs-lookup"><span data-stu-id="ee021-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content is being copied.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="ee021-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee021-109">Return value</span></span>

<span data-ttu-id="ee021-110">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="ee021-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee021-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="ee021-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="ee021-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ee021-112">Requirements</span></span>



| <span data-ttu-id="ee021-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ee021-113">Requirement</span></span>          |    <span data-ttu-id="ee021-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ee021-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee021-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee021-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee021-116">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="ee021-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="ee021-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ee021-117">DLL</span></span><br/>                      | <span data-ttu-id="ee021-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="ee021-118">EndpointDlp.dll</span></span> |