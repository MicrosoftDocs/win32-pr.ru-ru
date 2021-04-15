---
description: Типы данных для методов защищенного хранилища.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Типы PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648742"
---
# <a name="pstore-types"></a><span data-ttu-id="22823-103">Типы PStore</span><span class="sxs-lookup"><span data-stu-id="22823-103">PStore Types</span></span>

<span data-ttu-id="22823-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="22823-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="22823-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="22823-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="22823-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="22823-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="22823-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="22823-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="22823-108">Типы данных для методов защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="22823-108">The data types for Protected Storage methods.</span></span>


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

<span data-ttu-id="22823-109">**PST-файл \_ ACCESSMODE**</span><span class="sxs-lookup"><span data-stu-id="22823-109">**PST\_ACCESSMODE**</span></span>
</dt> <dd>

<span data-ttu-id="22823-110">Определяет режим чтения или записи правила доступа.</span><span class="sxs-lookup"><span data-stu-id="22823-110">Defines the read or write mode of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="22823-111">**PST-файл \_ акцессклаусетипе**</span><span class="sxs-lookup"><span data-stu-id="22823-111">**PST\_ACCESSCLAUSETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="22823-112">Определяет тип предложения правила доступа.</span><span class="sxs-lookup"><span data-stu-id="22823-112">Defines the clause type of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="22823-113">**\_ключ PST**</span><span class="sxs-lookup"><span data-stu-id="22823-113">**PST\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="22823-114">Определяет ключ для хранимого элемента.</span><span class="sxs-lookup"><span data-stu-id="22823-114">Defines the key for the stored item.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22823-115">Требования</span><span class="sxs-lookup"><span data-stu-id="22823-115">Requirements</span></span>



| <span data-ttu-id="22823-116">Требование</span><span class="sxs-lookup"><span data-stu-id="22823-116">Requirement</span></span> | <span data-ttu-id="22823-117">Значение</span><span class="sxs-lookup"><span data-stu-id="22823-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22823-118">Header</span><span class="sxs-lookup"><span data-stu-id="22823-118">Header</span></span><br/> | <dl> <span data-ttu-id="22823-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="22823-119"><dt>Pstore.h</dt></span></span> </dl> |



 

 
