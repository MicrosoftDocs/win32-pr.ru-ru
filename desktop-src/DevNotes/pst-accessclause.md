---
description: Содержит сведения о предложении доступа для защищенного хранилища.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: Структура PST_ACCESSCLAUSE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665251"
---
# <a name="pst_accessclause-structure"></a><span data-ttu-id="928be-103">\_Структура PST акцессклаусе</span><span class="sxs-lookup"><span data-stu-id="928be-103">PST\_ACCESSCLAUSE structure</span></span>

<span data-ttu-id="928be-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="928be-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="928be-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="928be-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="928be-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="928be-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="928be-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="928be-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="928be-108">Содержит сведения о предложении доступа для защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="928be-108">Contains information about the access clause for the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="928be-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="928be-109">Syntax</span></span>


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a><span data-ttu-id="928be-110">Члены</span><span class="sxs-lookup"><span data-stu-id="928be-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="928be-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="928be-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="928be-112">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="928be-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="928be-113">**клаусетипе**</span><span class="sxs-lookup"><span data-stu-id="928be-113">**ClauseType**</span></span>
</dt> <dd>

<span data-ttu-id="928be-114">Тип данных, на который указывает элемент **пбклауседата** .</span><span class="sxs-lookup"><span data-stu-id="928be-114">The type of data that is pointed to by the **pbClauseData** member.</span></span> <span data-ttu-id="928be-115">Дополнительные сведения см. в разделе [**типы PStore**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="928be-115">For more information, see [**PStore Types**](pstore-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="928be-116">**кбклауседата**</span><span class="sxs-lookup"><span data-stu-id="928be-116">**cbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="928be-117">Размер данных, на которые указывает элемент **пбклауседата** .</span><span class="sxs-lookup"><span data-stu-id="928be-117">The size of the data that is pointed to by the **pbClauseData** member.</span></span>

</dd> <dt>

<span data-ttu-id="928be-118">**пбклауседата**</span><span class="sxs-lookup"><span data-stu-id="928be-118">**pbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="928be-119">Указатель на данные предложения доступа.</span><span class="sxs-lookup"><span data-stu-id="928be-119">A pointer to the access clause data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="928be-120">Требования</span><span class="sxs-lookup"><span data-stu-id="928be-120">Requirements</span></span>



| <span data-ttu-id="928be-121">Требование</span><span class="sxs-lookup"><span data-stu-id="928be-121">Requirement</span></span> | <span data-ttu-id="928be-122">Значение</span><span class="sxs-lookup"><span data-stu-id="928be-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="928be-123">Header</span><span class="sxs-lookup"><span data-stu-id="928be-123">Header</span></span><br/> | <dl> <span data-ttu-id="928be-124"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="928be-124"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="928be-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="928be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="928be-126">**PST-файл \_ акцессруле**</span><span class="sxs-lookup"><span data-stu-id="928be-126">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> </dl>

 

 
