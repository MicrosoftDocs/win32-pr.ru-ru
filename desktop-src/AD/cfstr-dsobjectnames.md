---
title: CFSTR_DSOBJECTNAMES (DSClient. h)
description: '\_Формат буфера обмена кфстр дсобжектнамес предоставляет глобальный обработчик памяти (хглобал), содержащий структуру дсобжектнамес.'
ms.assetid: b28428fa-1504-4dcc-9b2b-32ca1ae30ec5
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOBJECTNAMES
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816f99f1b50f97ac362706cc46e4dbe4edf5f486
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135611"
---
# <a name="cfstr_dsobjectnames"></a><span data-ttu-id="75323-103">КФСТР \_ дсобжектнамес</span><span class="sxs-lookup"><span data-stu-id="75323-103">CFSTR\_DSOBJECTNAMES</span></span>

<dl> <dt>

<span data-ttu-id="75323-104"><span id="CFSTR_DSOBJECTNAMES"></span><span id="cfstr_dsobjectnames"></span>**КФСТР \_ дсобжектнамес**</span><span class="sxs-lookup"><span data-stu-id="75323-104"><span id="CFSTR_DSOBJECTNAMES"></span><span id="cfstr_dsobjectnames"></span>**CFSTR\_DSOBJECTNAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75323-105">"Дсобжектнамес"</span><span class="sxs-lookup"><span data-stu-id="75323-105">"DsObjectNames"</span></span>
</dt> <dt>



<span data-ttu-id="75323-106">Формат буфера обмена **кфстр \_ Дсобжектнамес** поддерживается [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , предоставленным методом [**икоммонкуери:: опенкуеривиндов**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) .</span><span class="sxs-lookup"><span data-stu-id="75323-106">The **CFSTR\_DSOBJECTNAMES** clipboard format is supported by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) provided by the [**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) method.</span></span> <span data-ttu-id="75323-107">Формат буфера обмена **кфстр \_ дсобжектнамес** предоставляет глобальный обработчик памяти (**хглобал**), содержащий структуру [**дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) .</span><span class="sxs-lookup"><span data-stu-id="75323-107">The **CFSTR\_DSOBJECTNAMES** clipboard format provides a global memory handle (**HGLOBAL**) that contains [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75323-108">Требования</span><span class="sxs-lookup"><span data-stu-id="75323-108">Requirements</span></span>



| <span data-ttu-id="75323-109">Требование</span><span class="sxs-lookup"><span data-stu-id="75323-109">Requirement</span></span> | <span data-ttu-id="75323-110">Значение</span><span class="sxs-lookup"><span data-stu-id="75323-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75323-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75323-111">Minimum supported client</span></span><br/> | <span data-ttu-id="75323-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75323-112">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="75323-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75323-113">Minimum supported server</span></span><br/> | <span data-ttu-id="75323-114">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75323-114">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="75323-115">Header</span><span class="sxs-lookup"><span data-stu-id="75323-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="75323-116"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="75323-116"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75323-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75323-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75323-118">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="75323-118">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[<span data-ttu-id="75323-119">**Икоммонкуери:: Опенкуеривиндов**</span><span class="sxs-lookup"><span data-stu-id="75323-119">**ICommonQuery::OpenQueryWindow**</span></span>](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[<span data-ttu-id="75323-120">**дсобжектнамес**</span><span class="sxs-lookup"><span data-stu-id="75323-120">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> </dl>

 

