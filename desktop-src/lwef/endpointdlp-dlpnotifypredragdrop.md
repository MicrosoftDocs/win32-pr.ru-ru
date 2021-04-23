---
description: Предоставляет системе сведения о документе до инициирования операции перетаскивания.
title: Функция Длпнотифипредрагдроп (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d88a28c0dff4b13cf1c1848eeb8623c3acd1c024
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495854"
---
# <a name="dlpnotifypredragdrop-function"></a><span data-ttu-id="d4564-103">Функция Длпнотифипредрагдроп</span><span class="sxs-lookup"><span data-stu-id="d4564-103">DlpNotifyPreDragDrop function</span></span>

<span data-ttu-id="d4564-104">Предоставляет системе сведения о документе до инициирования операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="d4564-104">Provides the system with information about a document before a drag drop operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4564-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4564-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="d4564-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4564-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4564-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4564-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4564-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, связанном с операцией перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="d4564-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="d4564-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4564-109">Return value</span></span>

<span data-ttu-id="d4564-110">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="d4564-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4564-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="d4564-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="d4564-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d4564-112">Requirements</span></span>



| <span data-ttu-id="d4564-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d4564-113">Requirement</span></span>          |    <span data-ttu-id="d4564-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d4564-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4564-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4564-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d4564-116">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="d4564-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="d4564-117">DLL</span><span class="sxs-lookup"><span data-stu-id="d4564-117">DLL</span></span><br/>                      | <span data-ttu-id="d4564-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="d4564-118">EndpointDlp.dll</span></span> |