---
description: Предоставляет системе сведения о файле документа до запуска операции открытия.
title: Функция Длпнотифипреопендокументфиле (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 12caf5230d8affce195a63da155ed6b6ca409b72
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495850"
---
# <a name="dlpnotifypreopendocumentfile-function"></a><span data-ttu-id="b1ef9-103">Функция Длпнотифипреопендокументфиле</span><span class="sxs-lookup"><span data-stu-id="b1ef9-103">DlpNotifyPreOpenDocumentFile function</span></span>

<span data-ttu-id="b1ef9-104">Предоставляет системе сведения о файле документа до запуска операции открытия.</span><span class="sxs-lookup"><span data-stu-id="b1ef9-104">Provides the system with information about a document file before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ef9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1ef9-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="b1ef9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1ef9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ef9-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1ef9-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ef9-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о открываемом документе.</span><span class="sxs-lookup"><span data-stu-id="b1ef9-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b1ef9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1ef9-109">Return value</span></span>

<span data-ttu-id="b1ef9-110">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="b1ef9-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1ef9-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="b1ef9-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b1ef9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b1ef9-112">Requirements</span></span>



| <span data-ttu-id="b1ef9-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b1ef9-113">Requirement</span></span>          |    <span data-ttu-id="b1ef9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b1ef9-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ef9-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1ef9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ef9-116">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="b1ef9-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b1ef9-117">DLL</span><span class="sxs-lookup"><span data-stu-id="b1ef9-117">DLL</span></span><br/>                      | <span data-ttu-id="b1ef9-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b1ef9-118">EndpointDlp.dll</span></span> |