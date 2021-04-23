---
description: Предоставляет системе сведения о документе при входе в цель перетаскивания.
title: Функция Длпнотифентердроптаржет (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ec1eee1cee7bbcc38ce3094e3e2f8b650cf3b2a9
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495900"
---
# <a name="dlpnotifyenterdroptarget-function"></a><span data-ttu-id="6b254-103">Функция Длпнотифентердроптаржет</span><span class="sxs-lookup"><span data-stu-id="6b254-103">DlpNotifyEnterDropTarget function</span></span>

<span data-ttu-id="6b254-104">Предоставляет системе сведения о документе при входе в цель перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="6b254-104">Provides the system with information about a document when a drop target is entered.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b254-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b254-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="6b254-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b254-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b254-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b254-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, связанном с операцией Drop.</span><span class="sxs-lookup"><span data-stu-id="6b254-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="6b254-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b254-109">Return value</span></span>

<span data-ttu-id="6b254-110">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="6b254-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b254-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="6b254-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="6b254-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6b254-112">Requirements</span></span>



| <span data-ttu-id="6b254-113">Требование</span><span class="sxs-lookup"><span data-stu-id="6b254-113">Requirement</span></span>          |    <span data-ttu-id="6b254-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6b254-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b254-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b254-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6b254-116">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="6b254-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="6b254-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6b254-117">DLL</span></span><br/>                      | <span data-ttu-id="6b254-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="6b254-118">EndpointDlp.dll</span></span> |