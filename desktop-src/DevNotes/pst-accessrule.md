---
description: Описывает правило доступа к элементам, хранящимся в защищенном хранилище.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: Структура PST_ACCESSRULE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648939"
---
# <a name="pst_accessrule-structure"></a><span data-ttu-id="f35c4-103">\_Структура PST акцессруле</span><span class="sxs-lookup"><span data-stu-id="f35c4-103">PST\_ACCESSRULE structure</span></span>

<span data-ttu-id="f35c4-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f35c4-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f35c4-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="f35c4-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f35c4-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="f35c4-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f35c4-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="f35c4-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f35c4-108">Описывает правило доступа к элементам, хранящимся в защищенном хранилище.</span><span class="sxs-lookup"><span data-stu-id="f35c4-108">Describes a rule for access to items stored in protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="f35c4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f35c4-109">Syntax</span></span>


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a><span data-ttu-id="f35c4-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f35c4-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f35c4-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="f35c4-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="f35c4-112">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="f35c4-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="f35c4-113">**акцессмодефлагс**</span><span class="sxs-lookup"><span data-stu-id="f35c4-113">**AccessModeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f35c4-114">Режимы доступа, к которым относятся указанные наборы предложений доступа.</span><span class="sxs-lookup"><span data-stu-id="f35c4-114">The access modes to which a specified set of access clauses pertain.</span></span>



| <span data-ttu-id="f35c4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f35c4-115">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="f35c4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f35c4-116">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="f35c4-117">PST-файл <dt>**\_ ЧТЕНИЕ**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f35c4-117"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="f35c4-118">Режим доступа для чтения.</span><span class="sxs-lookup"><span data-stu-id="f35c4-118">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="f35c4-119">PST-файл <dt>**\_ ЗАПИСЬ**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f35c4-119"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="f35c4-120">Режим доступа для записи.</span><span class="sxs-lookup"><span data-stu-id="f35c4-120">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f35c4-121">**кклаусес**</span><span class="sxs-lookup"><span data-stu-id="f35c4-121">**cClauses**</span></span>
</dt> <dd>

<span data-ttu-id="f35c4-122">Количество структур в массиве **ргклаусес** .</span><span class="sxs-lookup"><span data-stu-id="f35c4-122">The number of structures in the **rgClauses** array.</span></span>

</dd> <dt>

<span data-ttu-id="f35c4-123">**ргклаусес**</span><span class="sxs-lookup"><span data-stu-id="f35c4-123">**rgClauses**</span></span>
</dt> <dd>

<span data-ttu-id="f35c4-124">Указатель на массив [**\_ акцессклаусеных структур PST**](pst-accessclause.md) .</span><span class="sxs-lookup"><span data-stu-id="f35c4-124">A pointer to an array of [**PST\_ACCESSCLAUSE**](pst-accessclause.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f35c4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f35c4-125">Requirements</span></span>



| <span data-ttu-id="f35c4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f35c4-126">Requirement</span></span> | <span data-ttu-id="f35c4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f35c4-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f35c4-128">Header</span><span class="sxs-lookup"><span data-stu-id="f35c4-128">Header</span></span><br/> | <dl> <span data-ttu-id="f35c4-129"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f35c4-129"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f35c4-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f35c4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f35c4-131">**PST-файл \_ акцессклаусе**</span><span class="sxs-lookup"><span data-stu-id="f35c4-131">**PST\_ACCESSCLAUSE**</span></span>](pst-accessclause.md)
</dt> <dt>

[<span data-ttu-id="f35c4-132">**PST-файл \_ акцессрулесет**</span><span class="sxs-lookup"><span data-stu-id="f35c4-132">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> </dl>

 

 
