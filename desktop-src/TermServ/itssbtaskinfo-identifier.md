---
title: Итссбтаскинфо, свойство идентификатора
description: Извлекает идентификатор GUID, используемый агентом задачи в качестве уникального идентификатора.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства идентификатора
- Свойство идентификатора службы удаленных рабочих столов, интерфейс Итссбтаскинфо
- Службы удаленных рабочих столов интерфейса Итссбтаскинфо, свойство identifier
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803880"
---
# <a name="itssbtaskinfoidentifier-property"></a><span data-ttu-id="8b272-106">Свойство Итссбтаскинфо:: identifier</span><span class="sxs-lookup"><span data-stu-id="8b272-106">ITsSbTaskInfo::Identifier property</span></span>

<span data-ttu-id="8b272-107">Извлекает идентификатор GUID, используемый агентом задачи в качестве уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="8b272-107">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

<span data-ttu-id="8b272-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8b272-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b272-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b272-109">Syntax</span></span>


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a><span data-ttu-id="8b272-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8b272-110">Property value</span></span>

<span data-ttu-id="8b272-111">Указатель на значение **BSTR** , которое получает идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="8b272-111">A pointer to a **BSTR** value that receives the GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b272-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8b272-112">Requirements</span></span>



| <span data-ttu-id="8b272-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8b272-113">Requirement</span></span> | <span data-ttu-id="8b272-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8b272-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b272-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b272-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8b272-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8b272-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="8b272-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b272-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8b272-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b272-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="8b272-119">IDL</span><span class="sxs-lookup"><span data-stu-id="8b272-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b272-120"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b272-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b272-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b272-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b272-122">**итссбтаскинфо**</span><span class="sxs-lookup"><span data-stu-id="8b272-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





