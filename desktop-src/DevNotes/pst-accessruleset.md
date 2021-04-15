---
description: Определяет набор правил доступа для данных защищенного хранилища.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: Структура PST_ACCESSRULESET (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669098"
---
# <a name="pst_accessruleset-structure"></a><span data-ttu-id="82e83-103">\_Структура PST акцессрулесет</span><span class="sxs-lookup"><span data-stu-id="82e83-103">PST\_ACCESSRULESET structure</span></span>

<span data-ttu-id="82e83-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="82e83-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="82e83-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="82e83-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="82e83-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="82e83-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="82e83-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="82e83-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="82e83-108">Определяет набор правил доступа для данных защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="82e83-108">Identifies the set of access rules for the protected storage data.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e83-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82e83-109">Syntax</span></span>


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a><span data-ttu-id="82e83-110">Члены</span><span class="sxs-lookup"><span data-stu-id="82e83-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="82e83-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="82e83-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="82e83-112">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="82e83-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="82e83-113">**крулес**</span><span class="sxs-lookup"><span data-stu-id="82e83-113">**cRules**</span></span>
</dt> <dd>

<span data-ttu-id="82e83-114">Число правил в массиве **ргрулес** .</span><span class="sxs-lookup"><span data-stu-id="82e83-114">The number of rules in the **rgRules** array.</span></span>

</dd> <dt>

<span data-ttu-id="82e83-115">**ргрулес**</span><span class="sxs-lookup"><span data-stu-id="82e83-115">**rgRules**</span></span>
</dt> <dd>

<span data-ttu-id="82e83-116">Указатель на массив [**\_ акцессруленых структур PST**](pst-accessrule.md) .</span><span class="sxs-lookup"><span data-stu-id="82e83-116">A pointer to an array of [**PST\_ACCESSRULE**](pst-accessrule.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82e83-117">Требования</span><span class="sxs-lookup"><span data-stu-id="82e83-117">Requirements</span></span>



| <span data-ttu-id="82e83-118">Требование</span><span class="sxs-lookup"><span data-stu-id="82e83-118">Requirement</span></span> | <span data-ttu-id="82e83-119">Значение</span><span class="sxs-lookup"><span data-stu-id="82e83-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="82e83-120">Header</span><span class="sxs-lookup"><span data-stu-id="82e83-120">Header</span></span><br/> | <dl> <span data-ttu-id="82e83-121"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="82e83-121"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82e83-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82e83-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e83-123">**PST-файл \_ акцессруле**</span><span class="sxs-lookup"><span data-stu-id="82e83-123">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> <dt>

[<span data-ttu-id="82e83-124">**креатесубтипе**</span><span class="sxs-lookup"><span data-stu-id="82e83-124">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> </dl>

 

 
