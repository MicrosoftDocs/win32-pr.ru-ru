---
description: Предоставляет системе сведения о документе до инициирования операции закрытия файла документа.
title: Функция Длпнотификлоседокументфиле (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2438829cde84e9029a86d74e4ed704e1e8d33511
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495906"
---
# <a name="dlpnotifyclosedocumentfile-function"></a><span data-ttu-id="8d0a4-103">Функция Длпнотификлоседокументфиле</span><span class="sxs-lookup"><span data-stu-id="8d0a4-103">DlpNotifyCloseDocumentFile function</span></span>

<span data-ttu-id="8d0a4-104">Предоставляет системе сведения о документе до инициирования операции закрытия файла документа.</span><span class="sxs-lookup"><span data-stu-id="8d0a4-104">Provides the system with information about a document before the document file close operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d0a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d0a4-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="8d0a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d0a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d0a4-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d0a4-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0a4-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о открываемом документе.</span><span class="sxs-lookup"><span data-stu-id="8d0a4-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="8d0a4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d0a4-109">Return value</span></span>

<span data-ttu-id="8d0a4-110">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="8d0a4-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d0a4-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="8d0a4-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="8d0a4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8d0a4-112">Requirements</span></span>


| <span data-ttu-id="8d0a4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8d0a4-113">Requirement</span></span>          |    <span data-ttu-id="8d0a4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8d0a4-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0a4-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d0a4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8d0a4-116">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="8d0a4-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="8d0a4-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8d0a4-117">DLL</span></span><br/>                      | <span data-ttu-id="8d0a4-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="8d0a4-118">EndpointDlp.dll</span></span> |