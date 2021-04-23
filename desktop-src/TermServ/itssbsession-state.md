---
title: Итссбсессион State, свойство
description: Возвращает или задает состояние сеанса.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- Свойство State службы удаленных рабочих столов
- Свойство State службы удаленных рабочих столов, интерфейс Итссбсессион
- Интерфейс Итссбсессион службы удаленных рабочих столов, свойство State
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492993"
---
# <a name="itssbsessionstate-property"></a><span data-ttu-id="e5178-106">Свойство Итссбсессион:: State</span><span class="sxs-lookup"><span data-stu-id="e5178-106">ITsSbSession::State property</span></span>

<span data-ttu-id="e5178-107">Возвращает или задает состояние сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5178-107">Retrieves or specifies the session state.</span></span>

<span data-ttu-id="e5178-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e5178-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5178-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5178-109">Syntax</span></span>


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a><span data-ttu-id="e5178-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e5178-110">Property value</span></span>

<span data-ttu-id="e5178-111">Значение перечисления [**\_ состояния тссессион**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) , указывающее состояние сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5178-111">A value of the [**TSSESSION\_STATE**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) enumeration that indicates the state of a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5178-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e5178-112">Requirements</span></span>



| <span data-ttu-id="e5178-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e5178-113">Requirement</span></span> | <span data-ttu-id="e5178-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e5178-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5178-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5178-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e5178-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e5178-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e5178-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5178-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e5178-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5178-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e5178-119">IDL</span><span class="sxs-lookup"><span data-stu-id="e5178-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5178-120"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5178-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5178-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5178-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5178-122">**итссбсессион**</span><span class="sxs-lookup"><span data-stu-id="e5178-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[<span data-ttu-id="e5178-123">**\_состояние тссессион**</span><span class="sxs-lookup"><span data-stu-id="e5178-123">**TSSESSION\_STATE**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





