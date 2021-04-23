---
description: Предоставляет системе сведения о документе до инициации операции сохранения.
title: Функция Длпнотифипресавеасдокумент (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495821"
---
# <a name="dlpnotifypresaveasdocument-function"></a><span data-ttu-id="b812a-103">Функция Длпнотифипресавеасдокумент</span><span class="sxs-lookup"><span data-stu-id="b812a-103">DlpNotifyPreSaveAsDocument function</span></span>

<span data-ttu-id="b812a-104">Предоставляет системе сведения о документе до инициации операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="b812a-104">Provides the system with information about a document before a save as operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b812a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b812a-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a><span data-ttu-id="b812a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b812a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b812a-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b812a-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b812a-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, который необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="b812a-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b812a-109">*Назначение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b812a-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b812a-110">Объект **лпквстр** , содержащий путь назначения сохраняемого документа.</span><span class="sxs-lookup"><span data-stu-id="b812a-110">A **LPCWSTR** containing the destination path of the document to be saved.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b812a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b812a-111">Return value</span></span>

<span data-ttu-id="b812a-112">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="b812a-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b812a-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="b812a-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b812a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b812a-114">Requirements</span></span>



| <span data-ttu-id="b812a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b812a-115">Requirement</span></span>          |    <span data-ttu-id="b812a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b812a-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b812a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b812a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b812a-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="b812a-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b812a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="b812a-119">DLL</span></span><br/>                      | <span data-ttu-id="b812a-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b812a-120">EndpointDlp.dll</span></span> |