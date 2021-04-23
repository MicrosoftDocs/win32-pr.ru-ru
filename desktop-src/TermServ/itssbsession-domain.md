---
title: Итссбсессион, свойство домена
description: Возвращает доменное имя пользователя.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойств домена
- Службы удаленных рабочих столов свойств домена, интерфейс Итссбсессион
- Службы удаленных рабочих столов интерфейса Итссбсессион, свойство Domain
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682113"
---
# <a name="itssbsessiondomain-property"></a><span data-ttu-id="30754-106">Итссбсессион: свойство омаин:D</span><span class="sxs-lookup"><span data-stu-id="30754-106">ITsSbSession::Domain property</span></span>

<span data-ttu-id="30754-107">Возвращает доменное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="30754-107">Retrieves the domain name of the user.</span></span>

<span data-ttu-id="30754-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="30754-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30754-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30754-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a><span data-ttu-id="30754-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="30754-110">Property value</span></span>

<span data-ttu-id="30754-111">Указатель на переменную **BSTR** , которая получает доменное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="30754-111">A pointer to a **BSTR** variable that receives the domain name of the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="30754-112">Требования</span><span class="sxs-lookup"><span data-stu-id="30754-112">Requirements</span></span>



| <span data-ttu-id="30754-113">Требование</span><span class="sxs-lookup"><span data-stu-id="30754-113">Requirement</span></span> | <span data-ttu-id="30754-114">Значение</span><span class="sxs-lookup"><span data-stu-id="30754-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30754-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30754-115">Minimum supported client</span></span><br/> | <span data-ttu-id="30754-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="30754-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="30754-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30754-117">Minimum supported server</span></span><br/> | <span data-ttu-id="30754-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30754-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="30754-119">IDL</span><span class="sxs-lookup"><span data-stu-id="30754-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30754-120"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30754-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30754-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30754-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30754-122">**итссбсессион**</span><span class="sxs-lookup"><span data-stu-id="30754-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





