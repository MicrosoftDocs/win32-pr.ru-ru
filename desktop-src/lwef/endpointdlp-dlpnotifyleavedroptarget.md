---
description: Предоставляет системе сведения о документе при выходе из целевого объекта перетаскивания.
title: Функция Длпнотифилеаведроптаржет (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyLeaveDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2f96ea9a825ca930631fe94dd1a3d632019dd9c1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495905"
---
# <a name="dlpnotifyleavedroptarget-function"></a><span data-ttu-id="75183-103">Функция Длпнотифилеаведроптаржет</span><span class="sxs-lookup"><span data-stu-id="75183-103">DlpNotifyLeaveDropTarget function</span></span>

<span data-ttu-id="75183-104">Предоставляет системе сведения о документе при выходе из целевого объекта перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="75183-104">Provides the system with information about a document when a drop target is exited.</span></span>

## <a name="syntax"></a><span data-ttu-id="75183-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75183-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="75183-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75183-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75183-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75183-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, связанном с операцией Drop.</span><span class="sxs-lookup"><span data-stu-id="75183-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="75183-109">*Опстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75183-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75183-110">Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии операции выхода из целевого объекта Drop.</span><span class="sxs-lookup"><span data-stu-id="75183-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drop target exit operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="75183-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75183-111">Return value</span></span>

<span data-ttu-id="75183-112">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="75183-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="75183-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="75183-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="75183-114">Требования</span><span class="sxs-lookup"><span data-stu-id="75183-114">Requirements</span></span>



| <span data-ttu-id="75183-115">Требование</span><span class="sxs-lookup"><span data-stu-id="75183-115">Requirement</span></span>          |    <span data-ttu-id="75183-116">Значение</span><span class="sxs-lookup"><span data-stu-id="75183-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75183-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75183-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75183-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="75183-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="75183-119">DLL</span><span class="sxs-lookup"><span data-stu-id="75183-119">DLL</span></span><br/>                      | <span data-ttu-id="75183-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="75183-120">EndpointDlp.dll</span></span> |