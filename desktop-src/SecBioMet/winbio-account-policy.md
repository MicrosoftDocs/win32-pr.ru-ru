---
title: Структура WINBIO_ACCOUNT_POLICY (Винбио \_ Adapter. h)
description: Содержит политику антиподмены по умолчанию или учетную запись.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- API структуры WINBIO_ACCOUNT_POLICY биометрическая платформа Windows
- PWINBIO_ACCOUNT_POLICY API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988650"
---
# <a name="winbio_account_policy-structure"></a><span data-ttu-id="b4714-105">\_Структура политики учетных записей винбио \_</span><span class="sxs-lookup"><span data-stu-id="b4714-105">WINBIO\_ACCOUNT\_POLICY structure</span></span>

<span data-ttu-id="b4714-106">Структура **\_ \_ политики учетных записей винбио** содержит политику антиподмены по умолчанию или учетную запись.</span><span class="sxs-lookup"><span data-stu-id="b4714-106">The **WINBIO\_ACCOUNT\_POLICY** structure contains either a default or account-specific antispoofing policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4714-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4714-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a><span data-ttu-id="b4714-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b4714-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4714-109">**Удостоверение**</span><span class="sxs-lookup"><span data-stu-id="b4714-109">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="b4714-110">Структура [**\_ идентификации винбио**](winbio-identity.md) , указывающая сведения об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b4714-110">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that specifies the account information.</span></span>

</dd> <dt>

<span data-ttu-id="b4714-111">**антиспуфбехавиор**</span><span class="sxs-lookup"><span data-stu-id="b4714-111">**AntiSpoofBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="b4714-112">Одно из значений [**перечисления \_ \_ \_ \_ действий политики антифишинга винбио**](winbio-anti-spoof-policy-action.md) , которое указывает действие политики подделки, которое будет использоваться для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b4714-112">One of the [**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**](winbio-anti-spoof-policy-action.md) enumeration values that specifies what antispoofing policy action to use for the account.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4714-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4714-113">Remarks</span></span>

<span data-ttu-id="b4714-114">Описание того, как используется эта структура, см. в обсуждении метода [**енгинеадаптерсетаккаунтполици**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .</span><span class="sxs-lookup"><span data-stu-id="b4714-114">See the discussion of the [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) method for a description of how this structure is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4714-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b4714-115">Requirements</span></span>



| <span data-ttu-id="b4714-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b4714-116">Requirement</span></span> | <span data-ttu-id="b4714-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b4714-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4714-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4714-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4714-119">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b4714-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="b4714-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4714-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4714-121">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="b4714-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="b4714-122">Header</span><span class="sxs-lookup"><span data-stu-id="b4714-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4714-123"><dt>Винбио \_ Adapter. h (включить винбио \_ Adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4714-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





