---
title: Итссбтаскинфо, свойство контекста
description: Извлекает байты контекста, связанные с задачей.
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства контекста
- Свойство Context службы удаленных рабочих столов, интерфейс Итссбтаскинфо
- Службы удаленных рабочих столов интерфейса Итссбтаскинфо, свойство Context
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2adc4715f23b2c23ac6dfbdcdd8a489b2b0f5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137502"
---
# <a name="itssbtaskinfocontext-property"></a><span data-ttu-id="940e4-106">Свойство Итссбтаскинфо:: Context</span><span class="sxs-lookup"><span data-stu-id="940e4-106">ITsSbTaskInfo::Context property</span></span>

<span data-ttu-id="940e4-107">Извлекает байты контекста, связанные с задачей.</span><span class="sxs-lookup"><span data-stu-id="940e4-107">Retrieves the context bytes associated with the task.</span></span>

<span data-ttu-id="940e4-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="940e4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="940e4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="940e4-109">Syntax</span></span>


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a><span data-ttu-id="940e4-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="940e4-110">Property value</span></span>

<span data-ttu-id="940e4-111">Контекст задачи.</span><span class="sxs-lookup"><span data-stu-id="940e4-111">The context of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="940e4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="940e4-112">Requirements</span></span>



| <span data-ttu-id="940e4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="940e4-113">Requirement</span></span> | <span data-ttu-id="940e4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="940e4-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="940e4-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="940e4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="940e4-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="940e4-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="940e4-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="940e4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="940e4-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="940e4-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="940e4-119">IDL</span><span class="sxs-lookup"><span data-stu-id="940e4-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="940e4-120"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="940e4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="940e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940e4-122">**итссбтаскинфо**</span><span class="sxs-lookup"><span data-stu-id="940e4-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





