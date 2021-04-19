---
description: Предоставляет системе сведения о документе после завершения операции перетаскивания.
title: Функция Длпнотифипостдрагдроп (ендпоинтдлп. h)
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
ms.openlocfilehash: 468255cee3c3fef44e44dd033b541e317db3d268
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495894"
---
# <a name="dlpnotifypostdragdrop-function"></a><span data-ttu-id="3d00e-103">Функция Длпнотифипостдрагдроп</span><span class="sxs-lookup"><span data-stu-id="3d00e-103">DlpNotifyPostDragDrop function</span></span>

<span data-ttu-id="3d00e-104">Предоставляет системе сведения о документе после завершения операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="3d00e-104">Provides the system with information about a document after a drag drop operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d00e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d00e-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="3d00e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d00e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d00e-107">*Документинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d00e-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d00e-108">Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, связанном с операцией перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="3d00e-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3d00e-109">*Опстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d00e-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d00e-110">Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="3d00e-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drag drop.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="3d00e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d00e-111">Return value</span></span>

<span data-ttu-id="3d00e-112">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="3d00e-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d00e-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="3d00e-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="3d00e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3d00e-114">Requirements</span></span>



| <span data-ttu-id="3d00e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3d00e-115">Requirement</span></span>          |    <span data-ttu-id="3d00e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3d00e-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d00e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d00e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3d00e-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="3d00e-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="3d00e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3d00e-119">DLL</span></span><br/>                      | <span data-ttu-id="3d00e-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="3d00e-120">EndpointDlp.dll</span></span> |