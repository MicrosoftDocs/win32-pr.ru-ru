---
title: Итссбтаскинфо, свойство метки
description: Извлекает метку, которая описывает назначение задачи.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства метки
- Свойство метки службы удаленных рабочих столов, интерфейс Итссбтаскинфо
- Службы удаленных рабочих столов интерфейса Итссбтаскинфо, свойство Label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803779"
---
# <a name="itssbtaskinfolabel-property"></a><span data-ttu-id="2b55e-106">Итссбтаскинфо:: Label, свойство</span><span class="sxs-lookup"><span data-stu-id="2b55e-106">ITsSbTaskInfo::Label property</span></span>

<span data-ttu-id="2b55e-107">Извлекает метку, которая описывает назначение задачи.</span><span class="sxs-lookup"><span data-stu-id="2b55e-107">Retrieves the label that describes the purpose of the task.</span></span>

<span data-ttu-id="2b55e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2b55e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b55e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b55e-109">Syntax</span></span>


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a><span data-ttu-id="2b55e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2b55e-110">Property value</span></span>

<span data-ttu-id="2b55e-111">Указатель на значение **BSTR** , содержащее метку.</span><span class="sxs-lookup"><span data-stu-id="2b55e-111">A pointer to a **BSTR** value that contains the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b55e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2b55e-112">Requirements</span></span>



| <span data-ttu-id="2b55e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2b55e-113">Requirement</span></span> | <span data-ttu-id="2b55e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2b55e-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b55e-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b55e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2b55e-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2b55e-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="2b55e-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b55e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2b55e-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b55e-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="2b55e-119">IDL</span><span class="sxs-lookup"><span data-stu-id="2b55e-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b55e-120"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b55e-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b55e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b55e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b55e-122">**итссбтаскинфо**</span><span class="sxs-lookup"><span data-stu-id="2b55e-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





