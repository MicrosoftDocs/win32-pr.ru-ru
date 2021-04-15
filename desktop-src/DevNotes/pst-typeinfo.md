---
description: Описывает тип или подтип.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: Структура PST_TYPEINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648983"
---
# <a name="pst_typeinfo-structure"></a><span data-ttu-id="02927-103">\_Структура файла подструктуры PST</span><span class="sxs-lookup"><span data-stu-id="02927-103">PST\_TYPEINFO structure</span></span>

<span data-ttu-id="02927-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02927-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="02927-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="02927-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="02927-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="02927-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="02927-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="02927-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="02927-108">Описывает тип или подтип.</span><span class="sxs-lookup"><span data-stu-id="02927-108">Describes a type or a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="02927-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02927-109">Syntax</span></span>


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="02927-110">Члены</span><span class="sxs-lookup"><span data-stu-id="02927-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="02927-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="02927-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="02927-112">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="02927-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="02927-113">**сздисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="02927-113">**szDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="02927-114">Указатель на строку расширенных символов, представляющую отображаемое имя типа.</span><span class="sxs-lookup"><span data-stu-id="02927-114">A pointer to a wide character string that represents the display name for the type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02927-115">Требования</span><span class="sxs-lookup"><span data-stu-id="02927-115">Requirements</span></span>



| <span data-ttu-id="02927-116">Требование</span><span class="sxs-lookup"><span data-stu-id="02927-116">Requirement</span></span> | <span data-ttu-id="02927-117">Значение</span><span class="sxs-lookup"><span data-stu-id="02927-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02927-118">Header</span><span class="sxs-lookup"><span data-stu-id="02927-118">Header</span></span><br/> | <dl> <span data-ttu-id="02927-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="02927-119"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02927-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02927-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02927-121">**креатесубтипе**</span><span class="sxs-lookup"><span data-stu-id="02927-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> <dt>

[<span data-ttu-id="02927-122">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="02927-122">**CreateType**</span></span>](ipstore-createtype.md)
</dt> <dt>

[<span data-ttu-id="02927-123">**жетсубтипеинфо**</span><span class="sxs-lookup"><span data-stu-id="02927-123">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)
</dt> <dt>

[<span data-ttu-id="02927-124">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="02927-124">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
