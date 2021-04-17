---
title: Структура TSMF_SUPPORT_DATA_IN
description: Содержит сведения о форматах мультимедиа. | Структура TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN структуры службы удаленных рабочих столов
- PTSMF_SUPPORT_DATA_IN службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684892"
---
# <a name="tsmf_support_data_in-structure"></a><span data-ttu-id="cfdf9-106">\_Данные поддержки \_ тсмф \_ в структуре</span><span class="sxs-lookup"><span data-stu-id="cfdf9-106">TSMF\_SUPPORT\_DATA\_IN structure</span></span>

<span data-ttu-id="cfdf9-107">Содержит сведения о форматах мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cfdf9-107">Contains information about media formats.</span></span> <span data-ttu-id="cfdf9-108">Эта структура используется методом [**куерипроперти**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) во время запросов **\_ \_ \_ \_ поддержки формата врдс запросов MF** .</span><span class="sxs-lookup"><span data-stu-id="cfdf9-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfdf9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfdf9-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a><span data-ttu-id="cfdf9-110">Члены</span><span class="sxs-lookup"><span data-stu-id="cfdf9-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="cfdf9-111">**гуидмфсессион**</span><span class="sxs-lookup"><span data-stu-id="cfdf9-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="cfdf9-112">Сеанс.</span><span class="sxs-lookup"><span data-stu-id="cfdf9-112">The session.</span></span>

</dd> <dt>

<span data-ttu-id="cfdf9-113">**нументриес**</span><span class="sxs-lookup"><span data-stu-id="cfdf9-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="cfdf9-114">Количество структур в данных переменной длины.</span><span class="sxs-lookup"><span data-stu-id="cfdf9-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="cfdf9-115">**...**</span><span class="sxs-lookup"><span data-stu-id="cfdf9-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="cfdf9-116">Переменное число структур, содержащих данные в формате мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cfdf9-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfdf9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cfdf9-117">Requirements</span></span>



| <span data-ttu-id="cfdf9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cfdf9-118">Requirement</span></span> | <span data-ttu-id="cfdf9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cfdf9-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="cfdf9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfdf9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfdf9-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cfdf9-121">None supported</span></span><br/>         |
| <span data-ttu-id="cfdf9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfdf9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfdf9-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfdf9-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfdf9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfdf9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfdf9-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="cfdf9-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="cfdf9-126">**\_Поддержка тсмф \_ нодедата \_ в**</span><span class="sxs-lookup"><span data-stu-id="cfdf9-126">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





