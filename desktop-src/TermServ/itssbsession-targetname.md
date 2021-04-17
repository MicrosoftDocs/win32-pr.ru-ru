---
title: Итссбсессион, свойство TargetName
description: Возвращает имя целевого объекта, на котором был создан этот сеанс.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Свойство TargetName службы удаленных рабочих столов
- Свойство TargetName службы удаленных рабочих столов, интерфейс Итссбсессион
- Службы удаленных рабочих столов интерфейса Итссбсессион, свойство TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682112"
---
# <a name="itssbsessiontargetname-property"></a><span data-ttu-id="276a5-106">Свойство Итссбсессион:: TargetName</span><span class="sxs-lookup"><span data-stu-id="276a5-106">ITsSbSession::TargetName property</span></span>

<span data-ttu-id="276a5-107">Возвращает имя целевого объекта, на котором был создан этот сеанс.</span><span class="sxs-lookup"><span data-stu-id="276a5-107">Retrieves the name of the target on which this session was created.</span></span>

<span data-ttu-id="276a5-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="276a5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="276a5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="276a5-109">Syntax</span></span>


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a><span data-ttu-id="276a5-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="276a5-110">Property value</span></span>

<span data-ttu-id="276a5-111">Указатель на переменную **BSTR** , которая получает имя целевого объекта, на котором был создан этот сеанс.</span><span class="sxs-lookup"><span data-stu-id="276a5-111">A pointer to a **BSTR** variable that receives the name of the target on which this session was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="276a5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="276a5-112">Requirements</span></span>



| <span data-ttu-id="276a5-113">Требование</span><span class="sxs-lookup"><span data-stu-id="276a5-113">Requirement</span></span> | <span data-ttu-id="276a5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="276a5-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="276a5-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="276a5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="276a5-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="276a5-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="276a5-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="276a5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="276a5-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="276a5-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="276a5-119">IDL</span><span class="sxs-lookup"><span data-stu-id="276a5-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="276a5-120"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="276a5-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="276a5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="276a5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276a5-122">**итссбсессион**</span><span class="sxs-lookup"><span data-stu-id="276a5-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





