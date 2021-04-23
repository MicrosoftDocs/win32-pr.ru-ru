---
description: Предоставляет системе сведения о документе до начала операции вставки из буфера обмена.
title: Функция Длпнотифипрепастефромклипбоард (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cfec6e7abbf2b94ce8bf78e0b1a10082ec54419d
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495814"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a><span data-ttu-id="19656-103">Функция Длпнотифипрепастефромклипбоард</span><span class="sxs-lookup"><span data-stu-id="19656-103">DlpNotifyPrePasteFromClipboard function</span></span>

<span data-ttu-id="19656-104">Предоставляет системе сведения о документе до начала операции вставки из буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="19656-104">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="19656-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19656-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="19656-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19656-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19656-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19656-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19656-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, в который вставляется контент.</span><span class="sxs-lookup"><span data-stu-id="19656-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content is being pasted.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="19656-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19656-109">Return value</span></span>

<span data-ttu-id="19656-110">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="19656-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="19656-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="19656-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="19656-112">Требования</span><span class="sxs-lookup"><span data-stu-id="19656-112">Requirements</span></span>



| <span data-ttu-id="19656-113">Требование</span><span class="sxs-lookup"><span data-stu-id="19656-113">Requirement</span></span>          |    <span data-ttu-id="19656-114">Значение</span><span class="sxs-lookup"><span data-stu-id="19656-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19656-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19656-115">Minimum supported client</span></span><br/> | <span data-ttu-id="19656-116">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="19656-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="19656-117">DLL</span><span class="sxs-lookup"><span data-stu-id="19656-117">DLL</span></span><br/>                      | <span data-ttu-id="19656-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="19656-118">EndpointDlp.dll</span></span> |