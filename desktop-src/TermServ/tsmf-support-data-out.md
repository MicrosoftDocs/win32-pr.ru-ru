---
title: Структура TSMF_SUPPORT_DATA_OUT
description: Содержит сведения о форматах мультимедиа. | Структура TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT структуры службы удаленных рабочих столов
- PTSMF_SUPPORT_DATA_OUT службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000082"
---
# <a name="tsmf_support_data_out-structure"></a><span data-ttu-id="c8daf-106">\_ \_ Структура out данных поддержки тсмф \_</span><span class="sxs-lookup"><span data-stu-id="c8daf-106">TSMF\_SUPPORT\_DATA\_OUT structure</span></span>

<span data-ttu-id="c8daf-107">Содержит сведения о форматах мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c8daf-107">Contains information about media formats.</span></span> <span data-ttu-id="c8daf-108">Эта структура используется методом [**куерипроперти**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) во время запросов **\_ \_ \_ \_ поддержки формата врдс запросов MF** .</span><span class="sxs-lookup"><span data-stu-id="c8daf-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8daf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8daf-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a><span data-ttu-id="c8daf-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c8daf-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c8daf-111">**гуидмфсессион**</span><span class="sxs-lookup"><span data-stu-id="c8daf-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="c8daf-112">Оно должно соответствовать свойству **гуидмфсессион** в соответствующих [**\_ данных поддержки тсмф \_ \_ в**](tsmf-support-data-in.md) структуре.</span><span class="sxs-lookup"><span data-stu-id="c8daf-112">This must match the **guidMfSession** property in the corresponding [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c8daf-113">**нументриес**</span><span class="sxs-lookup"><span data-stu-id="c8daf-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c8daf-114">Количество структур в данных переменной длины.</span><span class="sxs-lookup"><span data-stu-id="c8daf-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="c8daf-115">**...**</span><span class="sxs-lookup"><span data-stu-id="c8daf-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="c8daf-116">Переменное число структур, содержащих данные в формате мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c8daf-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8daf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c8daf-117">Requirements</span></span>



| <span data-ttu-id="c8daf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c8daf-118">Requirement</span></span> | <span data-ttu-id="c8daf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c8daf-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="c8daf-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8daf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c8daf-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c8daf-121">None supported</span></span><br/>         |
| <span data-ttu-id="c8daf-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8daf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c8daf-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8daf-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8daf-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8daf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8daf-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="c8daf-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="c8daf-126">**ТСМФ \_ Поддержка \_ нодедата \_**</span><span class="sxs-lookup"><span data-stu-id="c8daf-126">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





